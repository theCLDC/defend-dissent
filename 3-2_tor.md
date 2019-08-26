## Using Tor for social movement work

> You should be familiar with the technical concepts in [Anonymous Routing](anonymous-routing.md) and the [range of digital threats to social movements](threat-overview.md) as well as the [goals](goals.md) and [principles](trust.md) of social movement digital security.
> We also recommend that you read about [metadata](meta-data.md), [exchanging keys](key-exchange.md), and [end-to-end encryption](end-to-end-encryption.md) before reading this section.

#### What you'll learn

1. How to install and use Tor safely in most cases
1. Four distict ways to use Tor for social movement work
1. Some things you should never try to do using Tor

### Overview

Using Tor it is possible to conceal your identity online from [most adversaries](threat-overview.md) and even enjoy significant protection against a [nation-state level adversary](threat-state.md), with only a few known exceptions.  There are important warnings and caveats, however: **remember, unless you cannot avoid it, never entrust your life or freedom entirely to** ~~a complex machine you noone fully understands let alone can control~~ **a computer**.

### Warning: Situations in which Tor cannot protect you

If an adversary (Edgar) is able to watch Assata's connection to the Tor network as well her connection leaving the Tor network (to Bobby's website), Edgar will be able to determine that Assata is visiting Bobby's website.  This is called an [*end-to-end timing* or *correlation* attack].  Also, if you attempt to use applications not designed for Tor over the Tor network, they may leak identifying information.  [Go here for more details](https://www.torproject.org/about/overview.html.en#stayinganonymous).

### Getting Tor

Download Tor Browser from [the Tor Project website](https://www.torproject.org/).  For maximum safety, in particular if you consider yourself or your organization subject to targeted attack, [verify the PGP signature of the downloaded file](https://www.torproject.org/).  See [end-to-end encryption](end-to-end-encryption.md) and [GPG](GPG.md) for background.


### Different ways to use Tor

1. **Anonymous browsing** - Don't log in to any websites, ideally make a new identity to separate top secret research.

1. **Pseudonymous posting** - Create a pseudonym unrelated to your true identity in order to post press releases, or participate in forums and other online discussions.  Be sure to *never* log in using this pseudonym outside of Tor.  Also, greater caution is required the longer a pseudonmyous identity needs to be maintained.

1. **Hide your physical location** - Non-anonymous use of personal/organizational social media, to conceal physical location from the social media platform;

1. **Top secret chats** - people who know each other use the Tor network to chat using some Tor-compatible chat program like xmpp/pidgin/gajim, tor messenger, tox, riot.im.  Since this involves using apps other than the Tor browser, this use should be considered somewhat experimental.  

#### External resources

* [Tor Project Overview](https://www.torproject.org/about/overview.html.en)
