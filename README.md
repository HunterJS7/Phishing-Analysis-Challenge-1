# Phishing-Analysis-Challenge-1

# Phishing Email Analysis – Challenge Walkthrough

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

