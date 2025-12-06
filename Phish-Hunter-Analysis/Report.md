
📝 Phish Hunter — Email Threat Investigation Summary

Analyst: Shaik Shebeervali
Target Role: SOC Analyst – Level 1
Contact: shebeervalishaik@gmail.com

Platform: TryHackMe — Phish Hunter Challenge
Report Type: Learning-Based Email Investigation

🧾 1. Executive Summary

This report documents a phishing investigation involving a suspicious email containing a malicious attachment and a deceptive link. The goal was to identify sender spoofing, inspect malicious objects, extract IOCs, and determine the level of risk.

The investigation used industry-standard analysis tools to review both artifacts and email metadata, resulting in a confirmed phishing attack attempting credential theft and malware delivery.

🛠️ 2. Tools Used
Tool	Purpose
VirusTotal	File/URL Reputation
URLScan.io	URL Redirection & Risk
CyberChef	Decode/Deobfuscate Payload
Email Header Analyzer	Sender/Source Metadata
Sandbox Tools	Malware Behavior
🕵️ 3. Observations & Findings

The email impersonated a trusted service using a typosquatted domain.

The sender IP reputation was flagged as malicious during lookup.

The attachment contained obfuscated code that downloads additional payloads.

The embedded URL redirected to a credential phishing page.

The message attempted to force urgency with social engineering (“urgent invoice”).

📌 4. Indicators of Compromise (Generalized)
IOC Type	Example (Generalized)
Sender Domain	secure-support-billing.com
Sender Email	invoice@billing-secure.com
Malicious URL	hxxp://login-verify-update[.]com
File Hash (Attachment)	<obfuscated malware hash>
Sender IP	X.X.X.X (poor reputation score)
🛰️ 5. MITRE ATT&CK Mapping
Technique ID	Technique	Context
T1566.001	Spearphishing Attachment	Malicious invoice attachment
T1566.002	Spearphishing Link	Credential phishing URL
T1059	Script Execution	Obfuscated JS/VBA code
T1589	Credential Access	Targeting user login credentials
🛡️ 6. SOC Response & Prevention Recommendations

✔ Quarantine email for affected user(s)
✔ Block sender domain and IP in email gateway
✔ Deploy SPF, DKIM, and DMARC enforcement
✔ Block malicious hash and domain in EDR/SIEM
✔ Conduct phishing awareness training for employees
✔ Implement MFA to reduce credential theft impact

📌 Conclusion

The email was successfully attributed as a phishing campaign designed to steal user credentials and potentially execute malicious code. This investigation reinforces core SOC skills such as email forensics, threat intelligence lookup, IOC extraction, and user protection strategies.

Prepared By:
Shaik Shebeervali
📧 shebeervalishaik@gmail.com

🎯 Aspiring SOC Analyst
