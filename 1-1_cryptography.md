## What is encryption?

Encryption is the process of scrambling a message so that it can only be unscrambled (and read) by the intended parties. The method by which you scramble the original message, or _plaintext_, is called the _cipher_ or encryption _protocol_. 

### A simple cipher: The Caesar cipher

Consider perhaps the simplest cipher, called the _Caesar cipher_ wherein each letter in the message is shifted by an agreed-upon amount in the alphabet. For example, suppose you wanted to encrypt the plaintext

```
IF VOTING CHANGED ANYTHING IT WOULD BE ILLEGAL
```

by shifting each letter in the alphabet forward by three places, so that `A` becomes `D`, `B` becomes `E` and so on, with `Z` wrapping back through the start of the alphabet to become `C`. Then the plaintext gets encrypted to the following _ciphertext_:

```
LI YRWLPK FKDQKHG DQBWKLPK LW ZRXOG EH LOOHKDO
```

To decrypt this message, the recipient would do the reverse, shifting each letter in the alphabet backward three places, so `Z` become `W` and `A` wraps around through the end of the alphabet to become `X`. For the recipient to be able to decrypt the message (quickly), they would have to know the _key_ to the cipher.  For the Caesar cipher, this is the number of places that each letter is shifted in the alphabet; in this example, it is the number `3`.

Of course, the Caesar cipher is not a very strong cipher, and you certainly shouldn't trust it to keep your secret plans secret. All an adversary would have to do to _break_ your code is try every possible shift through the alphabet (and there are only 25 of those).  This _attack_ is called a _brute force_ attack: the adversary tries to break your code by trying every possible key.  This attack is feasible because there are not that many possible keys.

### A slightly more complicated cipher: The Vigen&egrave;re cipher

The Vigen&egrave;re cipher is a set of Caesar ciphers, each with their own key.  Typically the key is a word where the place of the letters of the word in the alphabet tells you how the letter `A` is mapped for the Caesar cipher. This is easiest to see with an example.  Suppose you wish to encrypt the plaintext

```RESPECT EXISTENCE OR EXPECT RESISTENCE```

with the key

```ACT```

Then:

* Encrypt every third letter starting with the first letter of the plaintext with a Caesar cipher that maps `A` to `A` (a shift of zero, or a Caesar cipher using the key `0`).
* Encrypt every third letter starting with the second letter of the plaintext with a Caesar cipher that maps `A` to `C` (a Caesar cipher using the key `2`).
* Encrypt every third letter starting with the third letter of the plaintext with a Caesar cipher that maps `A` to `T` (a Caesar cipher using the key `19`).

Alternating between these three Caesar ciphers results in the cipher text

```RGLPGVT GQIUMEPVE QK EZIEEM RGLIUMAPVE```

To break this cipher, if your adversary knows the length of your key, then your adversary could try decrypting the ciphertext with all possible words (or, more generally, combinations of letters) of that length.  In this example, that would take at most `26 x 26 x 26 = 17576` attempts, which is more than you would attempt by hand, but easily done by a computer.  If your adversary doesn't know the length of your key, then they would have to try many more possible keys to try and brute force break the code.  Notice that your adversary has to work harder to break your code the longer your key is.

### In context: The unbreakable one-time pad

A Vigen&egrave;re cipher whose key is a sequence of randomly selected letters and that is as long as the plain-text is a cipher known as the _one-time pad_.  (Historically, the key itself would be written in a pad of paper that is only used once.)  It is impossible to break this cipher without having the key--that is, it is impossible to guess the key, even with unlimited time and resources because any plaintext (of the right length) could result in the given ciphertext with the right key.

Of course, the one-time pad has the practical problem of how one how to exchange the key, which is as long as the message.  Despite that, it has been used historically, allowing for groups to share a one-time pad in person and then send messages over insecure channels when they are apart.  In the late 80s, the African National Congress, who, at the time, was fighting South African apartheid, used one-time pads to encrypt messages between foreign support and in-country operatives.  The one-time pads were physically transported by a trusted air stewardess who worked the Amsterdam-to-Johannesburg route.  They had also computerized the encryption and decryption and translated encrypted messages into tonal sequences that were played over a phone connection and recorded to or received from an answering machine, allowing for asynchronous communication.

#### What to learn next

* [Modern Cryptography](1-2_modern-cryptography.md)
* [Key Exchange: How to agree on a cryptographic key over the Internet](1-3_key-exchange.md)

#### External resources

[Talking To Vula: The Story of the Secret Underground Communications Network of Operation Vula](http://www.anc.org.za/content/talking-vula)