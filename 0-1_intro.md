## Introduction, Scope & Goals 

Here we discuss what we are trying to achieve in our discussions of communications security for liberatory social movements.

In this text we focus on the foundations of cryptography and digital communications, and attempt to delineate the *minimum known* capabilities of distinct classes of adversaries threatening US-based social movements.  Because of the global reach of many adversaries and the international scope of many social struggles, we anticipate that much of this knowledge will be relevant to social movements outside of the United States.

### What does Security mean?  

Security is a complex, subjective, gendered, and otherwise multifaceted concept.  Security can be thought of as both: (a) the perception of being free from or protected against harm or threats of harm; and (b) having safe or defensible spaces to carry out social movement work.

This topic has been explored in depth for two groups: journalists and human rights workers, focusing on risks for those working in geographical regions where political violence or legal system threats to the practice of journalism (e.g. sources) is commonplace.  Accordingly, there are well-developed digital security resources available to these groups (e.g. , [Access Now](https://accessnow.org), [Security in a Box](https://securityinabox.org/en/), and [Digital First Aid Kit](https://www.digitaldefenders.org/digitalfirstaid/)) as well as educational materials for trainers working with them (e.g. [Holistic Security](https://holistic-security.tacticaltech.org/) and [Level Up](https://level-up.cc)).  In the same vein, assessments of digital threats tend to emphasize overtly authoritarian states (see many excellent investigations and reports by [Citizen Lab](https://citizenlab.ca)).

For social movements based in the United States of America, where political expression and activity have a high degree of formal protection under the law, digital security recommendations are often directed at the general public (e.g. [Securing your Digital Life like a Normal Person](https://medium.com/@mshelton/securing-your-digital-life-like-a-normal-person-a-hasty-and-incomplete-guide-56437f127425), the excellent [Library Freedom Project](https://libraryfreedomproject.org/resources/), as well as [a DIY Guide to Feminist Cybersecurity](https://hackblossom.org/cybersecurity/)).  Some resources (e.g. by [Equality Labs](https://www.equalitylabs.org/internet-freedom-and-digital-security/), [Ruckus Society](https://ruckus.org/training-manuals/security-tips-resources/), and parts of [EFF Surveillance Self-Defense](https://ssd.eff.org/)) are explicitly intended for communities of color and direct-action oriented environmental, social justice, and anti-racist groups, who have experienced generations of varying degrees of targeted police violence and state suppression.  Most general digital security advice is relevant to activists, of course, as a baseline of security practices.  

So what is missing, and what are we trying to address here?  We have three primary goals: 1) continuing-education resources for computer-savvy or techno-curious members of social movements, who in some cases have forgone a formal computer science education but who stand to benefit from a (relevant, accessible) deeper dive into technical topics; and 2) a clear, up-to-date articulation of specific digital threats to social movement groups for all those working to convince their colleagues of the importance of taking their security seriously; 3) and prioritizing organization- or movement-wide adoption of better secured platforms and practices;

### Comprehending and categorizing threats

Digital threat modeling--understanding what information or communications need to be protected, who they need to be protected from, and the degree of harm if they are compromised--is the starting point of most approaches to digital security.  Comprehending the full range of digital threats available to adversaries is difficult enough--realistically assessing the likelihood that these threats will be deployed (especially by various levels of law enforcement or private security) is an added challenge.

This is covered in detail in the [Overview of threats](threat-overview.md) section.

### Countermeasures

We cover only a limited number of specific security-focused apps, technologies, and platforms.  These cases are used to illustrate what we consider to be fundamental elements of good security practices and security-enhancing technologies:

1. Minimize the number of **trusted** platforms, apps, devices, and people.  In contrast, **trustworthy** entities are essential to community organizing and should be embraced and nurtured!  But make technological and operational choices that *require* the trust of as few as possible--since each **trusted** entity represents a possible point of compromise.
1. Use [open source](modern-cryptography#security-is-provided-by-transparency) apps whenever possible.
1. Use [end to end encrypted](end-to-end-encryption.md) apps whenever possible, otherwise store data locally.
1. Ensure devices remain under your physical control (they are not confiscated or otherwise physically accessed without your knowledge).
1. Keep all and device operating systems up to date.
1. Use [strong passwords](passwords.md) and [practices](password-practices.md).
1. [Compartmentalize](security-culture.md) communications whenever feasible. 

### What is the end goal of better communications security and digital security practices?

In the real world, digital security can never be guaranteed.  In part this is due to the intrinsic complexity of digital systems <!--[ref proof that general purpose computers inevitably have bugs]-->.  A second major factor is that no fully open computer exists, i.e. the proprietary design of most microprocessors, other hardware, and device drivers preclude transparent security audits.  <!--[specific concerns: ref Intel ME, wifi chip].-->  

In this light, however, defensive security measures become more meaningful within an organizational or social movement context.  While guaranteeing a particular individual's safety might be infeasible, each security measure increases the costs of surveillance.  For well-resourced adversaries, financial cost is perhaps less relevant than the political cost associated with the risk that surveillance efforts will be discovered.  Consider that mass surveillance that relies on passive data collection is both cheap and largely undetectable.  Such passive data collection methods are relatively easy to defeat, using the simplest of the countermeasures above.  On the other hand, the increasingly invasive, active surveillance methods required to circumvent these countermeasures carry the risk of physical discovery or provoking disclosure of surveillance programs by whistleblowers.  Social movements, especially those deploying non-violent methods, may for example gain strategic advantage over a political adversary that deploys some sophisticated technical measure normally justifiable only in the case of protecting direct threats to human life.   

In summary, social movements and their individual members can act in solidarity with one another <!--[ref machine learning in future version]--> to improve the collective security of the broad swath of civil society comprised of social movements that challenge injustices and the inequitable distribution of social, economic, and political power.

### What to learn next



### External resources

* [Holistic Security](https://holistic-security.tacticaltech.org/)
* [Surveillance Self-Defense](https://ssd.eff.org/)
* [Security Education Companion](https://sec.eff.org/)
* [Security in a Box](https://securityinabox.org/en/)
* [Digtial First Aid Kit](https://www.digitaldefenders.org/digitalfirstaid/)