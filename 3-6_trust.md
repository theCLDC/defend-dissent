## Conclusion: Selecting Digital Security Tools

> We recommend that you read this section last.
	
#### What you'll learn

1. Criteria for evaluating and selecting communications tools.

---

There are many different digital security tools from which to choose.  Decisions about which to use can be overwhelming.  When we recommend a tool we try to pick a tool such that we can minimize trust in the providers of the tool.  The **required criteria** listed below are selected with this in mind.  We include **additional technical criteria** which would be nice to meet, but aren't as essential.  Finally, there are some **non-technical criteria** that technology providers make that can help when making decisions among the myriad of choices.  

Rarely will a tool be perfect, as we will illustrate with examples.  Part of the selection process is finding the tool that is right for the group that will use it.  This might result in compromises, even on the required criteria.  And note that not every criteria is applicable to every tool.  For example, the Tor Browser provides the ability to anonymously browse the internet but on its own does not aim to provide end-to-end encryption, so the first criteria doesn't apply.

Finally, choose a tool carefully and test it out before asking a lot of people to adopt it.  There is a social cost to asking people to use something new or change their practices and you want to minimize how often this happens.

### Required criteria

1. **End-to-end encryption** (as described in the Chapter on [Protecting your Communications](3-3_comms.md)) allows us to follow the security culture principle of minimizing the number of trusted parties.  End-to-end encryption allows you to keep your data from the tool provider (but not necessarily the meta-data).  Having robustly implemented end-to-end encryption is our number one criteria for protecting the rights of social movement participants (and everyone).

1. If a tool provides the **ability to authenticate your contacts' keys** via fingerprinting, this allows you to prevent man-in-the-middle attacks as described in the Chapter on [The Man in the Middle](1-5_man-in-the-middle.md).  Further, if the tool does not provide this fingerprinting ability, the provider of the tool could be mounting man-in-the-middle attacks all the time without anyone being able to tell.

1. Having an **open source client** allows the broader community of cybersecurity professionals to verify, for example, that end-to-end encryption is indeed robustly implemented.  Source code and what open source means is described in the Chapter on [Modern Cryptography](1-2_modern-cryptography.md).  By client, we mean the code for the app that would run on your device as distinctive from software that would run on the provider's servers.  Having an open source server software would also be ideal, but many apps keep that software closed so as to protect their intellectual property.  However, since encryption occurs on the device, it is sufficient to verify how much information the server would see by examining the source code for the client.

1. Having the **ability to authenticate the app** does what it says requires more than just access to the source code.  You also need to be able to verify that the app you download is the app that comes from the source code.  This requires two steps: (a) being able to reproduce that the app that you run on your device is indeed compilable from the published (open) source code, and (b) ensuring that the app or source code is authentically that which the provider makes available (isn't subject to a scam as in the story at the end of the Chapter on [Protecting your Identity](3-5_apac.md) or a man-in-the-middle attack).  The former is rarely made available for any user and can be very difficult to do.  But the latter can (and is for many tools) be verified using cryptographic signatures as described in the Chapter on [Authenticity through Cryptographic Signing](1-8_authenticity.md).

1. An app should be under **active development** and have **responsive developers**, for if it is not, it will not be keeping up with even the most basic updates like keeping up with the operating systems (e.g. Android, iOS) as they change.  Further, if a problem is found with an app, it needs to be fixed quickly to keep all the app's users' information safe.

### Additional desirable technical criteria

1. A digital security tool should be **cross-platform and otherwise widely accessible**.  By cross-platform, we mean that (ideally and if applicable) be able to run on Linux, Mac, and Windows operating systems as well as Android and iOS smartphones.  Further, tools should play well with screen readers and other accessibility measures.  Compromises on this should not be taken lightly.  Perhaps at the moment, everyone in your group has Android devices and so using an Android-only communication tool might be okay.  For now.  But what if in the future someone wants to join the group who doesn't have an Android phone (or any smartphone)?

1. **Security audits** are when a (responsible and respected) third party evaluates the security of a given tool by looking at their code and server practices.  For some tools, this is an unreasonable ask.  For example, Whonix, an anonymity- and security-focused operating system based on Linux, has not undergone a security audit.  But no operating system has undergone a complete security audit.

1. A tool that provides for **anonymity** or **pseudonymity** is more desirable.  This can go as far as being Tor compatible.  Or it can make pseudonymous accounts easy (for example, by not requiring a phone number or email address to register).

1. **Tool defaults** make a big impact on users' practices.  We have seen a number of secure messaging apps over the years that don't have encryption enabled by default.  How many users will forget to enable encryption when they start a new conversation?

1. The **degree of centralization** of a tool can impact both quality of service but also changes how much data over which a single entity has control.  For example, a communication app can either route all communications through the provider's server, or the server can be used to initialize the communication and thereafter the data goes directly between the users (through the internet but not through the provider's server).  The latter is called *peer-to-peer* communication and can improve call quality (by shortening the distance in the network) and reduce the amount of metadata available to the provider (such as call length).  Another option is to allow federation.  Consider, as an example, email: one can send emails between different email providers (e.g. Google to Microsoft).  On the other hand, Signal only allows two users to communicate if they are both using Signal and establishing their calls with Signal's servers.

### Non-technical criteria

1. The **financial model** of a provider can impact the ability to access a tool (if you need to pay for access), the long-term stability of the tool (what happens if they run out of money?), and the motivations of the provider (are they monetizing your data or metadata for?).  Choices range from free through freemium (pay for more services) through pay-to-play.  
If a tool is free to use, once should ask why?  Is it run by a large company that can monetize even the metadata (such as Facebook having access to contact networks of WhatsApp)?  Or is running on donations and grants?

1. If a tool is **movement oriented**, this can either be positive or negative.  As discussed at the end of the Chapter on [Protecting your Communications](3-3_comms.md), an unencrypted video conferencing option through movement-oriented Mayfirst was more trustworthy than that through Zoom which has been known to engage in censorship and data-sharing with authorities.  On the other hand, a VPN option through movement-oriented Riseup might draw more attention from authorities as opposed to hiding among the users of a more populous VPN.

1. **Provider transparency** can help to build trust.  Most major companies publish transparency reports as discussed in the Chapter on [Understanding Surveillance Threats](2-02_digital-threats.md).  In many cases these only underscore how much the companies are willing to share their data with your opponents.  Another option is the **warrant canary** which we discussed in the Chapter on [Authenticity through Cryptographic Signing](3-6_trust.md).

#### What to learn next 

There are a number of guides and resources that delve into more detail for particular users or particular aspects that we recommend for further study:	
* [The Holistic Security Manual](https://holistic-security.tacticaltech.org/)
* [Surveillance Self-Defense](https://ssd.eff.org/)
* [Security Education Companion](https://sec.eff.org/)
* [Security in a Box](https://securityinabox.org/en/)
* [Digtial First Aid Kit](https://www.digitaldefenders.org/digitalfirstaid/)
