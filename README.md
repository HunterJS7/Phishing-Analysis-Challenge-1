# Phishing-Analysis-Challenge-1

# Phishing Email Analysis – Challenge Walkthrough

**Challenge File:**  
`01_Phishing_Analysis/Challenges/challenge1.eml`

---

## Question 1

**What is the full date and time of the email delivery?**

To answer this, begin by opening the `.eml` file in **Thunderbird**. While Thunderbird shows the date/time in the GUI, we need to confirm the raw header value.

Instead, open the email in **Sublime Text**:


``subl challenge1.eml
Scroll down to the Date: header to find the precise timestamp.``

Answer:

yaml
Copy
Edit
Tue, 31 Oct 2023 10:10:04 -0900

