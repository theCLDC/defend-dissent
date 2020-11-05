## Introduction: Why Digital Security?

In the summer of 2013, Edward Snowden shook the world with a trove of disclosed documents from the National Security Agency, Central Intelligence Agency and a host of other global three-letter agencies.  For more than a year, there were weekly (if not daily) revelations of just how extensive the digital information gathering capabilities were, particularly of the United States.  It felt as though the NSA was able to get any information that went through internet or phone networks that wasn't encrypted plus some information that was weakly encrypted and some more information that wasn't encrypted on corporate servers.  That feeling is close to the truth.

At the time, I had been engaged in environmental activism and was aware of how social movements had historically suffered from state repression that was made possible through spying.  The sheer extent of the information that the NSA and CIA were able to gather meant that suppression efforts by the State could be all the easier and more effective.  The more information the State knows about your activities, the easier it is for the State to interfere with your goals. 

So, I was worried.  Could we combat climate change when the odds are stacked against all the groups working to do so?  What about systemic racism?  Did we have any hope?  

Not long after the Snowden revelations, I partnered with the Civil Liberties Defense Center (CLDC), a non-profit that provides legal support to  social movements that "seek to dismantle the political and economic structures at the root of social inequality and environmental destruction."  The CLDC gives know-your-(legal)-rights trainings to social movement participants emphasizing how to protect and invoke one's First and Fourth Amendment rights: the right to free speech and the right to no illegal searches and seizures.  These rights are eroded with mass surveillance.	This is quite clear with Fourth Amendment rights.  For First Amendment rights, legal scholars often point to the *chilling effect*: that citizens restrict their speech if they know they are being surveilled.  To complement the CLDC's legal trainings, I started regularly holding digital security trainings for activists, centered around the premise that **encryption is the only way to protect your First and Fourth Amendment rights in the modern world of mass surveillance**.  This book has grown out of these educational efforts.

### Downloading a "secure" app isn't enough

It isn't enough to download a "secure" app.  Firstly, what does
"secure" even mean?  Security is a complex, subjective and
multifaceted concept.  While perfect freedom from risk is usually out
of reach, especially when digital technologies are involved, strong
relative protections are possible.  In order to evaluate or at least explain (and convince a group a people to take advantage of) the relative protections of an app requires understanding at least a little bit about cryptography and what information is at risk (and with what likelihood) when using a given app or digital service.

Our trainings scratch the surface of the information that I would like to impart.  Social movement participants tend to be busy people and often want a set of simple and doable digital security recommendations from people that they trust.  My goal with this book (and the companion course at Oregon State University: CS 175 Communications Security and Social Movements) is to increase the number of people who know enough to make those recommendations (or at least know how and where to learn more).

### Political Scope of this book

As might be gathered from the references to the First and Fourth
Amendments, this book is rooted in political arena of the United
States.  While much of the book will be relevant outside of the US
as well, we recommend that anyone applying this knowledge outside of the US get additional country-specific advice.

### Overview of this book

This book is not intended to be comprehensive for three reasons:
* I want this book to be accessible to any person who is curious.  Going into further details in cryptography would require some college-level mathematics. I also believe that one doesn't need to understand specific cryptographic protocols to make reasoned digital security recommendations -- one can lean on cybersecurity experts for that.
* The state of mass surveillance and the apps that are available to counter surveillance are constantly changing.  As I put the finishing touches on this book, I am resisting the urge to include the latest news on State surveillance capabilities.
* I want the book to be short enough to read in a weekend.

The book has three parts as follows:

#### Part I: An Introduction to Cryptography

This is a basic introduction to cryptography: enough to understand the basics of what information is protected and what is not and why.  Some interesting concepts (such as forward secrecy and blockchains) are left out because I felt that it might overwhelm my intended audience.  However, the curious reader, after reading Part I, should be able to appreciate, say, the Wikipedia articles on more advanced topics like forward secrecy and blockchains.

When describing cryptographic protocols, most people refer to a cast of characters: Alice sends a message to Bob and Eve might be eavesdropping on their communications.  The companion course for this book focuses on Civil Rights era social movements, particularly Black Liberation movements, and the State suppression of those movements.  To that end, rather than Alice, Bob and Eve, we use the running example of Assata communicating with Bobby, and Edgar is eavesdropping:
* Assata Shakur was a member of Black Liberation Army and Black Panther Party (in the early 1970s), was targeted by the FBI (as described in the Chapter on [Mechanisms of Social Movement Suppression](2-01_suppression.md)), and is still a political refugee in Cuba.
* Bobby Seale is a co-founder of the Civil Rights Era Black Panther Party and was also subject to surveillance and harassment by the FBI.
* J. Edgar Hoover founded the FBI and has been deemed responsible for the surveillance and repressive efforts of the FBI.  We occasionally refer to Edgar as "the Man" where appropriate (i.e. in the Chapter on [The Man in the Middle](1-5_man-in-the-middle.md), where a man-in-the-middle attack is standard cryptographic terminology.

While the remainder of the book is likely to require significant updates in the coming years, Part I is likely to stand the test of time.

#### Part II: Digital Suppression of Social Movements (in the US)

This part is rather depressing as it overviews:
* How social movements have historically been suppressed in the US (and where surveillance plays a role) in the Chapter on [Mechanisms of Social Movement Suppression](3-0_defense_overview.md), and
* What surveillance and other digital threats are in use in the US in the Chapter on [Digital Threats to Social Movements](3-1_security_culture.md)
In this Part, we use "the State" to refer to any constellation of governmental
and non-governmental organizations that represent established power
structures with the resources and motivation to deploy a wide range of
suppressive strategies and sophisticated technical measures against
social movements.

We keep this part deliberately short so that we can move onto the last part, which is more empowering.  In Part II, we pick *illustrative examples* to give an overview of how mechanisms of social movement suppression are used and what types of surveillance and other digital threats are in play.  The Chapter on [Digital Threats to Social Movements](3-1_security_culture.md), in particular, will never be up to date, as new threats and capabilities are constantly being developed and deployed.  We hope that anyone who reads this Part quickly follows up with the last Part.

#### Part III: Defending Social Movements (in the US)

Part III is intended to be empowering.  Starting with threat analysis (which is country and context dependent), we quickly move into *classes* of tools to protect your information.  I say classes of tools rather than specific tools as specific tools can come and go as the projects supporting those tools or apps can fail or appear and it will not be feasible to update this book multiple times a year.  This section is country dependent, as the availability of or associated risk of using certain tools can depend on the political context in which you are.  For example, it can be more challenging to use Tor (an anonymity-providing internet browser, which we will discuss in the Chapters on [Anonymous Routing](1-a10_anonymous-routing.md) and [Protecting your Identity](3-5_apac.md)) in certain countries that engage in widespread censorship (such as China).

#### What to learn next 

* [What is Encryption?](1-1_cryptography.md)
* [Mechanisms of Social Movement Suppression](2-01_suppression.md)
