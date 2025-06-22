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

---

## Question 9

**What corporation owns the sender's IP address?**

The Whois results will list the ASN/organization.

<img src="https://i.imgur.com/SylIjin.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
MICROSOFT

---

## Question 10

**What was the result of the SPF check?**

Find the Received-SPF: header for the sender domain.

<img src="https://i.imgur.com/mA742S7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
Pass

---

## Question 11

**What is the full SPF record of the sender's domain?**

Use this command in a terminal to query DNS TXT records:
``nslookup -type=txt social.helwan.edu.eg | grep -i spf``

<img src="https://i.imgur.com/yVmzf6r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<img src="https://i.imgur.com/ZizYX0m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
``v=spf1 include:spf.protection.outlook.com -all``

---

## Question 12

**What is the email's Message-ID?**

Locate the Message-ID: header in the file.

<img src="https://i.imgur.com/jX3aQje.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
JMrByPl2c3HBo8SctKnJ5C5Gp64sPSSWk76p4sjQ@s6

---

## Question 13

**What type of encoding was used to transfer the email body content?**

Look for the Content-Transfer-Encoding: header.

<img src="https://i.imgur.com/zIAZ8BJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
base64

---

## Question 14

**In defanged format, what is the second URL extracted from the email?**

1. Copy the Base64-encoded content from the email body.

   <img src="https://i.imgur.com/1G0262u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

2. Go to [CyberChef](https://gchq.github.io/CyberChef/).

<img src="https://i.imgur.com/QjNbJyE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

3. Use the following operations:

``From Base64``

``Extract URLs``

``Defang URL``

<img src="https://i.imgur.com/I1rAHx7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
hxxps[://]0[.]232[.]205[.]92[.]host[.]secureserver[.]net/lclbluewin08812/

---

## Question 15

**Perform a VirusTotal scan on the URL. What verdict did Fortinet assign to it?**

1. Decode and copy the URL from CyberChef.


2. Visit [VirusTotal](https://www.virustotal.com/gui/home/upload).

<img src="https://i.imgur.com/jr5n7DG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

3. Submit the URL for analysis.


4. Look for Fortinet in the list of security vendors

<img src="https://i.imgur.com/4pZlDcD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Answer:</b>
Phishing

---
