## Using Tor for social movement work

> You should be familiar with the technical concepts in [Anonymous Routing](anonymous-routing.md) and the [range of digital threats to social movements](threat-overview.md) as well as the [goals](goals.md) and [principles](trust.md) of social movement digital security.
> We also recommend that you read about [metadata](meta-data.md), [exchanging keys](key-exchange.md), and [end-to-end encryption](end-to-end-encryption.md) before reading this section.

#### What you'll learn

1. How to install and use Tor safely in most cases
1. Four distict ways to use Tor for social movement work
1. Some things you should never try to do using Tor

### Overview

Using Tor it is possible to conceal your identity online from [most adversaries](threat-overview.md) and even enjoy significant protection against a [nation-state level adversary](threat-state.md), with only a few known exceptions.  There are important warnings and caveats, however: **remember, unless you cannot avoid it, never entrust your life or freedom entirely to** ~~a complex machine you cannot fully control~~ **a computer**.

### Warning: Situations in which Tor cannot protect you

If an adversary (Edgar) is able to watch Assata's connection to the Tor network as well her connection leaving the Tor network (to Bobby's website), Edgar will be able to determine that Assata is visiting Bobby's website.  This is called an [*end-to-end timing* or *correlation* attack].  Also, if you attempt to use applications not designed for Tor over the Tor network, they may leak identifying information.  [Go here for more details](https://www.torproject.org/about/overview.html.en#stayinganonymous).

### Getting Tor

Download Tor Browser from [the Tor Project website](https://www.torproject.org/).  For maximum safety, in particular if you consider yourself or your organization subject to targeted attack, [verify the PGP signature of the downloaded file](https://www.torproject.org/).  See [end-to-end encryption](end-to-end-encryption.md) and [GPG](GPG.md) for background.


### Different ways to use Tor

1. **Anonymous browsing** - Don't log in to any websites, ideally make a new identity to separate top secret research.

1. **Pseudonymous posting** - Create a pseudonym unrelated to your true identity in order to post press releases, or participate in forums and other online discussions.  Be sure to *never* log in using this pseudonym outside of Tor.  Also, greater caution is required the longer a pseudonmyous identity needs to be maintained.

1. **Hide your physical location** - Non-anonymous use of personal/organizational social media, to conceal physical location from the social media platform;

1. **Top secret chats** - people who know each other use the Tor network to chat using some Tor-compatible chat program like xmpp/pidgin/gajim, tor messenger, tox, riot.im.  Since this involves using apps other than the Tor browser, this use should be considered somewhat experimental.  

### Tor best practices

The relative importance of a given warning or recommendation here depends largely on the adversary you are most trying to protect yourself from.

### passive, mass surveillance

-   need to use protocol-specific apps/support software to avoid leaking
    identifying information e.g. Tor Browser, Torbirdy+Thunderbird,
    Whonix for desktop-wide Tor connectivity anything potentially
    identifying/deanonymizing  screen resolution, etc.

-   accessing social networking sites or other online services with your
    own login, your name or other revealing information in web forms
    will deanonymize you may be useful to conceal your geographical
    location and avoid being tracked

-   it is still as (or more) important to use end-to-end encryption: Tor
    exit relays do not encrypt connections to destination servers;
    moreover, a malicious exit node could capture all cleartext (esp if
    sending email over the Tor network) a Tor exit node may be used to
    conduct a MitM

-     Don't open documents downloaded through Tor while online these documents can contain Internet resources that will be downloaded outside of Tor by the application that opens them. This will reveal your non-Tor IP address.1
-                Don't torrent over Tor - Torrent file-sharing applications have been observed to ignore proxy settings and make direct connections even when they are told to use Tor.1
-                Use HTTPS versions of websites1 The encryption of your traffic to the final destination website depends upon on that website. Tor Browser includes HTTPS Everywhere to force the use of HTTPS encryption with websites that support it. You should still watch the browser URL bar to ensure that websites you provide sensitive information to include https:// in the URL.1
-                Don't use Windows. Vulnerabilities in the software Tor Browser Bundle on Windows figure prominently in both the NSA slides and FBI's recent takedown of Freedom Hosting. Run Linux and carefully configure the latest available versions of Tor, a proxy such as Privoxy, and the Tor Browser, with all outgoing clearnet access firewalled, or consider using Tails or Whonix instead, where most of this work is done for you. 
-                Disable JavaScript, Flash and Java by default. The FBI has used tools which exploit all three in order to identify Tor users. If a site requires any of these, visit somewhere else.2
-                Drop cookies and local data that sites send you. Consider using an addon such as Self-Destructing Cookies to keep your cookies to a minimum.2
-                Don't use Google to search the Internet. A good alternative is Startpage; the default search engine for TBB, Tails and Whonix. Another good option is DuckDuckGo.2
-                Keep your computer up to date to ensure you are protected from the latest security vulnerabilities. 

#### non-technical steps  another list by the whonix folks <https://www.whonix.org/wiki/DoNot> 

**NEVER (i.e. Thou Shalt Not): **

-   Visit your Own Website when Anonymous

-   Login to Social Networks Accounts and Think you are Anonymous

-   Login to Accounts Used without Tor (even once!)

-   Login to Banking or Online Payment Accounts

-   Switch Between Tor and Open Wi-Fi

-   Use Tor over Tor Scenarios

-   Send Sensitive Data without End-to-end Encryption

-   Disclose Identifying Data Online

-   Use un-Bridged Tor if Tor Use is Dangerous or Suspicious in your
    Location but bridges aren’t perfect:
    <https://www.whonix.org/wiki/Bridges>

-   Maintain Long-term Identities

-   Use Different Online Identities at the Same Time

-   Login to Twitter, Facebook, Google etc. Longer than Necessary

-   Mix Anonymity Modes: Mode 1: Anonymous User; Any Recipient Mode 2:
    User Knows Recipient; Both Use Tor Mode 3: User Non-anonymous and
    Using Tor; Any Recipient Mode 4: User Non-anonymous; Any Recipient

-   Change Settings if the Consequences are Unknown

-   Use Clearnet and Tor at the Same Time

-   Connect to a Server Anonymously and Non-anonymously at the Same Time

-   Confuse Anonymity with Pseudonymity

-   Spread your Own Link First

-   Open Random Files or Links

-   Use (Mobile) Phone Verification

#### Other Tor warnings & limitations

-   source: <https://www.whonix.org/wiki/Warning>

-   never safe to use bittorrent oer TOR

-   source:
    <https://www.torproject.org/about/overview.html.en#stayinganonymous>

-   Tor does not provide protection against end-to-end timing attacks:
    If your attacker can watch the traffic coming out of your computer,
    and also the traffic arriving at your chosen destination, he can use
    statistical analysis to discover that they are part of the
    same circuit.

-   Beware opening PDFs and other scriptable documents (.doc,
    .xls, etc.) which can open URLs outside of the Tor network.

-   Document metadata, photo/video/audio metadata

-   also: <https://www.torproject.org/docs/hidden-services.html.en>

-   it is obvious that you are using Tor  unless special precautions
    (available in Whonix... other distros?) are taken (e.g. Tunnel
    Proxy/SSH/VPN through Tor)

-   your writing style can be used to identify you (“stylometry”; 1000
    words or less?)

#### application of Tor to anonymous chatting

- coming soon!

#### Tor Hidden Services

-   <https://www.torproject.org/docs/hidden-services.html.en>

-   bitmessage


### TAILS

- coming soon! 

#### External resources

* [Tor Project Overview](https://www.torproject.org/about/overview.html.en)
