## Overview of digital threats

> Before reading this section, it's a good idea to read the sections on [goals](goals.md) and fundamental concepts

#### What you'll learn

1. how to assess risk of various threats social movements face - how likely, how damaging, how feasible are defensive or mitigation steps
1. how to categorize digital threats - by type, technique, adversary
1. some specific examples of attacks

### Types of threats & threat modelling

Social movements challenging powerful individuals, organizations, and social structures face a broad range of digital threats.  Specific threats vary widely in technical sophistication, likelihood, and potential for harm.  *Threat modeling* is a process whereby an organization or individual considers their range of adversaries, estimates the likelihood of their various data and devices falling victim to attack, and finally considers the damage done if attacks were to succeed.  There are a number of ways to categorize possible attacks: by **adversary** (e.g. your unfriendly neighborhood neonazi, a corporate security firm, or government-sponsored hackers), by **site** of attack (a coffee shop wifi network, someone breaking into your office, or siphoning all traffic from the internet backbone) or **technique** (man-in-the-middle, brute force password cracking, tricking you or looking over your shoulder).  Given a [list of NSA programs](https://snowdenarchive.cjfe.org) it makes most sense to consider attacks by both **site** and **technique**, for example:

#### Threats according to attack type (site or technique): 

When possible, the following attack types are sorted roughly by most to least likely, and lowest to greatest cost (including least to greatest risk that an attack would be discovered).

1. Passive remote (network) attacks
    * mass collection of data in transit (Upstream: e.g. Stormbrew, Tempest)
    * includes all unencrypted content, and metadata outside of private networks
* web browser profiling, tracking cookies
1. Searches of unencrypted stored data 
    * by legal authorities (subpeonas, search warrants) 
    * theft (illegal)
    * extraordinary (national security) authorities (PRISM, section 702)
      * parallel construction to produce a path to constitutionally-gathered evidence
1. Active network attacks
    - botnet / implants (QUANTUM suite of programs, controlled using [TURBINE](https://theintercept.com/2014/03/12/nsa-plans-infect-millions-computers-malware/))
    - man-in-the-middle attacks [SECONDDATE](https://theintercept.com/2014/03/12/nsa-plans-infect-millions-computers-malware/)
    - brute force password attacks
    - password sniffing methods
1. Active attacks on user devices
    - malware
    - hotmicing, remote hijacking (pegasus, NSO group malware)
    - physical modifications, including interdiction and supply chain attacks (TAO program) 

For social movement groups conducting threat modeling, it is important to also evaluate threats according to **adversary**.  This is the approach we take in this text, and there are three main reasons for this.  First, the range of techniques and attack sites available to a given adversary depends on the degree of technical sophistication, resources, and legal authorities available to that particular adversary.  Therefore it's possible to create a heirarchy of adversaries, where many surveillance methods used by higher-level adversaries are inaccessible to lower-tier adversaries.  At the same time, methods available to lower-grade adversaries are often widely available to higher-grade adversaries.

Second, depending on the kinds of work done (e.g. topics and tactics) by particular social movements, two different social movement groups are likely to face varying degrees of threat from different grades of adversary.  In an actual threat-modeling discussion within an organization or social movement, *who* potential adversaries are is often more readily apparent than *how* or *where* such adversaries would carry out attacks.

Third, the countermeasures required to protect against certain higher-grade adversary attacks tend to be more sophisticated (requiring greater training or resources).  Likewise, higher-grade attacks can be defended against with less certainty.

#### Adversaries - from lowest to highest grade capabilities

Note that most techniques available to lower grade adversaries are also available to higher-grade adversaries.  Also, it is important to note that these categories are not sharply defined, for example police departments in large cities may have access to nation-state level resources, or a particularly skilled Neighborhood Nazi may possess advanced hacking skills that enable some corporate- or nation-state-level attacks.  Here we use three categories of adversaries: (1) low-resourced adversaries (which may only have certain advantages if they are located in close geographic proximity, e.g. capable of physically stealing devices, with relatively little effort); (2) Private industry & corporate security (i.e. many resources available, and certain unique advantages, such as being unconstrained by the US Constitution in terms of mass, warrantless data collection); (3) Nation-states (with access to unique forms of attack, including manipulating the supply chain at scale).  What follows are brief lists of example capabilities.

<!--condensed original ~seven categories into low-medium-high capability-->

1. **Low-resourced, technically unsophisticated adversaries**
   
    * *Open Source Intelligence*
      - concepts, guides (howto- and counter-)
      - public social media posts, open google groups
    
    - *local*
      - in person spying shoulder surfing passwords / info
      - device theft
    - phishing / social engineering / social media hijacking
    
    * doxxing
      * campaigns sometimes orchestrated by national groups
    * cyber attacks on very outdated devices
    
1. **Private industry & corporate security**
   
    * *Employers/Local Sysadmins*
      - work or school email and file storage
      - web browsing history and unencrypted content
      - password capture
      - local network censorship
    * data voluntarily shared with companies (machine learning, surveillance mining)
    
    * systematic data collection that would risk constitutional challenge if conducted by government agencies (e.g. license plate reader databases) 
    * cell site simulators/IMSI catchers - https://www.eff.org/deeplinks/2019/07/announcing-gotta-catch-em-all-understanding-how-imsi-catchers-exploit-cell
    * mobile phone text messages (SS7 system)
    * legal requests (subpeona) to commercial platforms (email, cloud storage)
    * covert physical attacks (a/v bugs, keystroke loggers)
    * social media monitoring
    * Fusion Center collaborations
    * commercial malware - phone hacking -- 
      - https://www.theglobeandmail.com/opinion/article-governments-are-deploying-spyware-on-killers-drug-lords-and/
      - also various citizenlabreports 
    * alexa, google, siri, etc. -- https://www.vice.com/en_us/article/kz4agn/police-promised-witnesses-free-ring-surveillance-cameras-if-they-testified-against-neighbors
    
1. **Nation-States**

    - *Local Law Enforcement*
        - legal requests (subpeonas, search warrants)
        - device confiscation and searches (e.g. Greykey)
    - the metadata trap -- https://theintercept.com/2019/08/04/whistleblowers-surveillance-fbi-trump/
    - mass surveillance (passive global surveillance of Internet and cell networks)
    - storage, search, and analysis (XKEYSCORE, EMBERS)
    - web redirection via packet injection (QUANTUM)
    - national-security requests (section 702 program)
    - access to internal corporate networks (NSA PRISM program)
    - custom malware, botnets
    - network attacks using zero-day vulnerabilities -- https://www.wired.com/story/imessage-interactionless-hacks-google-project-zero/
    - sophisticated physical attacks, including supply chain attacks (e.g. the NSA Tailored Access Operations program)
* advanced persistent threats against infrastructure (web servers)
* country-level censorship (e.g. the Great Firewall of China)
* machine learning -- https://www.propublica.org/nerds/making-sense-of-messy-data#166075

In the sections corresponding to each grade of adversary, we will highlight important examples of attacks against social movements, whenever possible.

#### What to learn next

<!--The following chapters provide detailed discussions on each grade of adversary and suggested countermeasures.  Alternatively, skip to the most relevant to the social movement group of interest.-->


#### External resources

##### Threat modeling
* NYCATC threat matrix
* [threat modeling with the EFF](https://ssd.eff.org/en/module/assessing-your-risks)

##### Adversary capabilities
* [NSA programs at Snowden Archive](https://snowdenarchive.cjfe.org)

* alternative snowden archive

  
