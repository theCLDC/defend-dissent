## Protect your communications / data in the wild 

> We recommend that you read ???? before reading this section.



<!--transform this section into a case study: Signal.-->



#### What you'll learn

1. TODO

### What the infrastructure looks like

* tactical tech figure - https://holistic-security.tacticaltech.org/ckeditor_assets/pictures/25/content_datamotion.png
* phone communications also go through the same or similar networks

### What you can do

* secure communications
* strong passwords

### What you can't do

* protect meta-data (content vs. metadata?)
* trust ISPs

### What does this protect me from? Snoops, Wiretaps, Stingrays, Warrants, and Subpoenas

* you boss can snoop your communications over your work network
	* work or school email and file storage
    * web browsing history and unencrypted content
    * password capture
    * local network censorship
	* University monitoring of student email content?
* nazis can snoop your wifi connection
* cops can make wiretaps, but also access to cell network through vulnerabilities 
  * e.g. ss7 https://www.thedailybeast.com/you-can-spy-like-the-nsa-for-a-few-thousand-bucks
* cops and mercenaries can buy IMSI catchers
* cops can issue warrants
* anyone with a legal issue can issue a subpoena

### In context:

### Resources:

#### Network flows:

* holistic security:
    ** https://holistic-security.tacticaltech.org/chapters/explore/2-6-information-in-motion
    ** https://holistic-security.tacticaltech.org/ckeditor_assets/pictures/25/content_datamotion.png

#### Cell phones 

* level-up.cc/curriculum/mobile-safety/how-mobile-networks-work/
* http://level-up.cc/curriculum/mobile-safety/how-mobile-networks-work/activity-discussion/where-am-i/
* http://level-up.cc/curriculum/mobile-safety/how-mobile-networks-work/input/how-do-mobile-devices-work/
* https://www.accessnow.org/cms/assets/uploads/archive/docs/Protecting%20Your%20Security%20Online%20-%20A%20Practical%20Guide%20(design).pdf

#### Other things

https://tacticaltech.org/projects/flash-training-materials-2011/
https://tacticaltech.org/media/files/Flash%20cards%20%28A5%29.zip

https://securityinabox.org/en/guide/mobile-phones/
* Security in a box--some things horribly out of date but good to account for things here:
    ** https://securityinabox.org/en/guide/mobile-phones/
    ** https://securityinabox.org/en/guide/smartphones/



### (notes)

* Private messaging, voice and video communcations
** Use cases
** Apps: features and tradeoffs
** Tiers of Encryption

Tier 1 (top shelf, best possible security) uses truly end-to-end, Direct Encryption.  Private conversations can only be eavesdropped on by breaking into one of the participants' devices.  Wire and Signal meet this standard, and are also open source, so their security claims can be thoroughly verified.  If Zoom does this for 1-on-1 calls, as they claim, they could switch it off anytime--it's a setting that zoom customers/administrators can change via the administrator panel at zoom.us -- so a zoom employee could do the same thing.  This is a pretty terrible implementation of end-to-end encryption, so we don't count it as Direct Encryption, where  *only* you and your friends control encryption keys.

Tier 2 (less than ideal but still hard for some adversaries to break) is the sort of "in transit" encryption Zoom uses for group calls where comms are encrypted from participants' devices to Zoom's server, mixed, encrypted again then sent out to all participants' devices.  Breaking this would likely require Zoom's active co-operation, most likely obtained via a warrant or National Security Letter.

Tier 3 (not at all good, open to multiple adversaries including private security) is plain old cell phone encryption -- governments can relatively easily ask cell phone companies for access to their networks (and to break encryption done by the cell phone company) -- worse yet, cell site simulators ("Stingrays") can force phone network security down from 4G to 3G, weakening encryption enough for anyone with access to a Stingray to break (local cops, very probably corporate security).



