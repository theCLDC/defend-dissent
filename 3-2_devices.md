## Protecting your Devices

> We recommend that you read the Chapters on [Passwords](1-6_passwords.md) and [Digital Threats to Social Movements](2-02_digital-threats.md) before reading this chapter.

#### What you'll learn
1. Common ways in which phones and computers are compromised.
1. Strategies for protecting phones and computers.

---

The amount of data you keep on your phone and laptop is staggering.  Contacts, emails, photos, documents, calendars, tax returns, banking details, and, in the case of a smartphone, often a detailed history of your location as long as you've had that phone.
A lot of this data you will also share with your cloud storage providers (i.e. Apple, Google, DropBox), but that is the focus of the Chapter on [Protecting your Remote Data](3-4_cloud.md). Here we focus on protecting the data that you keep with you, on your laptops and cell phones, from a remote or physical attack.

### Physical attacks

By a physical attack, we mean that your adversary would first gain physical access to your device through loss, theft, or confiscation.  You may lose your phone at an inopportune moment that places it in the hands of an adversary rather than a good Samaritan, or your adversary may steal your phone.  More likely your phone may be confiscated while crossing a border or during an arrest, either planned or unplanned.

Those who were swept up in the mass arrests during the protests of the presidential inauguration on January 20, 2017 (J20) had their phones confiscated and subject to search by a tool from the Israeli company Cellebrite which extracts all information on a device (phone or computer) and all remote accounts that device has access to (e.g. Google, Facebook, Dropbox).  One J20 defendant described the 8000 pages of data that a Cellebrite tool extracted from his confiscated cell phone; he received this information from his lawyer as they prepared for his defense:

> * A list of all my contacts, including phone numbers and emails that contacted me that were not stored in my phone, with a count of how many times I called, messaged, or emailed them or was called, messaged, or emailed by then.
> * The number of emails I received, sent, and drafted to specific email addresses and how many shared calendar events I had with those email addresses.  The number of incoming/outgoing/missed calls from each number and if they were my contacts, and how long total calls were between me and a number.  Whether they were in my contacts, and if so what nickname I call them in my phone.
> * The number of SMS texts received/sent/drafted to a number.  The content of all texts, even if they were deleted, including drafts.
> * Whatsapp contacts, their "usernames" (i.e. the phone number attached to their account), and how many chats/calls took place between me and them.
> * All apps, when they were installed/deleted/last used/purchased, and what permissions they had.
> * Audio files that were stored in Google Drive, as well as any podcasts, voice memos, and ringtones.  Timestamps for their creation/deletion/modification/last access.
> * All calendar events, attendees invited, location tags, etc.
> * Traditional call log info you might expect.
> * Date and time of all cell towers my phone had ever connected to and their location, conveniently linked to Google Maps.  A world map marking all cell towers accessed by my phone.
> * Chats from Signal, WhatsApp, SMS, Google Hangouts, TextSecure, GroupMe, and Google Docs; a list of all participants in those chats; text body content; whether it was read or unread, with a timestamp for sent and read; if it was starred; if it was deleted; all attachments.  These chats were also from years ago, before I even had a smartphone.
> * All information for my contacts, including whether the contact was deleted or not.
> * Web browser cookies.
> * Any document ever opened on my phone, including text documents, attachments, Google docs, and those created by apps.
> * Emails and email drafts, including all sending information, entire text content, and up to 16 attachments.
> * Images/photos/videos along with their created/accessed timestamp and any metadata.
> * Ninety-six random tweets from one of my Twitter accounts, some from as far back as 2013.
> * A list of all wifi networks that my phone ever connected to, their passwords, hardware identifiers, and when I connected to them.
> * The last five times my phone was turned on, including twice two months after I lost access to it.
> * Web history and web and Playstore search history.
> * A list of every word ever typed into my phone and how many times that word was typed, including email addresses as words, and words I added to the dictionary to they wouldn't continue to be autocorrected to something else.
> * What they call my "timeline": every action (texts, calls, emails, web history, app usage including maps searches, connections to wifi networks or new cell towers, etc.) with timestamp to be easily sorted. 

<!--
![From "How to Protect Yourself from the Snitch in Your Pocket", Earth First! The Journal of Ecological Resistance. Winter 2017-18.](pictures/cellebrite-data-extraction.jpg)-->

#### What can I do?

A detective testifying at a J20 trial noted that among the phones that had encryption enabled, he was only able to access basic device information and not the contents of the phone storage. iPhones and Android devices that are running up-to-date operating systems  have encryption enabled by default, while Apple and Microsoft computers need to have this enabled.  Encrypting your device is not, however, a panacea.  The encryption that protects your device is only as strong as the password protecting it.

Device encryption passwords regrettably suffer from a convenience-security tradeoff.  A passphrase (as described in the Chapter on [Passwords](1-6_passwords.md)) may need to be composed of 6 or more words to sustain a physical attack, but such a passphrase is cumbersome to type in frequently.  There are a few options, all with trade-offs.  For phones or laptops, you can modify your settings to change how often you need to enter your password, passphase or unlock code. (Note that encryption is only in effect when a screen lock is enabled.) Or you could modify the strength (length) of your password, passphase or unlock code depending on your situation.  However, these strategies rely on knowing when your situation requires higher levels of security and consistently strengthening your security when needed.

