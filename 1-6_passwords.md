## Passwords

> We recommend that you read the Chapter on [Cryptographic Hash](1-4_cryptographic-hash.md) before reading this chapter.

#### What you'll learn

1. When password-protected means something is encrypted, and when it does not.
1. How passwords are defeated.
1. What password practices you can use to minimize the risk of your passwords.
1. How encryption keys can be generated from passwords.

---

### When password-protected does not mean encrypted

All passwords are used to control access. *Account passwords* are used
to grant access to an online account, for example. Rarely, though, is
the information in that account encrypted with a key that you control
and it is likely that your information is not encrypted at all.  That is, the information is usually readable by the provide (e.g. Google, Dropbox). Other
passwords are used to *unlock* an encrypted file or document, and we
will refer to these as *encryption passwords*.  Use of an account
password is like telling a bouncer your name and having that name be
matched on a list of approved guests, whereas use of an encryption
password is more like using a key to unlock a safe.  In the first
case, it is up to the bouncer (a metaphor for your online account
provider) to give you access. In the latter case, the safe represents
the ciphertext and the contents of the safe are the plaintext --
gaining access to the plain text is impossible (or at least,
impractical) without the key, or password.  (In fact, encryption keys are in some cases generated from the password, as we describe below.)

That said, even though your information is not encrypted with an account password, you should still minimize the people who could have access to your information.  But to understand why we recommend the password practices we do, it helps to understand how passwords can be compromised.

### Password cracking

Passwords can be compromised or *cracked* one at a time or as a whole batch, as in all the passwords for all the accounts on a given system. Passwords are hot commodities.  Since people frequently use the same password for many accounts and "popular" (a.k.a. terrible) passwords are used by many people (`123456`, `password`, `qwerty`, `admin`, `welcome`, `password`, to name a few real examples), discovering passwords used for one service can result in an account compromise for a different service, and possibly for a different person.

Let's consider the ways in which passwords are compromised.

To crack one password, an adversary could do so via the same means that you enter your password, for example via a website, over the internet.  This is relatively easy for the website operator to help protect against by, for example, locking an account after a few incorrect password entries or forcing delays after entering the password to slow down repeated guesses.  Another way the account provider can help is by allowing for 2-factor authentication. This is where, in addition to entering a password to access an account, you must also enter an authentication code that is delivered to you via text, an app on smartphone, or to a physical authentication key (such as a YubiKey). To compromise your account, an adversary would need your password as well as your device that receives the authentication code.

An adversary could also physically access the device (your phone or computer) on which you enter your password. More likely, and as is regularly reported in the news, the server on which your password is stored is compromised or hacked. In this case, if won't just be your username and password that is compromised, but everyone who has an account on that system. Although an adversary who has gained access to a database of passwords on the server will likely have access to your account information too, as we alluded to above, the point of the hack might not be to gain access to the hacked service, but another service entirely.

A responsible web service provider won't store your password in plaintext on their server, but will store a cryptographic hash of your password.  To uncover a password (or all passwords), an adversary computes the cryptographic hash of a guessed password and compares this to the database of stolen passwords.  In practice, password cracking tools (for example, John the Ripper) use three techniques:
1. Dictionary attacks: Trying dictionary words, common *salts* of dictionary words (e.g. `pa55w0rd`, `fr33d0m`), and previously cracked passwords.
1. Brute force: Trying all possible combinations of letters and numbers of symbols.  For practical reasons, this method only works for relatively short passwords.
1. Pre-computed hashes: Comparing against a table of cryptographic hashes of possible passwords that are computed ahead of time.

A user can foil the first two techniques by using good password practices (described below).  A service provider can make password cracking less practical by using a cryptographic hash function that is slow to compute or uses a lot of memory. This wouldn't be noticeable for a single password (such as would be done when you log in), but would slow the computation of the hashes during cracking.

A service provider can further foil the use of pre-computed hashes if they add a long random sequence of characters (*salt*) to your password when you log in.  This salt can be stored in plaintext with your username, so an adversary would have this information too, but would not have had the salt when the pre-computed table of hashes was prepared. Additionally, if two users have the same password, because their salt will be different, the cryptographic hash of their passwords with the corresponding salts will be different.  This forces an attacker to uncover each password individually.

