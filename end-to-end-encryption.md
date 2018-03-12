(to merge into [modern crypto](modern-cryptography.md))

## End-to-End Encryption

End-to-end encryption involves scrambling a message so that it can only be read by the endpoints of a conversation.  But here's where confusion comes in -- what are the endpoints?  Are they just you and your friends?  Or is the server an endpoint too? It depends on the application.  As an example, HTTPS (which secures communications between you and the servers hosting the webpages you visit) is encrypted so that only you and the server can decrypt the content of the webpages.  Signal, a secure instant messaging app tied to your smart phone, encrypts messages so that only you and your friend that you are messaging can read your messages.  In both cases, only the people or entities that you could imagine needing to know the information are able to decrypt encrypted information.  This is the heart of end-to-end encryption.  Please check out our post on Direct Encryption for more details on end-to-end encryption

Here are some pictures to illustrate why Direct Encryption is so important in private messaging. Marcos (left) is trying to get a message (Ursula K. Le Guin’s the Dispossessed) to Ernesto (right) using laptops and the Internet:

[//]: # (comment)

![MITM-attack-0](pictures/integrity-TMITM-illuminated6.png)
<img src="pictures/integrity-TMITM-illuminated6.png" width="800">

But the ghost of mean old J. Edgar Hoover haunts the infrastructure. The Man in the middle here is able to intercept, read, and change any unprotected message sent between our two heroes. Like so:

<img src="pictures/integrity-TMITM-illuminated8.png" width="800">

(Edgar could also just read and send the message along unaltered).  To make matters worse, saying that an app uses "encryption" (without being specific about who holds the keys) doesn't guarantee that messages remain private and authentic.  For example, if a server between the two comrades is managing the encryption keys, anyone with access to the server could read and modify all messages between them:

<img src="pictures/integrity-fingerprinting10.png" width="800">

How do you know whether an app uses Direct Encryption?  The best indication is that there is some way to verify encryption keys -- Signal makes this super easy with safety numbers and Wire uses more traditional fingerprints, one per device.  This can get cumbersome if your friends have lots of devices, but with Wire or PGP/GPG it's easy to post your fingerprints somewhere public -- like social media -- and ask friends to copy/paste/find to verify them.  It's also important that the app is open source, so that its security features are verifiable.

Another way to reduce exposure to a malicious interloper is through peer-to-peer messaging, where it is said that there is "no server" in between, managing your messages or contacts.  Even this can be a bit misleading, however: there is a ton of Internet infrastructure in between you and your friends, it's just invisible to most users and apps.  But this infrastructure is precisely what the State exploits to conduct suspicionless, mass surveillance.

Stay safe out there!

## Tiers of Encryption

Tier 1 (top shelf, best possible security) uses truly end-to-end, Direct Encryption.  Private conversations can only be eavesdropped on by breaking into one of the participants' devices.  Wire and Signal meet this standard, and are also open source, so their security claims can be thoroughly verified.  If Zoom does this for 1-on-1 calls, as they claim, they could switch it off anytime--it's a setting that zoom customers/administrators can change via the administrator panel at zoom.us -- so a zoom employee could do the same thing.  This is a pretty terrible implementation of end-to-end encryption, so we don't count it as Direct Encryption, where  *only* you and your friends control encryption keys.

Tier 2 (less than ideal but still hard for some adversaries to break) is the sort of "in transit" encryption Zoom uses for group calls where comms are encrypted from participants' devices to Zoom's server, mixed, encrypted again then sent out to all participants' devices.  Breaking this would likely require Zoom's active co-operation, most likely obtained via a warrant or National Security Letter.

Tier 3 (not at all good, open to multiple adversaries including private security) is plain old cell phone encryption -- governments can relatively easily ask cell phone companies for access to their networks (and to break encryption done by the cell phone company) -- worse yet, cell site simulators ("Stingrays") can force phone network security down from 4G to 3G, weakening encryption enough for anyone with access to a Stingray to break (local cops, very probably corporate security).