For phone and some laptops, one can often choose between a typed passphrase or biometric input (such as a fingerprint).  A fingerprint is more convenient than a typed password.  For the purposes of encryption, your fingerprint will be paired with a passphrase (which should be as strong as you can manage).  However, if your device is confiscated by law enforcement, your fingerprint may be compelled from you.  So when the risk of device confiscation is high, one should still consider removing the ability to biometrically unlock your device.

There are additional protections against physical interference that one might consider.  A privacy screen can provide protection from an eavesdropper to you typing in passwords (and anything else).  Faraday bags can prevent your phone from transmitting or receiving information; among other things, this can prevent your phone from recording location information.  The ability to remotely wipe your phone is provided by major cell phone manufacturers, and while it may relinquish control over your device to the same corporations that may share your information with your adversaries (as we discuss in the Chapter on [Protecting your Remote Data](3-4_cloud.md)), it may be a useful tool in certain situations.

### Remote attacks

By a remote attack, we mean that an adversary would access the data on your phone or laptop through an internet or data connection.  There are companies that design and sell the ability to infect your device (usually focusing on smartphones) with malware that would allow their customer (your adversary, be it a corporate or state agent) to gain remote access to some or all of your information.

For example, Citizen Lab uncovered wide and varied use of the spyware Pegasus created and sold by another Israeli company, NSO Group.  Coupled with some social engineering to convince the target to click on a link, the spyware grants the ability to turn on and record from the phone's camera and microphone, record calls and text messages (even those providing end-to-end encryption), log GPS locations and send all this information back to the target's adversary. Citizen Lab reported that Pegasus attempts were made against Ahmed Mansoor, a human rights defender based in the UAE and 22 individuals in Mexico ranging from politicians campaigning against government corruption to scientists advocating for a state tax on sugary drinks.

#### What can I do?

Remote attacks, such as sold by NSO Group, rely on flaws in computer software known as zero-days. Such flaws are unknown to the software provider (e.g. Apple or Microsoft). Until they are known to the software provider (which happens on "day zero"), there is no chance that the software provider could have fixed or patched the vulnerability and so there is no chance that a victim could protect themself.  Computer security is often a cat-and-mouse game.  The products of malware and spyware creators (such as NSO Group) are only good so long as the targets (or more accurately, companies like Apple, Google and Microsoft) don't know about the malware being deployed.  As soon as they do, they fix their products so that the malware is no longer effective.

But these product fixes only work if the target (you) update your device.  So the lesson here is to **install all security updates as soon as they are available**.  Unfortunately, smartphones do not receive security updates indefinitely, with particular devices (e.g. Nokia 5.3) only being supported by an operating system (e.g. Android) for a few years.  You can check if an Apple or Android phone is receiving security updates through the settings.

Many malware products require phishing for installation on the target's device: convincing the target to click on a link or opening a file (either in an email or a text message).  So, the second thing you can do is **be wary of what you click on**.  Do you know the sender?  Are you expecting something from the sender?  Does anything seem, well, fishy?  In fact, it was vigilance that led Ahmed Mansoor to avoid spyware infection: he sent the phishing text along to Citizen Lab that led to their reporting on the abuse of spyware from NSO Group.

Finally, **be wary of the apps you install and what permissions you grant them**.  Does a flashlight app need access to your contacts and camera?  Do you really need to install that game created by an unknown software creator?  Every app you install is a potential vector for malware, so it is a good opportunity to practice minimalism.

### In context: Compromising protestors' phones

In September 2020, it came to light that the Department of Homeland Security was "extracting information from protestors' phones" during the extended protests during Summer 2020 in Portland, Oregon.  Purportedly using a novel cell phone cloning method, the government was able to intercept communications to the phones of protestors.  While this is distrubing and likely illegal, the details of the attack remained classified.  However, we can try to infer likely methods of attack and likely protective practices.

If the cloning method requires a physical attack, most likely the compromised phones are those that were confiscated in prior arrests during the summer.  However, this limits the surveillance potential to only the phones of arrestees, and allows arrestees to either no longer trust their phones or to factory reset their phones to remove likely malware.

On the other hand, if the cloning method can be done remotely, this greatly expands the number of phones that might be compromised and no signaling event of such.

In either case, use of in-transit and end-to-end encryption would still protect phone communications (but perhaps not metadata), as you can learn about in the Chapter on [Protecting your Communications](3-3_comms.md).
	
#### What to learn next

* [Protecting your Communications](3-3_comms.md)
* [Protecting your Identity](3-5_apac.md)
	
#### External Resources

1. "How to Protect Yourself from the Snitch in Your Pocket", Earth First! The Journal of Ecological Resistance. Winter 2017-18.
1. [The Million Dollar Dissident NSO Group’s iPhone Zero-Days used against a UAE Human Rights Defender.](https://citizenlab.ca/2016/08/million-dollar-dissident-iphone-zero-day-nso-group-uae/)  Citizen Lab, August 2016.
1. [Criminalizing Dissent: Contested Evidence Introduced in J20 Trial Testimony](https://www.unicornriot.ninja/2017/criminalizing-dissent-contested-evidence-introduced-j20-trial-testimony/), Unicorn Riot. November 29, 2017.
1. [Phone Crackers](https://motherboard.vice.com/en_us/topic/phone-crackers), Motherboard. December 21, 2016 to present.
1. [Federal Agencies Tapped Protesters’ Phones in Portland](https://www.thenation.com/article/politics/homeland-security-portland/), The Nation, September 2020.
