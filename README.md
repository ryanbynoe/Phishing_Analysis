<h1>Phishing Analysis</h1>

 

<h2>Description</h2>
Project consists of analyzing a malicious email which is impersonating Walmart. I walkthrough my thought process and how we can see the attachment without placing potential harm to my system.
<br />


<h2>Languages and Utilities Used</h2>

- <b>URL2PNG</b>
- <b>Virtual Box</b>
- <b>VirusTotal</b>
- <b>WHOIS</b>





<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Malicious Email: <br/>
<img src="https://i.imgur.com/qF94OFb.png" height="80%" width="80%" alt="Malicious Email"/>
<br />
<br />
First part of my phishing analysis was opening up a virtual box and booting up the good ol' virtual machine of Windows 10. I will be downloading the email and just in case of any accidents occurring, It will burn the virtual machine instead of my OS.

Now I am putting on my Analyzing glasses and viewing the email at hand. What do I notice?

Let's take a look at the Subject line: “You have Won a Vikings Knife Set: CustomerID: 809325. The sender of the email is trying to grasp the attention of the recipient by saying I have won a prize. One red flag I noticed is the the “T” in customer is capitalized. An ID number is also provided in the subject line. 

The Contact name says Walmart but the sender address is completely different from the contact name and looks bizarre. 

The Email date it was sent was 02/20/23 at 12:28 PM and the email contains a Hyperlink titled “Please confirm receipt”
 <br/>
<br />
<br />
Artifacts:
Subject Line = You Have Won a Viking Knife Set CusTomerlD:.809325
Sending Address = contact@exqngva.mpdlorjr.com
Date + Time = Monday 2/20/23 12:28 PM
Sending Server IP =  45.144.154.199
Recipients = rellowa1@live.com
URL =  http://exqngva.mpdlorjr[.]com/rd/c5644UduTZ697224HpDt20539Emi36NYnA172
Attachments = None
WHOIS Analysis: Performing a WHOIS search shows that the domain was registered about 8 years ago December 08, 2015.

VirusTotal Reputation: Searched full URL and 1 security vendor Seclookup flagged the URL as being malicious. 

URL2PNG: Using URL2PNG to view the link destination showed that the site was telling the use to complete the survey in order to win the offer prize. Possibly a credential harvester. Webpage is using Walmart like logos.

Report:

The sending address exqngva.mpdlorjr.com isn’t one of the well known addresses such as Gmail or outlook. We may be able to block sending server IP and not cause a negative impact. Blocking the sender may also be appropriate because it is not a legitimate email and will stop further malicious email from being delivered.


Next I opened the email I downloaded into notepad just to view some more details around the email. I used shortcut CTRL +F and searched for “IP” to find the sender IP address:
<br/>
<img src="https://i.imgur.com/Ijz2R2E.png" height="80%" width="80%" alt="Report"/>
<br />
<br />
After locating the Sender IP, I went to Whois.com to gather more details around the Senders IP address:  <br/>
<img src="https://i.imgur.com/h1U3KGl.png" height="80%" width="80%" alt="WHOIS"/>
<br />
<br />
The host mailing address is rdns.sterly.com.tr:  <br/>
<img src="https://i.imgur.com/p6W2ZT6.png" height="80%" width="80%" alt="Resolve Host/ Host mailing address"/>
<br />
<br />
Used URL2PNG to view the webpage: <br/>
<img src="https://i.imgur.com/iqov7NE.png" height="80%" width="80%" alt="URL2PNG"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
