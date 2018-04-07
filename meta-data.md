## Metadata

#### What you'll learn

1. What metadata is.
1. What metadata can reveal.
1. Why metadata is difficult to protect.

### What is metadata?

Metadata is all the information *about* the data, but not the data itself and is best illustrated with a few examples.
* For a phone call, the metadata will include the phone numbers involved, the start time of the call, the length of the call. For cell-phone calls, the metadata will likely include the location of your phone (the GPS coordinates), the cell-tower that you are connected to, and even the type of phone you are using.  Metadata of phone calls would not include the audio transmission itself - this would be the "data".  The original historical use of being recorded for phone calls is for the purposes of billing. 
* Most modern digital photographs include information about the time and place the photo was taken, the type of camera used and its settings.  In this case, the photo itself is the data.  Many websites, such as Facebook, Twitter and Instagram, remove this metadata, for your privacy, when you upload a photo or video.  Others do not, such as Google, Flickr and YouTube.
* Almost all modern color printers, at the request of the US government to printer manufacturers over fears of their use in money counterfeiting, print a forensic code on each page that may be visible or not.  In this case, the printed sheet (less the forensic code) would be the data, and the information encoded by the forensic code would be the metadata. The forensic code, which may or may not be visible to the human eye, has been known to include the day and time the sheet was printed and the serial number of the printer used.

The first disclosure by Edward Snowden revealed that the NSA was collecting all the metadata of calls made by Verizon customers, forcing a conversation about metadata into the public consciousness. A debate on what privacy was being invaded by this practice ensued.  Earlier that year, the Associated Press fought back against the collection of metadata obtained by subpoena from the Justice Department, saying "These records potentially reveal communications with confidential sources across all of the newsgathering activities undertaken by the AP during a two-month period, provide a road map to AP's newsgathering operations, and disclose information about AP's activities and operations that the government has no conceivable right to know." A court opinion noted that the collection of GPS data through such metadata collection "can deduce whether he is a weekly churchgoer, a heavy drinker, a regular at the gym, an unfaithful husband, an outpatient receiving medical treatment, an associate of particular individuals or political groups."

The NSA has referred to, in an internal document, as metadata being one of the agency's "most useful tools."

### Metadata and the Internet

When you visit a website, information is being sent between your computer and the server of the website through the Internet. At a basic level, a message is sent from your computer to the server requesting the contents of the website and then the contents of the website are sent from the server to your computer.  The information being sent over the Internet is often referred to as *traffic*, and any message being sent will actually be broken up into many shorter messages or *packets*. Each packet has three main parts:
* The **header** includes the Internet address of the sender and the receiver (e.g. your computer and the website's server) and a description of the type of data that is being sent (e.g. html).
* The **data** is the content of the message (e.g. the content of the webpage, or part of the webpage).
* The **trailer**  indicates end of packet and provides proof that the packet has not been corrupted in transit (using a hash function, which we describe in [Cryptographic Hash Functions](cryptographic-hash.md)).

The metadata is composed of the header and the trailer.  The header is difficult to protect or conceal because it indicates where a packet should be sent.  Just like sending a letter, an address is needed for delivery.  Your Internet address, or IP address, is related to your physical location; in fact, often your physical location can be determined from you IP address.

This description applies to any information that is sent over the Internet: email, video streaming, VOIP calls, and instant messages included.

### In context: Protecting a Whistleblower

In May 2017, Reality Winner disclosed NSA documents reporting on Russian interference in the 2016 US presidential election.  Her arrest, days before the story was published, prompted much speculation around how she was so quickly identified as the whistleblower, with many people pointing the blame at The Intercept for their handling of the story.  Reality Winner had anonymously mailed a color printout of the documents to The Intercept.  In standard journalistic fashion, The Intercept sent a photograph of the documents to the NSA for verification.  The same photograph was redacted and made public in their reporting.  Shortly after the publication of the story, several people pointed out that printer forensic code was visible in the photo and determined the day and time the document was printed and the serial number of the printer.  While it is possible that the FBI could have identified Reality Winner from this information (and The Intercept could have redacted the forensic code from the photo), it is probably more likely she was outed by logs of file accesses on her work computer.

#### What to learn next

* HTTPS?
* How to conceal your Internet traffic metadata using a [Virtual Private Network or Tor](anonymous-routing.md). NOTE THIS REQUIRES UNDERSTANDING MODERN CRYPTOGRAPHY AND OTHER TOPICS FIRST ...


#### External resources

1. [AP blasts feds for phone records search](http://www.cnn.com/2013/05/13/us/justice-ap-phones) CNN. May 14 2013. Accessed January 11, 2018.
1. [Justice Department Subpoena of AP Journalists Shows Need to Protect Calling Records](https://www.eff.org/deeplinks/2013/05/doj-subpoena-ap-journalists-shows-need-protect-calling-records) Electronic Frontier Foundation. May 13, 2013. Accessed January 11, 2018.
1. [Secret Code in Color Printers Lets Government Track You](https://www.eff.org/press/archives/2005/10/16) Electronic Frontier Foundation. October 16, 2005. Accessed January 11, 2018.
1. [DocuColor Tracking Dot Decoding Guide](https://w2.eff.org/Privacy/printers/docucolor/index.php) Electronic Frontier Foundation. Accessed January 11, 2018.
1. [The Rewards of Metadata](https://theintercept.com/snowden-sidtoday/3232989-the-rewards-of-metadata/) Snowden Archive -- The SIDtoday files. January 23, 2004. The Intercept. Accessed January 11, 2018.
1. [The Metadata Program in Eleven Documents](https://www.newyorker.com/news/daily-comment/the-metadata-program-in-eleven-documents) The New Yorker.  December 31, 2013. Accessed January 11, 2018.
1. [Top-Secret NSA Report Details Russian Hacking Effort Days Before 2016 Election](https://theintercept.com/2017/06/05/top-secret-nsa-report-details-russian-hacking-effort-days-before-2016-election/) The Intercept. June 5, 2017. Accessed January 11, 2018.
1. [The Mysterious Printer Code That Could Have Led the FBI to Reality Winner](https://www.theatlantic.com/technology/archive/2017/06/the-mysterious-printer-code-that-could-have-led-the-fbi-to-reality-winner/529350/
)  The Atlantic.  June 6, 2017. Accessed January 11, 2018.