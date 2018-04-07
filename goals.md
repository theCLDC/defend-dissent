## Goals 

Here we discuss what we are trying to achieve in our discussion of communications security for liberatory social movements.

#### What does Security mean?  What is the end goal of better communications security and digital security practices?

Security is a subjective, multifactored, complex, and gendered concept.  Security can be thought of as both (a) the subjective feeling of being free from or protected against threats and (b) having safe or protected spaces to carry out social movement work.

This topic has been explored in great detail for two groups: journalists and human rights workers, focusing especially on risks for those working in geographical areas where political violence is commonplace.  Likewise there are well-developed digital security resources available to these groups (e.g. , [Access Now](https://accessnow.org), [Security in a Box](https://securityinabox.org/en/), and [Digital First Aid Kit](https://www.digitaldefenders.org/digitalfirstaid/)) as well as for trainers working with them (e.g. [Holistic Security](https://holistic-security.tacticaltech.org/) and [Level Up](https://level-up.cc))  In the same vein, assessments of digital threats tend to focus on overtly authoritarian states (see many excellent investigations and reports by [Citizen Lab](https://citizenlab.ca)).

For social movements based in the United States of America, where political expression and activity have a high degree of formal protection, digital security recommendations are often directed at the general public (e.g. [Securing your Digital Life like a Normal Person](https://medium.com/@mshelton/securing-your-digital-life-like-a-normal-person-a-hasty-and-incomplete-guide-56437f127425), the excellent [Library Freedom Project](https://libraryfreedomproject.org/resources/), and to some extent [a DIY Guide to Feminist Cybersecurity](https://hackblossom.org/cybersecurity/)].  Some resources (e.g. by [Equality Labs](https://www.equalitylabs.org/internet-freedom-and-digital-security/), [Ruckus Society](https://ruckus.org/training-manuals/security-tips-resources/), and parts of [EFF Surveillance Self-Defense](https://ssd.eff.org/)) are explicitly intended for communities of color and direct-action oriented environmental, social justice, and racial justice groups, who have experienced generations of varying degrees of directed police violence and state suppression.  Most general digital security advice is relevant to activists, of course, as a baseline of security practices.  

So what is missing?  Two things: 1) continuing-education resources for social movement geeks, who might lack formal computer science education but who could benefit from a deeper dive into technical topics that is relevant and accessible; and 2) a clear, up-to-date articulation of specifc digital threats to social movement groups for people working to convince their comrades of the importance of taking their security seriously, and expending the effort in making moves toward more secure platforms and practices.

And so in this text we focus our efforts on the foundations of cryptography and digital communications, and attempt to delineate the *minimum* capabilities of distinct adversaries threatening US-based social movements.  Because of the global reach of many adversaries and the international scope of many social struggles, we anticipate that many of these lessons will be applicable to social movement activists in other contexts as well.

#### Comprehending and categorizing threats

Digital threat modeling--understanding what information or communications need to be protected, who they need to be protected from, and the degree of harm if they are compromised--is the starting point of most approaches to digital security.  Comprehending the full range of digital threats available to adversaries is difficult enough--realistically assessing the likelihood that these threats will be deployed (especially by various levels of law enforcement or private security) can be especially challenging.

This is covered in detail in the [Overview of threats](threat-overview.md) section.

#### Countermeasures

While we won't spend much time listing specific "secure" apps, technologies, and platforms (since this work is well done elsewhere) we will explore fundamental properties of security-enhancing technologies and choices.

1. Minimize the number of **trusted** platforms, apps, devices, and people.  In contrast, **trustworthy** entities are essential to community organizing and should be embraced and nurtured!  But make technological and operational choices that *require* the trust of as few as possible--since each **trusted** entity represents a possible point of compromise.

1. Use [open source](modern-cryptography#security-is-provided-by-transparency) apps whenever possible.

1. Use [end to end encrypted](end-to-end-encryption.md) apps whenever possible, otherwise store data locally.

1. Ensure devices remain under your physical control (they are not confiscated or physically accessed without your knowledge).

1. Keep all and device operating systems up to date.

1. Use [strong passwords](passwords.md).

#### External resources

* [Holistic Security](https://holistic-security.tacticaltech.org/)
* [Surveillance Self-Defense](https://ssd.eff.org/)
* [Security Education Companion](https://sec.eff.org/)
* [Security in a Box](https://securityinabox.org/en/)
* [Digtial First Aid Kit](https://www.digitaldefenders.org/digitalfirstaid/)