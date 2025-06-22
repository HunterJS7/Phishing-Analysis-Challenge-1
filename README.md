# Phishing-Analysis-Challenge-1

<h1>Instructions:</h1>

You are a SOC Analyst at Mighty Solutions, Inc. An account executive, Dana Derringer, noticed a warning email in her inbox claiming her online access has been disabled. However, she noticed this was odd as she is still able to access her online business platforms and inbox. She decided to forward the email in question to the security team's phishing mailbox for review.

Using what you've learned within this domain, perform a detailed email analysis on the <b>challenge1.eml</b> file to answer the report questions below.

**Challenge File:**  
`01_Phishing_Analysis/Challenges/challenge1.eml`

---

## Question 1

**What is the full date and time of the email delivery?**

To answer this, begin by opening the `.eml` file in **Thunderbird**. While Thunderbird shows the date/time in the GUI, we need to confirm the raw header value.

<img src="https://i.imgur.com/8b1BVLM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


Instead, open the email in **Sublime Text**:

   <img src="https://i.imgur.com/cVqc35W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

``subl challenge1.eml
Scroll down to the Date: header to find the precise timestamp.``

<img src="https://i.imgur.com/5CPmXPd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

 <img src="https://i.imgur.com/gd7hzkB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
Tue, 31 Oct 2023 10:10:04 -0900

---

## Question 2

**What is the subject of the email?**

Look for the Subject: header in the email file.

 <img src="https://i.imgur.com/7nX54wU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


<b>Answer:</b>
Your account has been flagged for unusual activity

---

## Question 3

**Who was the email sent to?**

Find the To: header in the .eml file.

<img src="https://i.imgur.com/yZbTGRA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
dderringer@mighty-solutions.net

---

## Question 4

**Based on the sender's display name, who does the email claim to be from?**

Locate the From: header. The display name precedes the actual email address.

<img src="https://i.imgur.com/i9imOd3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
Outlook Support Team

---

## Question 5

**What is the sender's email address?**

Also found in the From: header.

<img src="https://i.imgur.com/w0xOxVr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
social201511138@social.helwan.edu.eg

---

## Question 6

**What email address is used for receiving bounced emails?**

Check the Return-Path: header, which specifies the address for bounce handling.

<img src="https://i.imgur.com/vl5Wa0I.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
social201511138@social.helwan.edu.eg

---

## Question 7

**What is the IP address of the sender's email server?**

Look for the X-Sender-IP: header.

<img src="https://i.imgur.com/bSWCWeC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
40.107.22.60

---

## Question 8

**What is the resolved hostname of the sender's IP address?**

Use a tool like [DomainTools Whois Lookup](https://whois.domaintools.com/) to resolve the IP.

<img src="https://i.imgur.com/tJdA2Md.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<img src="https://i.imgur.com/kaAai4c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
mail-am6eur05on2060.outbound.protection.outlook.com
