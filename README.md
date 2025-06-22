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



