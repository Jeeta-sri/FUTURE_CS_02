# 🔐 Phishing Email Detection & Awareness System

## 📌 Project Overview

This project presents a structured phishing email detection and threat analysis assessment conducted using simulated email headers and public verification tools.

Three email headers were analyzed:

1. SBI Security Alert (Spoofed Domain)
2. Amazon Password Reset (Display Name Spoofing – “amaz0n”)
3. GitHub Login Alert (Legitimate Email)

The objective was to identify phishing indicators using technical authentication analysis and domain verification methods, classify emails based on risk, and provide business-focused awareness recommendations.

---

## 🎯 Objectives

- Detect phishing indicators in email headers
- Analyze SPF, DKIM, and DMARC authentication results
- Perform domain legitimacy verification
- Classify emails as Safe / Suspicious / Phishing
- Translate technical findings into business-friendly explanations
- Provide user awareness and prevention guidelines

---

## 🛠 Tools Used

- MXToolbox (Email Header Analyzer)
- WHOIS Lookup (Domain Registration Verification)
- Dupli Checker (Domain Age Detection)
- Browser Developer Tools
- GitHub (Documentation & Version Control)

---

## 🧪 Methodology

The analysis followed a layered approach:

1. Extracted full email headers.
2. Uploaded headers to MXToolbox for authentication analysis.
3. Verified SPF, DKIM, and DMARC results.
4. Checked sender IP reputation.
5. Conducted WHOIS lookup to verify domain registration details.
6. Used Dupli Checker to determine domain age.
7. Compared display name vs actual return-path domain.
8. Classified each email based on technical and contextual indicators.

---

# 🔎 Detailed Email Header Analysis

---

## 🔴 Case 1: SBI Security Alert (Spoofed Domain)

### Header Observations

- SPF: Fail
- DKIM: None
- DMARC: Fail
- Sending IP not authorized
- Domain: sbi-secureverify-login.com

### WHOIS & Domain Age Findings

- Recently registered domain
- Not associated with official SBI domain
- Suspicious naming pattern (extra words: secure, verify, login)

### Risk Indicators

- Authentication failure
- Lookalike domain impersonation
- Generic subject with urgency
- Brand spoofing attempt

### Classification

🔴 Phishing

### Business Risk

Users may submit banking credentials to attacker-controlled website, leading to financial fraud.

---

## 🔴 Case 2: Amazon Password Reset (Display Name Spoofing)

### Header Observations

- From: Amazon Support <support@amazon.com>
- Return-Path: noreply@amaz0n-security-update.com
- SPF: Softfail
- DKIM: None
- DMARC: Fail
- Hosting server located in suspicious region

### WHOIS & Domain Age Findings

- Domain: amaz0n-security-update.com
- Recently registered
- Typographical impersonation (“0” instead of “o”)

### Risk Indicators

- Display name spoofing
- Domain typosquatting
- Authentication failure
- Credential harvesting attempt

### Classification

🔴 Phishing

### Business Risk

High probability of credential theft and account compromise.

---

## 🟢 Case 3: GitHub Login Alert (Legitimate Email)

### Header Observations

- SPF: Pass
- DKIM: Pass
- DMARC: Pass
- Sending IP matches authorized GitHub mail servers
- Domain: github.com

### WHOIS & Domain Age Findings

- Established domain
- Registered long ago
- Verified organization ownership

### Risk Indicators

- No domain mismatch
- No spoofing
- Valid digital signature

### Classification

🟢 Safe

### Business Impact

Legitimate security notification.

---

# 📊 Risk Classification Summary

| Email Case | Authentication Result | Domain Age | Classification |
|------------|----------------------|------------|----------------|
| SBI Alert | SPF Fail / DMARC Fail | Recently Registered | 🔴 Phishing |
| Amaz0n Reset | SPF Softfail / DMARC Fail | Recently Registered | 🔴 Phishing |
| GitHub Alert | SPF Pass / DKIM Pass / DMARC Pass | Established | 🟢 Safe |

---

# 🛡 Phishing Techniques Identified

- Domain impersonation (Typosquatting)
- Display name spoofing
- Authentication bypass attempts
- Social engineering (Urgency)
- Credential harvesting setup

---

# 🏢 Business Risk Impact

If such emails are not detected:

- Financial fraud may occur
- User credentials can be compromised
- Sensitive corporate data may be exposed
- Organizational reputation may suffer
- Regulatory compliance risks may increase

---

# 🛠 Prevention & Awareness Guidelines

## For Individuals

- Verify full sender email address (not just display name)
- Avoid clicking urgent links
- Inspect domain spelling carefully
- Check for HTTPS
- Report suspicious emails immediately

## For Organizations

- Enforce SPF, DKIM, and DMARC policies (p=reject recommended)
- Implement email filtering gateways
- Conduct phishing simulation training
- Monitor domain impersonation attempts
- Enable Multi-Factor Authentication (MFA)

---

# 📈 Skills Demonstrated

- Email header analysis
- SPF, DKIM, DMARC validation
- Domain impersonation detection
- WHOIS & domain age verification
- Risk classification
- Security awareness documentation
- Business-focused cybersecurity reporting

---

# ⚖ Ethical Disclaimer

All analyzed email headers were simulated for educational purposes.

No real accounts, organizations, or production systems were targeted.

This project was conducted strictly for cybersecurity learning and awareness development.

---

# 🚀 Conclusion

The analysis demonstrates how combining technical authentication checks with domain verification significantly improves phishing detection accuracy.

Strong email security controls, combined with user awareness training, form a critical defense against phishing-based cyber threats.

---

## 👤 Author

Srijeeta Dutta,
Cybersecurity Enthusiast

