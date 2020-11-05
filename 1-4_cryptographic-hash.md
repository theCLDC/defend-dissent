## Cryptographic Hash

> We recommend that you read the Chapter on [Modern Cryptography](1-2_modern-cryptography.md) before reading this chapter.

#### What you'll learn

1. What a hash function does.
1. What a cryptographic hash function does and how it is distinct from an ordinary hash function.
1. Some examples of the use of cryptographic hash functions.

---

A *hash function* is any (computer) function that transforms data of arbitrary size (e.g. a name, a document, a computer program) into data of fixed size (e.g. a 3 digit number, a 16 bit number).  The output of a hash function is called the digest, fingerprint, hash value or hash (of the input *message*).

A *cryptographic hash* function has the following properties that make it useful for cryptographic applications.
1. The same message always results in the same output hash.
1. It is infeasible to generate the input message from its output hash value except by brute force (trying all possible input messages).
1. It is infeasible to find two different input messages that result in the same output hash value.
1. A small change to the input message changes the output hash value so extensively that the new hash value appears uncorrelated with the old hash value.

The first two of these properties are similar to properties of most encryption protocols.  If you encrypt the same message on two different occasions, you would expect the same result, assuming you are using the same encryption key.  Given only the ciphertext, it should be infeasible to generate the plaintext (without the decryption key).  However, encryption allows you to go backwards, from ciphertext to plaintext, using the decryption key.  Hash functions are inherently one-way: there is no key to go backwards.  That the result is sometimes called a digest or a fingerprint is a useful analogy: while the output of a cryptographic hash function does not encode all of the information of the input message (in the way that a ciphertext does), it encodes enough information that you can use it to identify the input (relying on Properties 1 and 3) and that this is very difficult to fake (Property 2).

We will see applications of cryptographic hash functions in the Chapters on [Passwords](1-6_passwords.md), [The Man in the Middle](1-5_man-in-the-middle.md) and [Public Key Cryptography](1-7_public-key-cryptography.md), but let's look at a simple use here, known as a *commitment scheme*.

### Using cryptographic hash functions to prove how smart you are

Assata and Bobby are both trying to solve a difficult math problem.  Assata gets the answer (S) first, and wants to prove to Bobby that she has the answer before he has solved it without leaking the solution to him.  So, Assata takes a cryptographic hash of the solution S, hash(S), and gives Bobby hash(S).  Since the hash is cryptographic, Bobby can't learn S from hash(S) (property 2).  When Bobby eventually solves the problem, finding S for himself, he can compute hash(S) and check that the result is the same as what Assata gave him.  By properties 1 and 3, Bobby knows that Assata's input to the hash function must be the same as his input to the hash function, thus proving that Assata solved the problem first.  (Property 4 was not used here, but without this property, if Assata got a solution that was close to correct, but not quite, the two has outputs might be very similar, and a cursory comparison may not uncover that they are different.)

### What do hash functions look like?

There are many different cryptographic hash functions in use today, but describing them in detail is beyond the scope of this book.  However, to give you a sense of what they might look like, we give an example that satisfies some, but not all, of the properties that cryptographic hash functions have.

The example hash function is called `chunked XOR`.  Exclusive or, a.k.a. `XOR`, is a function that, when given a pair of inputs, outputs true (or 1) if the inputs are different and false otherwise.  So, for example: `apple XOR banana = 1`, `apple XOR apple = 0`, `0 XOR 1 = 1`, `1 XOR 1 = 0`.  We can take a chain of `XOR`s on binary numbers (0s and 1s) and get a meaningful answer: `1 XOR 1 XOR 0 = 0`, `1 XOR 1 XOR 0 XOR 1 = 1`.  For a sequence of binary numbers, `XOR` returns 1 if there are an odd number of 1s in the chain, and 0 otherwise.

`Chunked XOR` operates on a binary input.  (If your input is not binary, you could represent it in binary first, the same way a computer would.)  We group the input into chunks equal to the size of the output of the hash function, for example groups of 8 bits.  We line the chunks up vertically, and then `XOR` the contents of each column, as illustrated below.

```
        input: 00111011 11101101 00101000 00101011 01011000 11001110

      chunked: 00111011
               11101101 
               00101000 
               00101011 
               01011000 
               11001110 

XOR'd columns: 01010011 (output)
```

This is a hash function in that, no matter what the length of the input, the output will always have the same length (8 in this example).  You should be able to see that `chunked XOR` satisfies the first property of cryptographic hash functions.  However, it fails on the remaining properties.  It is easy to create *an* input message (but not necessarily your desired input message) with a given output hash: for example, you could concatenate 11111111 11111111 onto the result of the hash.  For the same reason, you could create multiple messages having the same output hash.  Finally, changing a single bit of the input message will change only a single bit of the output hash.

### In context: Cryptographic hashes violate your 4th amendment rights

In 2008, a US District Judge ruled that if the US government wants to cryptographically hash your private data, then they need a warrant first.  The case in question had a special agent of the Pennsylvania Attorney General's Office copy the hard drive of a suspects computer.  The special agent computed a cryptographic hash of the copy (so that it could be later compared to the original to prove that they did not tamper with it, relying on Properties 1 and 3).  The agent then used a forensic tool which:
* Computed a cryptographic hash of each individual file (including deleted, but not yet overwritten files) on the copied hard drive.
* Compared these hashes to hashes of files in a database of contraband files.
The agent found three matches between hashes of files on the hard drive and hashes of contraband files.  By Properties 1 and 3, this means that the hard drive contains at least 3 illegal files.  The judge on the case determined this practice (of hashing the files and comparing them to known hashes) to constitute a *search* of the hard drive, violating the accused's 4th amendment rights to protection from illegal searches and seizures. As a result, the evidence could not be used in trial.

We should disclose the particulars of the case, which involves possession of child pornography.  While we would never defend the right of possession (or creation or distribution) of child pornography, it is important to imagine a power (in this case that of determining the existence of particular files on a computer) to be used in a way that you would *not* want it to be used.  Music that a friend shared with you?  Images of oil spills?  Images of #blacklivesmatter protests?  Earth First! Journal articles?

#### What to learn next

* [Passwords](1-6_passwords.md)
* [The Man in the Middle](1-5_man-in-the-middle.md)
* [Authenticity through Crytographic Signing](1-8_authenticity.md)

#### External resources

* [UNITED STATES of America v. Robert Ellsworth CRIST, III, Defendant. Criminal Action No. 1:07-cr-211.](https://www.leagle.com/decision/infdco20081023b74)




