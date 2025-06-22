# Phishing-Analysis-Challenge-1


# Phishing Email Analysis – Challenge Walkthrough

**Challenge File:**  
`01_Phishing_Analysis/Challenges/challenge1.eml`

---

## Question 1

**What is the full date and time of the email delivery?**

To answer this, begin by opening the `.eml` file in **Thunderbird**. While Thunderbird shows the date/time in the GUI, we need to confirm the raw header value.

Instead, open the email in **Sublime Text**:

```bash
subl challenge1.eml
Scroll down to the Date: header to find the precise timestamp.

Answer:

yaml
Copy
Edit
Tue, 31 Oct 2023 10:10:04 -0900
Question 2
What is the subject of the email?

Look for the Subject: header in the email file.

Answer:

rust
Copy
Edit
Your account has been flagged for unusual activity
Question 3
Who was the email sent to?

Find the To: header in the .eml file.

Answer:

css
Copy
Edit
dderringer@mighty-solutions.net
Question 4
Based on the sender's display name, who does the email claim to be from?

Locate the From: header. The display name precedes the actual email address.

Answer:

nginx
Copy
Edit
Outlook Support Team
Question 5
What is the sender's email address?

Also found in the From: header.

Answer:

css
Copy
Edit
social201511138@social.helwan.edu.eg
Question 6
What email address is used for receiving bounced emails?

Check the Return-Path: header, which specifies the address for bounce handling.

Answer:

css
Copy
Edit
social201511138@social.helwan.edu.eg
Question 7
What is the IP address of the sender's email server?

Look for the X-Sender-IP: header.

Answer:

Copy
Edit
40.107.22.60
Question 8
What is the resolved hostname of the sender's IP address?

Use a tool like DomainTools Whois Lookup to resolve the IP.

Answer:

Copy
Edit
mail-am6eur05on2060.outbound.protection.outlook.com
Question 9
What corporation owns the sender's IP address?

The Whois results will list the ASN/organization.

Answer:

nginx
Copy
Edit
MICROSOFT
Question 10
What was the result of the SPF check?

Find the Received-SPF: header for the sender domain.

Answer:

nginx
Copy
Edit
Pass
Question 11
What is the full SPF record of the sender's domain?

Use this command in a terminal to query DNS TXT records:

bash
Copy
Edit
nslookup -type=txt social.helwan.edu.eg | grep -i spf
Answer:

ini
Copy
Edit
v=spf1 include:spf.protection.outlook.com -all
Question 12
What is the email's Message-ID?

Locate the Message-ID: header in the file.

Answer:

css
Copy
Edit
JMrByPl2c3HBo8SctKnJ5C5Gp64sPSSWk76p4sjQ@s6
Question 13
What type of encoding was used to transfer the email body content?

Look for the Content-Transfer-Encoding: header.

Answer:

bash
Copy
Edit
base64
Question 14
In defanged format, what is the second URL extracted from the email?

Copy the Base64-encoded content from the email body.

Go to CyberChef.

Use the following operations:

From Base64

Extract URLs

Defang URL

Answer:

css
Copy
Edit
hxxps[://]0[.]232[.]205[.]92[.]host[.]secureserver[.]net/lclbluewin08812/
Question 15
Perform a VirusTotal scan on the URL. What verdict did Fortinet assign to it?

Decode and copy the URL from CyberChef.

Visit VirusTotal.

Submit the URL for analysis.

Look for Fortinet in the list of security vendors.

Answer:

nginx
Copy
Edit
Phishing
Question 16
[Yes or No] - After your analysis, is this email genuine?

Answer:

yaml
Copy
Edit
No
📝 Acknowledgement
Thanks to TCM Security for providing this hands-on phishing lab challenge.
For more training and content, visit: https://academy.tcm-sec.com
