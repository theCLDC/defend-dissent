## The data you keep with you: protect your devices

> We recommend that you read about [modern cryptography](modern-cryptography.md) and about what makes a good password [[link to section on properties of good passwords]] before reading this section.

#### What you'll learn

1. TODO

---

The amount of data you keep on your phone and laptop is staggering.  Contacts, emails, photos, documents, calendars, tax returns, banking details, and, in the case of a smartphone, often a detailed history of your location as long as you've had that phone.  Our contextual story below will give more details on the extent of the information that is kept on a typical smart phone.

A lot of this data you will also share with your various cloud storage providers (i.e. Apple, Google, DropBox), but that is the focus of [another chapter](comms.md). Here we focus on protecting the data that you keep with you, on your laptops and cell phones, from a remote or physical attack.

### Remote attacks

By a remote attack, we mean that an adversary would access the data on your phone or laptop through an internet or data connection.  There are companies that design and sell the ability to infect your device (usually focusing on smartphones) with malware that would allow their customer (your adversary, be it a corporate or state agent) to gain remote access to some or all of your information.

For example, Citizen Lab uncovered wide and varied use of the spyware Pegasus created and sold by an Israeli company, NSO Group.  Coupled with some social engineering to convince the target to click on a link, the spyware grants the ability to turn on and record from the phone's camera and microphone, record calls and text messages (even those providing end-to-end encryption), log GPS locations and send all this information back to the target's adversary. Citizen Lab reported that Pegasus attempts were made against Ahmed Mansoor, a human rights defender based in the UAE and 22 individuals in Mexico ranging from politicians campaigning against government corruption to scientists advocating for a state tax on sugary drinks.

#### What can I do?

Remote attacks, such as sold by NSO Group, rely on flaws in computer software known as zero-days. Such flaws are unknown to the software provider (e.g. Apple, Microsoft, or Google). Until they are known to the software provider (which happens on "day zero"), there is no chance that the software provider could have fixed or patched the vulnerability and so there is no chance that a victim could protect themself.  Computer security is often a cat-and-mouse game.  The products of malware and spyware creators (such as NSO Group) are only good so long as the targets (or more accurately, companies like Apple, Google and Microsoft) don't know about the malware being deployed.  As soon as they do, they fix their products so that the malware is no longer effective.

But these product fixes only work if the target (you) update your device.  So the lesson here is to **install all security updates as soon as they are available**.  Unfortunately, smartphones [[add info here about smartphone security support]].

Many malware products require phishing for installation on the target's device: convincing the target to click on a link or opening a file (either in an email or a text message).  So, the second thing you can do is be wary of what you click on.  Do you know the sender?  Are you expecting something from the sender?  Does anything seem, well, fishy?  In fact, it was vigilance that led Ahmed Mansoor to avoid spyware infection: he sent the phishing text along to Citizen Lab that led to their reporting on the abuse of spyware from NSO Group.

Finally, be wary of the apps you install and what permissions you grant them.  Does a flashlight app need access to your contacts and camera?  Do you really need to install that game created by an unknown software creator?  Every app you install is a potential vector for malware, so it is a good opportunity to practice minimalism.

### Physical attacks

By a physical attack, we mean that your adversary would first gain physical access to your device through loss, theft, or confiscation.


* https://motherboard.vice.com/en_us/topic/phone-crackers
* nazis can steal your device,
* the cops/border can take your device



#### What you I do?

* device encryption vs. screen lock
* strong passwords, fingerprints vs. password/phrase vs. pin no.
* privacy screen
* remote wipe?

### What you can't do

* build your own computer/phone
* trust devices 100%, supply chain manipulation


* What devices look like
** Is this useful?  maybe incorporate into what you can't do - to talk about closed source nature of cell phones in particular
** tactical tech cell phone layers
** compare to laptops/computers


### In context: 

* earth first j20 cell phone confiscation report


#### External Resources

[Citizen Lab reporting on abuse of NSO Group's Spyware](https://citizenlab.ca/2016/08/million-dollar-dissident-iphone-zero-day-nso-group-uae/)


#### Cell Phones

* Level-UP.cc narrative of mobile device network and components:
    ** https://level-up.cc/curriculum/mobile-safety/how-mobile-networks-work/input/how-do-mobile-devices-work/
* Tactical Tech (me and my shadow) - mobile device layers diagram:
    ** https://myshadow.org/ckeditor_assets/attachments/94/mobile_breakdowna5.pdf
* Security in a box--some things horribly out of date but good to account for things here:
    ** https://securityinabox.org/en/guide/mobile-phones/
    ** https://securityinabox.org/en/guide/smartphones/

#### Data Protection

* Level-UP.cc training modules on PASSWORDS and BACKUPS:
** http://level-up.cc/curriculum/protecting-data/

#### Malware Protection
