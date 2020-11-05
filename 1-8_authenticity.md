## Authenticity through Cryptographic Signing

> We recommend that you read the Chapters on [Public Key Cryptography](1-7_public-key-cryptography.md) and [Cryptographic Hash](1-4_cryptographic-hash.md) before reading this chapter.

#### What you'll learn

1. How to achieve the digital equivalent of a signature.
1. How cryptographic signatures can be used to provide authenticity.
1. What electronic authenticity means.
1. How cryptographic signatures can be used to propagate trust.

---

Public key cryptographic systems can often be used to provide authenticity.  In PGP, this is allowed by the complementary nature of the public and private keys. In the beginning, two cryptographic keys are created and either key can be used as the public key, and the choice as to which is the public key is really just an arbitrary assignment.  That is, either key can be used for encryption as long as the other one is used for decryption (and the one used for decryption is kept private to provide security).

Once you have assigned one cryptographic key as the public key and the other cryptographic key as the private key, you could still choose to encrypt a message with your private key.  However, then anyone with your public key could decrypt the message.  If you make your public key, well, public, then anyone could decrypt your message, and so this would defeat the purpose of using encryption to achieve message privacy.

However, this should illustrate to you that the only person who could have encrypted a message that can be decrypted with *your* public key is *you*, the person with *your private key*.  Encrypting a message with your private key provides the digital equivalent of a signature and is called *cryptographic signing*.  In fact, cryptographic signing provides two properties of *authenticity*:

1. **Attribution:** You wrote the message (and not someone else).

1. **Integrity:** The message is received as it was written, that is, it has not been altered.

The second property comes from the fact that a tamperer would have to alter the ciphertext such that decrypting the ciphertext with your public key generates the tamperers desired altered plaintext.  But this is completely infeasible.

These properties are only meaningful if you are the only one who controls your private key, since anyone who gains control of your private key could cryptographically sign their own altered text.

### Cryptographically signing cryptographic hashes

In practice, rather than encrypting the entire message, one would encrypt a cryptographic hash (a.k.a. digest or fingerprint) of the message for the purpose of cryptographic signing.  This is done for efficiency reasons.  Let's consider the protocol for Assata signing a message and Bobby verifying the signature, pictured below.

Assata takes a cryptographic hash of her message and encrypts the result with her private key, creating a signature, which she can attach to the message:

![](pictures/pgpsigning1.png)

Bobby takes the signature and decrypts it using Assata's public key giving the hash that is the same as what Assata generated.  He then takes his own cryptographic hash of the message and compares the result to the decrypted hash he received from Assata:

![](pictures/pgpsigning2.png)

Recall that cryptographic hash functions are infeasible to counterfeit.  So, if the two hashes that Bobby generates (one directly from Assata's message and one from Assata's signature) are the same then we know two things:

1. Only Assata could have generated the signature.  Only Assata could encrypt something that can be decrypted with her public key, since she is the only one with her private key.
1. The message has not been altered since Assata wrote it.  If someone altered the message, then the  hash of the message would differ from the hash contained in the signature.  Any counterfeiter would therefore have to forge a new signature, but can't generate one without Assata's private key.

Authenticity, cryptographically.

Note that Edgar, in a man-in-the-middle attack, could simply remove the signature.  So, for cryptographic signing to be effective, you need to agree to use cryptographic signing all the time.  Modern end-to-end encrypted messaging apps generally have signing built inby default, though this is often invisible to the average user.

### Applications of cryptographic signing

As in our example above, cryptographic signing can provide authenticity to messages in a similar way to traditional hand-written signatures and wax seals.  However, you can cryptographically sign more than just messages (such as emails).

#### Verifying software

Perhaps the most explicit and common use of cryptographic signatures is for verifying software, even if you aren't aware of it.  Software, such as apps, will only do what their developers want and say they will do if they haven't been tampered on the way from the developer to your computer or phone.  Responsible developers will sign their products, in the same way as we describe for messages.  A program or app is really just a computer file (or set of files), which is just a sequence of characters, or a type of message.  If a developer has signed their software using public key cryptography, a careful users can check the signature by getting the developer's public key and performing the validation illustrated above.  (The developer should provide their public key via a channel different from the one you downloaded the software from.  This would allow an out-of-band comparison as described in the Chapter on [The Man in the Middle](1-5_man-in-the-middle.md) -- the public key, which you use for validation, is out-of-band from the message, or software download.)

#### Managing fingerprint validation and the web of trust

To trust Assata's public key, Bobby should really verify her public key by checking the fingerprint of key as [we have described](1-5_man-in-the-middle.md).  Otherwise, Edgar the interloper could furnish Bobby with a public key that he holds the corresponding private key for.  But, if Bobby has verified that Assata's public key is genuinely hers, Bobby can cryptographically sign Assata's public key (with his own private key).  This allows Bobby to keep track of the public keys that he has verified and allows him to share Assata's key with other people as follows.

Suppose Cleaver wants to send Assata an encrypted message, and wants to be sure that Edgar is not going to play the man in the middle.  But Cleaver does not have a secondary channel to verify Assata's public key through.  However, Cleaver has received and verified Bobby's public key.  So Bobby can send Assata's public key to Cleaver with his signature.  If Cleaver trusts Bobby, and has verified his public key, then Cleaver can verify his signature on Assata's public key and trust that Assata's public key is genuine.

This is the basis of the web of trust.  Rather than directly verifying fingerprints of keys, you can do so indirectly, as long as there is a path of trust between you and your desired correspondent.

### In context: Warrant canaries

Warrant canaries or canary statements inform users that the provider has *not*, by the published date, been subject to legal or other processes that might put users at risk, such as data breaches, being compelled to release encryption keys, or provide back-doors into the system.  If the statement is not updated according to a published schedule, users can infer that there has been a problem that may put their past or future data at risk.  Riseup.net, for example, maintains a quarterly canary statement which is cryptographically signed so that you can ensure its authenticity: that is, that that the people at riseup.net wrote the statement.  They include a link to a news article dated on the day of release in their statement to give evidence that the statement was not published before the day of release.

The use of warrant canaries began as a way to circumvent gag orders in the US which accompany some legal processes in which the US government can force someone to withhold speech.  On the other hand, the US government can rarely force someone to say something (particularly that isn't true) and so could not compel a provider to keep up a canary statement that falsely claims nothing has happened.

The term originates from the use of canaries in coal mines to detect poisonous gases: if the canary dies, get to clean air quickly!

#### What to learn next

* [Metadata](1-9_metadata.md)

#### External resources

* [Tor Project: How to Verify Signatures for Packages](https://www.torproject.org/docs/verifying-signatures.html.en)
* [Riseup.net's Canary Statement](https://riseup.net/canary)