For all of this, you are trusting the online service provider to responsibly store and protect your user information, including your hashed password, if they have even hashed it.  The rest is up to you.

### Best practices for passwords

To guard against the methods deployed in password cracking, your passwords should:
* be sufficiently long (to prevent against brute force attacks),
* be uncommon (to prevent against dictionary attacks),
* not be reused (so if one of your accounts gets compromised, all of your accounts aren't compromised).

To accomplish this, use a password manager to generate and store all of your passwords that you don't need to manually type in.  The password manager should be able to generate strong random passwords for you such as `bdY,Fsc_7\&*Q+cFP`.  This is great for a password that you never have to type in, that is, a password that the password manager will input for you.

For passwords that you will necessarily need to type in (for example: a password you enter on your phone, the password you protect your password manager with, the password you use to encrypt or unlock your computer) use a diceware password a.k.a. a passphrase a.k.a. a random sequence of words such as `remake.catfight.dwelled.lantern.unmasking.postnasal`.  You can generate this password manually using dice and a word list.  Many password managers will also generate such passwords, although you probably won't need many of these.

Note that the two above examples of passwords are randomly generated.  This is important, because even if you think your password is awesome and strong, if you came up with it with your brain, then someone else's brain probably also came up with it, and so it is susceptible to dictionary attacks.

![XKCD Password Strength, CC BY-NC 2.5 https://www.xkcd.com/936/](https://imgs.xkcd.com/comics/password_strength.png "XKCD Password Strength, CC BY-NC 2.5 https://www.xkcd.com/936/")

### Generating encryption keys from passwords

In some cases, passwords *are* used to unlock an encrypted file or device.  An encryption key in this case is in fact generated from a password or passphrase using a key derivation function, which is, essentially, a cryptographic hash function.  The input to the cryptographic hash function is your password and the output is the cryptographic key.
Why would this work?  Let's revisit the properties of cryptographic hash functions:
1. Regardless of the length of the input, the output is always the same size.  So, no matter how short (and weak!) your password is, you will get a cryptographic key of the right size.  (But a short and so weak password is susceptible to the password cracking methods we discuss above.)
1. *The same input always results in the same output.*  So, your password will always generate the corresponding cryptographic key you need.
1. *It is infeasible to generate the input from the output.*  So, if someone manages to get your key, at least they won't be able to recreate your password.
1. *It is infeasible to find two different inputs that result in the same output.*  So, someone trying to crack your password would be unlikely to even find some other password that results in the same cryptographic key as yours.
1. *A small change to the input changes the output so extensively that the new hash value appears uncorrelated with the old hash value.*  Well, this property isn't as useful for cryptographic key generation ...

### In context: when precautions are not enough

In 2016, long-time activist DeRay McKesson had his Twitter account and
two email addresses compromised in a targeted attack *despite* having
2-factor authentication set up.  His adversary was able to get control
of his phone by calling Verizon and requesting a new SIM card, and
knew enough about McKesson to convince Verizon to do so.  Once the
adversary had access to McKesson's phone number, they were able to
receive password reset codes to change his passwords and gain access
to his accounts.  It is a reminder that no security measure will be
perfect and for those that are subject to targeted attacks (in this
case, McKesson was targeted for his support of Black Lives Matter),
extra vigilance is necessary.  Here, the fact that access to
McKesson's phone number could be used to force a password reset
reduced account protections from 2-factor to 1-factor: only phone
access separated an adversary from McKesson's account, rather than a
password plus phone access.

#### What to learn next

* [Protecting your Devices](3-2_devices.md)

#### External resources

* [Top 50 Worst Passwords of 2019](https://www.teampassword.com/blog/top-50-worst-passwords-of-2019), TeamPassword. December 2019.
* [John the Ripper](https://en.wikipedia.org/wiki/John_the_Ripper), Wikipedia.
* [@Deray's Twitter Hack Reminds Us Even Two-Factor Isn't Enough](https://www.wired.com/2016/06/deray-twitter-hack-2-factor-isnt-enough/), Wired Magazine. June 2016.
