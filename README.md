Objective:

Analyze a phishing email sample (job scam email) to identify phishing indicators such as fake sender domains, urgent/scam language, suspicious links, and header mismatches using tools like MXToolbox Email Header Analyzer.
Sample Phishing Email Analyzed:
Subject: Urgent: Applicants Needed
From: Listings@in.jbe.best-jobs-online.com

Best-Jobs-Online
Late night stocker
Cashier
Police Records Specialist
Appointment Setter
... (multiple random job listings with salary details)
Unsubscribe

Analysis Steps and Findings:
1. Sender Address Check (Spoofing Test)
Appears As: Listings@in.jbe.best-jobs-online.com
Risk: The domain is not a verified job portal (like Naukri, LinkedIn, Indeed).
Observation: Likely a disposable/scam domain to send mass phishing emails.
2. Link Verification (Hover Over Links)
The email contains multiple "View Details" links.
Hovering over these links shows suspicious URLs, not pointing to any official company website.
Likely to redirect to fake websites designed to collect personal data.
3. Language and Urgency Tactics
Subject line: "Urgent: Applicants Needed" — Creates panic to make recipients click quickly.
Lists random job roles with attractive salary figures without any company details.
4. Generic Greeting
Email is sent "to me" — does not address the recipient by name.
5. Unverified Job Listings
The job listings are very generic with unrealistic pay rates.
No company names, job descriptions, or verification links.

### Email Header Analysis (MXToolbox Results)

| Check                     | Result     | Interpretation                               |
|---------------------------|------------|----------------------------------------------|
| DMARC Compliance           | Failed     | Possible spoofing detected                   |
| SPF Alignment              | Passed     | SPF record aligns with sender domain         |
| SPF Authentication         | Passed     | IP authorized to send emails for domain      |
| DKIM Alignment             | Passed     | Domain alignment correct                     |
| DKIM Authentication        | Failed     | Digital signature invalid (forged/spoofed)   |
| Received Delay             | 22 seconds | Slight delay — not a major phishing sign     |

Even though SPF checks passed, the DMARC failed, and DKIM failed.
DMARC failure indicates that the domain owner has set anti-spoofing policies, but the email did not pass them.
DKIM failure suggests the email's digital signature is invalid — a common indicator of email forgery/spoofing.
This confirms the email is suspicious and potentially a phishing attempt.

Key Learnings:
Identified phishing patterns in job scam emails.
Understood how to verify sender authenticity using email headers.
Learned to spot urgency tactics and fake job offers in phishing attempts.





