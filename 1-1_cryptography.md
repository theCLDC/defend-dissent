## What is encryption?

Let's start with the basics -- think, "pen and paper encryption" -- before moving on to more complex encryption methods made possible by computers.

#### What you'll learn

1. The basic elements of encryption: the *plaintext*, the *ciphertext*, the *cipher* (or *encryption protocol*), the *cryptographic key*.
2. How some classic encryption methods work.
3. Ways that encryption can be broken.
4. An unbreakable cipher.

Encryption is the process of scrambling a message so that it can only be unscrambled (and read) by the intended parties. The method by which you scramble the original message, or _plaintext_, is called the _cipher_ or _encryption protocol_. In almost all cases, the cipher is not intended to be kept secret. The scrambled, unreadable, encrypted message is called the *ciphertext*, and can be safely shared. Most ciphers require an additional piece of information, called a *cryptographic key* to encrypt and decrypt (scramble and unscramble) messages.  

### A simple cipher: The Caesar cipher

Consider first, perhaps the simplest cipher: the _Caesar cipher_.  Here, each letter in the message is shifted by an agreed-upon number of letters in the alphabet. For example, suppose you wanted to encrypt the *plaintext*:

```
IF VOTING CHANGED ANYTHING IT WOULD BE ILLEGAL
```

by shifting each letter in the message forward by three places in the alphabet, so that `A` becomes `D`, `B` becomes `E` and so on, with `Z` wrapping around to the start of the alphabet to become `C`. The plaintext gets encrypted to the following *ciphertext*:

```
LI YRWLQJ FKDQJHG DQBWKLQJ LW ZRXOG EH LOOHJDO
```

To decrypt this message, the recipient would do the reverse, shifting each letter in the message backward three places in the alphabet, so `Z` becomes `W` and `A` wraps around through the end of the alphabet to become `X`. For the recipient to be able to decrypt the message (quickly), they would have to know the _key_ to the cipher.  For the Caesar cipher, this is the number of places that each letter is shifted in the alphabet; in this example, it is the number `3`.  A Caesar cipher key can also represented by a letter of the alphabet corresponding to the result of the translation from `A`.  For example, a shift of `3` would be the key `D`, a shift of `23` would be the key `Z`, the shift of zero (the identity shift) would be the key `A`.   

Let's review the terms: in this example, the *cipher* (or *encryption protocol*) is, simply, "to encrypt, shift each letter in the message plaintext forward in the alphabet by **n** letters.  To decrypt, shift each letter in the message ciphertext backward in the alphabet by **n** letters."  The *key* is the amount of the shift, **n**.

Of course, the Caesar cipher is not a strong cipher, and you certainly shouldn't trust it to keep your secret plans secret. All an adversary would need to do to _break_ (or *crack*) your secret code (ciphertext) is to try every possible backward shift through the alphabet. There are not many possibilities, so this wouldn't take long: since the key `A` makes the ciphertext equal the plaintext, there are only 25 possible keys. Such an _attack_ is called a _brute force_ aEach ttack, in which an adversary attempts to decipher an encrypted message by trying every possible key.  This attack is feasible in the case of the Caesar cipher because there are very few possible keys.

### A slightly more complicated cipher: The Vigen&egrave;re cipher

The Vigen&egrave;re cipher is a set of Caesar ciphers, each with their own key.  Typically the key is given as a word where the position of the word's letter in the alphabet indicates how the letter `A` is shifted as in a Caesar cipher. This is easiest to see with an example.  Suppose you wish to encrypt the plaintext:

```RESPECT EXISTENCE OR EXPECT RESISTANCE```

with the key

```ACT```

Then:

* Encrypt every third letter starting with the first letter of the plaintext (`R`, `P`, `T`...) with a Caesar cipher that maps `A` to `A` (a shift of zero, or a Caesar cipher with the key `A` or`0`).
* Encrypt every third starting with the second letter of the plaintext (`E`, `E`, `E`...) with a Caesar cipher that maps `A` to `C` (a Caesar cipher using the key `C` or `2`).
* Encrypt every third letter starting with the third letter of the plaintext (`S`, `C`, `X`) with a Caesar cipher that maps `A` to `T` (a Caesar cipher using the key `19`).

Applying these three Caesar ciphers results in the ciphertext:

```RGLPGVT GQIUMEPVE QK EZIEEM RGLIUMAPVE```

To break this cipher, suppose your adversary knows the length of your key: your adversary would try to decrypt the ciphertext with all possible three-letter words (or, in general, any three-letter sequence of letters) of that length.  In this example, that would require at most `26 x 26 x 26 = 17576` attempts, which is more than could be easily attempted by hand, but is trivially done by a computer.  If your adversary doesn't know the length of your key, then they would have to try many more possible keys (perhaps `25 + 26 x 26 + 26 x 26 x 26 + (26)^4...`) to apply this brute force method to break the encryption.  Notice that the longer your key is, the more difficult brute force methods are--and the harder an adversary must work to break the encryption.

### In context: The unbreakable one-time pad

A Vigen&egrave;re cipher whose key is a sequence of **randomly** selected letters and that is as at least as long as a message plaintext makes possible a cipher known as the _one-time pad_. Historically, the key itself would be written in a pad of paper, distributed among communicating parties. To encrypt, a Vigen&egrave;re cipher is applied to the plaintext where each letter in the one-time pad is used only once before proceeding to the next letter, and so on. Decryption relies on possession of this one-time pad, and the starting position in the key. It is **impossible** to break this cipher without the key--that is, it is impossible to guess the key and crack the ciphertext, even with unlimited time and resources. This is because a ciphertext of a given length could correspond to  any plaintext of the same length. For example, without knowledge of the random key, the one-time pad-encrypted ciphertext `sou ducyfuk rxl hqkpj` could (with equal probability) correspond to either the plaintext `all animals are equal` or `few animals are happy`. Without the key, there is no way to know what the intended (plaintext) message is!  Omitting spaces between words or encrypting the spaces between words (using a 27-letter alphabet, `ABCDEFGHIJKLMNOPQRSTUVWXYZ_`, where `_` is a space) would make it far more difficult to guess even the set of possible plaintext messages.

Of course, the one-time pad has the practical problem of how to exchange the key (the one-time pad itself), which is as long as the message, or as long as the total length of all possible future messages.  Despite that, it has been used historically, allowing for groups to share a one-time pad in person and then send messages over insecure channels.  In the late 1980's, the African National Congress (the ANC--at the time, fighting apartheid in South Africa) used one-time pads to encrypt messages between foreign supporters and in-country operatives.  The one-time pads (the keys) were physically transported by a trusted air stewardess who worked the Amsterdam-to-Johannesburg route. Incidentally, the ANC also computerized the encryption and decryption--making it possible to translate encrypted messages into tonal sequences transmitted over a phone connection and recorded to, or received from, an answering machine, allowing for *asynchronous* communication.

#### What to learn next

* [Modern Cryptography](1-2_modern-cryptography.md)
* [Key Exchange: How to agree on a cryptographic key over the Internet](1-3_key-exchange.md)

#### External resources

[Talking To Vula: The Story of the Secret Underground Communications Network of Operation Vula](http://www.anc.org.za/content/talking-vula)