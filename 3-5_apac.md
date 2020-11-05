## Protecting your Identity

> We recommend that you the Chapters on [Anonymous Routing](1-10_anonymous-routing.md) and [Public Key Cryptography](1-7_public-key-cryptography.md) before reading this chapter.
	
#### What you'll learn

1. The difference between being anonymous and pseudonymous.
1. Three distinct ways to use Tor.
1. Some things you should never try to do using Tor.

---

In the Chapter on [Anonymous Routing](1-10_anonymous-routing.md), we compared and contrasted Virtual Private Networks (VPNs) and Tor as two methods for disguising one's metadata online.  This can help one achieve anonymity or pseudonymity, but this is difficult to do over the long term.  In this chapter, we will focus on skills for using Tor over VPN, but these lessons apply to using a VPN.  One needs to additionally remember though, that when using a VPN, the VPN provider knows who you are and the metadata of your internet communications (and the content, if it isn't encrypted).  While we will focus on using Tor via the Tor Browser, know that there are other applications (such as secure messaging applications or whole operating systems) that route internet requests through the Tor network.

### Anonymity versus pseudonymity

Before we describe different ways to use Tor, let's us consider the difference between anonymity and pseudonymity.  These terms are used in different ways in different contexts, and we restrict our use here to online communications and behavior.

**Anonymity** refers to being without name, or more generally without any identifier that could link to you.  If you visit a website anonymously today and the same website anonymously tomorrow, the website should not even be able to tell that it was the same person both times.  All the website should know is that "someone visited me anonymously yesterday" and "someone visited me anonymously today."

**Pseudonymity** refers to using a false name, with few or no people knowing your true identity.  For example, Samuel Clemens published under the pseudonym "Mark Twain", but of course his publisher and others knew who the true author was.  Edward Snowden used the pseudonym Cincinnatus in contacting journalist Glenn Greenwald.  Greenwald did not know who was contacting him as Cincinnatus, and because Snowden was using Tor to contact Greenwald, neither did anyone else.  However, Snowden's repeated use of Cincinnatus allowed Greenwald to connect different communications he (and fellow journalist Laura Poitras) received from Snowden.  We will refer to psuedonymity as allowing one to link different and otherwise anonymous sessions of communications under one persona.
	
### Ways to use Tor

Tor can be used to hide information about your identity (such as your physical location) and achieve anonymity and pseudonymity.  For the novice user, Tor is accessed using the Tor Browser or Tor-compatible apps.  For a more advanced user, non-web browser communications can be routed through Tor by using an operating system (such as Tails or Whonix) that routes all your webtraffic through Tor.

#### Hiding your physical location

Using the Tor Browser as you do any other browser, including accessing accounts that are linked to you such as email or social media accounts, will conceal your physical location from those accounts.  Each time you open a new Tor browser tab or window and after a certain delay, Tor will route your web requests via a new location.  However, many email and social media platforms will flag your account activity as suspicious if it is being accessed from different locations as it will appear to be when accessing through Tor.  So while it is possible to use Tor all the time and for everything, it may not be practical.  If you are able to navigate these difficulties, you will still need to be smart to consistently hide your physical location by **avoiding** the following behaviors:
* Entering identifying information into a website (such as your address).
* Downloading a document that might access some part of the document via the web (like a photo) and opening it outside the Tor Browser.  Word documents and pdfs can do this.  If you need to access such a document, disconnect from the internet before opening.

#### Achieving anonymity

Using Tor can help you achieve anonymity.  However, you will need to restrict your behavior to ensure your don't leak information that could break your anonymity.  To that end, in order to maintain anonymity, you need to **avoid** the following behaviors during your **anonymous session** (in addition to those for hiding your physical location):
* Logging into accounts (e.g. social media, email, banking).
* Visiting your own website repeatedly.
	
#### Achieving and maintaining pseudonymity

If you create a pseudonym that is unrelated to your true identity, for example, in order to post press releases or participate in forums, Tor can help ensure that your pseudonym stays unrelated to your true identity.  However, to keep your real and pseudonymous identity separate you need to **avoid** the following behaviors:
* Accessing different pseudonymous (or your pseudonymous and real) identities in the same session as this can link these identities.
* Accessing a pseudonymous account even once outside of Tor.
* Using two-factor authentication with a phone (as your phone, even it is a "burner", can reveal your physical location).
* Posting media with revealing metadata (such as location).	

Note that the longer you attempt to maintain a pseudonymous identity, the more opportunity you give yourself to make a mistake.  In addition to the mistakes above, your writing style can be used to identify you using stylometry.  The more examples of your writing style that are available (under both your real and pseudonymous identity) the easier it would be to identify you.

### Tor warnings

There are some additional things to be aware of when accessing the internet via Tor.

As with any protective technology, nothing is perfect.
If an adversary (Edgar) is able to watch Assata's connection to the Tor network as well her connection leaving the Tor network (to Bobby's website), Edgar will be able to determine that Assata is visiting Bobby's website.  This is called an *end-to-end timing attack* or *correlation attack*.

If you attempt to use applications not designed for Tor over the Tor network, they may leak identifying information, such as screen resolution or a unique set of settings you may have.

Finally, when using Tor, keep in mind it only provides anonymity — for privacy, you need to be accessing webpages using end-to-end encryption via HTTPS (though unfortunately not all websites support this).

### In context: Getting the real Tor Browser

The tools you use to protect yourself online are only useful if they are the real thing.  In 2019, it was discovered that a false version of the Tor browser was being promoted by people interested in (and successfully) stealing BitCoin.  They made the malicious Tor Browser available through incorrect domains like tor-browser[.]org and torproect[.]org (instead of the authentic domain, torproject.org.  To protect yourself from such mistakes as downloading from the wrong site or to protect yourself from a man-in-the-middle attack which supplies you with a malicious app, apps such as the Tor Browser make it possible for you to check the signature of a download, as we discuss in the Chapter on [Public Key Cryptography](1-7_public-key-cryptography.md).

#### What to learn next

* Any remaining chapter in [Part III](index.md).

#### External resources

1. [Tor Project Overview](https://www.torproject.org/about/overview.html.en)
1. [Tails](https://tails.boum.org/)
1. [Whonix](https://www.whonix.org/)
2. [Whonix' Tips on Remaining Anonymous](https://www.whonix.org/wiki/DoNot)
3. [Phony HTTPS Everywhere Extension Used in Fake Tor Browser](https://www.eff.org/deeplinks/2019/10/phony-https-everywhere-extension-used-fake-tor-browser)

