## Introduction, Scope & Goals 

What are we trying to achieve in technical and political discussions of communications security for liberatory social movements?

In this text we focus on the foundations of cryptography and digital communications, and attempt to delineate distinct classes of adversaries facing social movements seeking radical social and environmental change in the United States.  We define adversary classes in part by their *minimum known* surveillance capabilities.  Such capabilities arise variously from technical sophistication, financial resources, and legal authorities.  Because of the international scope of many social movement campaigns and the global reach of most powerful adversaries, we anticipate that much of this work will be relevant for social movements outside of the U.S. as well.

### Who is this text written for? and other definitions

We write for individuals organizing movements working for the liberation of human and non-human animals and to preserve the ecological systems upon which all depend.  For students of [CS 175](https://secure.oregonstate.edu/ap/cps/documents/view/123515) (at Oregon State University) and any course examining issues of difference, power, and discrimination, particular attention is given to social movements that employ direct action tactics, as such movements tend to be the focus of the broadest spectrum of State suppression methods.

In this text, "the State" refers to any constellation of governmental and non-governmental organizations that represent established power structures with the resources and motivation to deploy a wide range of suppressive strategies and sophisticated technical measures against social movements.  A common aim is to neutralize and otherwise oppose their political objectives.

### What does Security even mean?  

Security is a complex, subjective, gendered, and otherwise multifaceted concept.  While perfect freedom from risk is usually out of reach, especially when digital technologies are involved, strong relative protections are possible.  Security can be thought of as both: (a) the perception of being free from or protected against physical and social harm, or threats of harm; and (b) the availability of safe or defensible spaces to carry out social movement work.  

This topic has been explored in depth for two at-risk groups: journalists and human rights workers.  Digital security practitioners (e.g. trainers, auditors, risk assessors) mainly focus on risks facing individuals and groups in geographical regions where the legal system or extrajudicial political violence threatens human rights defenders, perceived political adversaries, journalists, whistleblowers, and sources.  Accordingly, there are well-developed digital security resources tailored to these groups (e.g. [Access Now](https://accessnow.org), [Security in a Box](https://securityinabox.org/en/), and the [Digital First Aid Kit](https://www.digitaldefenders.org/digitalfirstaid/)) as well as educational materials for trainers engaging with them (e.g. [Holistic Security](https://holistic-security.tacticaltech.org/) and [Level Up](https://level-up.cc)).  In the same vein, critical work assessing digital threats tend to emphasize overtly authoritarian states (e.g. the many excellent investigations and reports by [Citizen Lab](https://citizenlab.ca)).

For social movements based in the United States of America, where political expression has a high degree of formal protection under the law, digital security recommendations are often directed at the general public (e.g. [Securing your Digital Life like a Normal Person](https://medium.com/@mshelton/securing-your-digital-life-like-a-normal-person-a-hasty-and-incomplete-guide-56437f127425)) or at-risk individuals (e.g. the excellent [Library Freedom Project](https://libraryfreedomproject.org/resources/), as well as [a DIY Guide to Feminist Cybersecurity](https://hackblossom.org/cybersecurity/)).  Certain resources (e.g. [Equality Labs](https://www.equalitylabs.org/internet-freedom-and-digital-security/), [Ruckus Society](https://ruckus.org/training-manuals/security-tips-resources/), and certain parts of [EFF's Surveillance Self-Defense](https://ssd.eff.org/)) are explicitly intended for communities of color and direct-action oriented environmental, social justice, and anti-racist groups, who have often experienced generations of  targeted police violence and state suppression.  

Most general digital security advice is relevant to social movement activists, of course, as a baseline of good security practice.   So what exactly is missing, and what are we trying to address here?  

### Goals

We have three primary goals: 1) to provide continuing-education resources for computer-savvy or techno-curious members of social movements, who may lack formal computer science training but who stand to benefit from a (relevant, accessible) deeper dive into technical topics; 2) a clear, up-to-date articulation of specific digital threats facing social movement groups, especially to support individuals seeking to convince their colleagues of the importance of implementing strong digital security measures; and 3) promoting movement-wide adoption of better-secured digital platforms and practices.

### Comprehending and categorizing threats

Digital threat modeling--understanding what information or communications need to be protected, who they need to be protected from, the risk (likelihood and degree of harm) associated with compromise--is the starting point of most structured approaches to digital security.  Comprehending the full range of digital threats available to adversaries is difficult enough--realistically assessing the likelihood that these threats will be deployed (especially by various levels of law enforcement or private security) is an added challenge.

This is covered in detail in the [Overview of threats](threat-overview.md) section.

### Properties of effective countermeasures

This text examines a small set of security-focused apps, technologies, and platforms.  These are used as case studies to illustrate fundamental elements of good security practices and security-enhancing technologies:

1. **Minimize** the number of platforms, apps, devices, and people requiring absolute **trust**.  Given that, for most entities, full, continuous verification is not feasible, the fewer entities that must be trusted with privileged access to information or devices, the fewer opportunities exist for an adversary to compromise information or device security.  This negative concept of trust should be contrasted with **trustworthiness**.  Trustworthy people and relationships, as well as certain technologies, are essential to social movement organizing and should be embraced and nurtured!  At the same time, technological and operational choices should be made to *require* the trust of as few entities as possible.  This is another way of saying reducing attack surface.
1. [Open source](modern-cryptography#security-is-provided-by-transparency) apps should be used whenever possible.  Only apps for which source code is available can be audited on a free and ongoing basis.
1. [End to end encrypted](end-to-end-encryption.md) apps should be used whenever possible, such that communications infrastructure and platforms are not required to be trusted.  
1. Devices should remain under your physical control (they are not confiscated or otherwise physically accessed without your knowledge).
1. Device operating systems and firmware should be updated to patch security vulnerabilities.
1. Use [strong passwords](1-6_passwords.md) and [good password practices](password-practices.md).
1. [Compartmentalize](security-culture.md) communications whenever feasible. 

### What is the end goal of better communications security and digital security practices?

In the real world, digital security can never be guaranteed.  In part this is due to the intrinsic complexity of digital systems <!--[if sensible, ref proof that general purpose computers inevitably have bugs]-->.  A second major factor is that no fully open computer exists, i.e. the proprietary design of nearly all microprocessors, motherboards (including systems-on-chips), peripherals, and device drivers preclude full and transparent security audits.  <!--[name some specific concerns: ref Intel ME,  x-ray/electron micrograph evidence of undocumented 3G].-->  

In this light, defensive security measures become *more* meaningful as one moves away from securing the individual toward securing social movements and organizations.  While guaranteeing a particular individual's safety might be infeasible, each security measure undertaken increases the costs and risks of surveillance.  For well-resourced adversaries, financial cost is perhaps less relevant than the political risk associated with the discovery or disclosure of covert surveillance.  Consider first that mass surveillance that relies on passive data collection is both cheap and often undetectable.  Such passive data collection methods are relatively easy to defeat, using the simple countermeasures meeting the criteria above.  Active surveillance methods required to circumvent such countermeasures are often invasive and risk discovery or provoking  whistleblowers to disclose surveillance activities.  Social movements, especially those deploying non-violent methods, may gain strategic/political advantage over an adversary that deploys sophisticated surveillance methods normally justifiable only in the case of averting direct threats to human life.   

In summary, social movements and their individual members can act in solidarity with one another <!--[ref machine learning in future version]--> to improve the collective security of social movements that challenge injustices and the inequitable distribution of social, economic, and political power.

### Selected external resources

* [Holistic Security](https://holistic-security.tacticaltech.org/)
* [Surveillance Self-Defense](https://ssd.eff.org/)
* [Security Education Companion](https://sec.eff.org/)
* [Security in a Box](https://securityinabox.org/en/)
* [Digtial First Aid Kit](https://www.digitaldefenders.org/digitalfirstaid/)