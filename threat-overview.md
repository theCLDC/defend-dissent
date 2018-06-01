## Overview of digital threats

> Before reading this section, it's a good idea to read the sections on [goals](goals.md) and fundamental concepts

#### What you'll learn

1. how to assess risk of various threats social movements face - how likely, how damaging, how willing to change
1. how to categorize digital threats - by type, technique, adversary
1. some specific examples of attacks

### Types of threats & threat modelling

Social movements challenging powerful individuals, organizations, and social structures face a broad range of digital threats.  Specific threats vary widely in technical sophistication, likelihood, and potential for harm.  *Threat modeling* is a process whereby an organization or individual considers their range of adversaries, estimates the likelihood of their various data and devices falling victim to attack, and finally considers the damage done if attacks were to succeed.  There are a number of ways to categorize possible attacks: by **adversary** (e.g. your unfriendly neighborhood neonazi, a corporate security firm, or government-sponsored hackers), by **site** of attack (a coffee shop wifi network, someone breaking into your office, or siphoning all traffic from the internet backbone) or **technique** (man-in-the-middle, brute force password cracking, tricking you or looking over your shoulder).  Given a [list of NSA programs](https://snowdenarchive.cjfe.org) it makes most sense to categorize attacks by both **site** and **technique**, for example:

#### Threats according to attack type (site or technique): 

> Sorted roughly by most to least likely, and lowest to highest risk of attack discovery

1. Passive network attacks
    * mass collection of data in transit (Stormbrew)
    * includes unencrypted content, and metadata outside of private networks

1. Searches of unencrypted stored data 
    * by legal authorities (subpeonas, search warrants) 
    * extra-legal authorities (PRISM, section 702)

1. Passive data collection
    * smartphone sensors
    * web browser profiling

1. Active network attacks 
    * botnets
    * MITM

1. Attacks on encrypted stored data
    * brute force password attacks
    * password sniffing methods

1. Active attacks on user devices
    * malware
    * physical attacks

However, from the perspective of a social movement group conducting threat modeling, it makes more sense to categorize threats by **adversary**.  This is the approach we take in this text, and there are three main reasons for this.  First, the range of techniques and attack sites available to a given adversary depends on the degree of technical sophistication, resources, and legal authorities available to that particular adversary.  Therefore it's possible to create a heirarchy of adversary classes, where the methods of attack generally available to higher-grade adversaries are typically inaccessible to lower-grade adversaries.  At the same time, methods available to lower-grade adversaries are generally available to higher-grade adversaries.

Second, depending on the kinds of work done (e.g. topics and tactics) by particular social movements, two different social movement groups are likely to face varying degrees of threat from different grades of adversary.  In an actual threat-modeling discussion within an organization or social movement, *who* potential adversaries are is often more readily apparent than *how* or *where* such adversaries would carry out attacks.

Third, the countermeasures required to protect against certain higher-grade adversary attacks tend to be more sophisticated (requiring greater training or resources).  Likewise, higher-grade attacks can be defended against with less certainty.

#### Adversaries - from lowest to highest grade capabilities

Note that most techniques available to lower grade adversaries are also available to higher-grade adversaries.  Also, it is import  ant to note that these categories are not absolute, for example police departments in large cities may have access to nation-state level resources, or a particularly skilled Neighborhood Nazi may possess advanced hacking skills that enable some corporate- or nation-state-level attacks.

1. **Yourself, Oversharing**
    * public social media
    * data voluntarily shared with companies (machine learning, surveillance mining)


1. **Neighborhood Nazis**
    * phishing / social engineering / social media hijacking
    * doxxing
    * shoulder surfing passwords / info
    * device theft
    * possibly attacks on outdated devices

1. **Bosses/Local Sysadmins**
    * work or school email and file storage
    * web browsing history and unencrypted content
    * password capture
    * local network censorship

1. **Private Industry**
    * commercial malware - phone hacking
    * cell site simulators/IMSI catchers
    * possible mobile phone communications (SS7)
    * legal requests (subpeona) to commercial platforms (email, cloud storage)
    * covert physical attacks (a/v bugs, keystroke loggers)
    * social media monitoring
    * Fusion Center data

1. **Local Law Enforcement**
    * legal requests (subpeonas, search warrants)
    * device confiscation

1. **Nation-States**
    * mass surveillance (passive global surveillance of Internet and cell networks)
    * storage, search, and anaylsis (XKEYSCORE, machine learning)
    * web redirection via packet injection (QUANTUM)
    * national-security requests (section 702)
    * access to internal corporate networks (PRISM)
    * custom malware, botnets
    * network attacks using zero-day vulnerabilities
    * sophisticated physical attacks (TAO), including supply chain attacks
    * advanced persistent threats against infrastructure (web servers)
    * country-wide censorship

In the sections corresponding to each grade of adversary, we will highlight important examples of attacks against social movements, whenever possible.

#### What to learn next

Detailed discussions on each grade of adversary and suggested countermeasures.  Alternatively, skip to the most relevant to the social movement group of interest.

* [Yourself, Oversharing](threat-you.md)
* [Neighborhood Nazis](threat-neigh.md)
* [Bosses/Local Sysadmins](threat-bosses.md)
* [Private Industry](threat-industry.md)
* [Local Law Enforcement](threat-cops.md)
* [Nation-States](threat-state.md)


#### External resources

##### Threat modeling
* NYCATC threat matrix
* [EFF threat modeling](https://ssd.eff.org/en/module/assessing-your-risks)

##### Adversary capabilities
* [NSA programs at Snowden Archive](https://snowdenarchive.cjfe.org)
