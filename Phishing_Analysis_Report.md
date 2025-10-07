
# Phishing Email Analysis Report

## 1. Overview

- **Date of Analysis:** 2025-10-07
- **Analyst:** SELF 
- **Objective:** To identify and document phishing characteristics in a sample email.
- **File Analyzed:** `sample-phishing-email.eml`

---

## 2. Email Header Analysis

An analysis of the email headers reveals several discrepancies that point to a phishing attempt.

- **`Return-Path` Mismatch:** The `Return-Path` is `<bounce-12345@suspicious-server.net>`, which does not match the sender's domain (`paypa1.com`). This indicates that replies and bounces are being sent to a different, unrelated server.
- **`Received` Header:** The email was received from `mail-server.suspicious-server.net` with an IP address of `198.51.100.123`. This is not an official PayPal mail server. A legitimate email would originate from servers owned by PayPal.

---

## 3. Body and Content Analysis

The body of the email contains numerous classic phishing indicators.

| Phishing Indicator | Description |
| :--- | :--- |
| **1. Spoofed Sender Address** | The sender's email is `support@paypa1.com`. The domain uses the number `1` instead of the letter `l` (`paypa**1**` vs. `paypa**l**`). This is a common technique called "typosquatting" to deceive recipients. |
| **2. Urgent/Threatening Language** | The email uses phrases like "Urgent," "Action Required," "temporarily limited access," and threatens "permanent account suspension." This creates a sense of panic to rush the user into action without thinking. |
| **3. Mismatched URL / Deceptive Link** | The visible link text is `https://www.paypal.com/us/signin`, which appears legitimate. However, hovering over the link (or inspecting the HTML) reveals the actual destination URL is `http://paypal-security-update.ga/login`. This malicious URL is designed to look like a real PayPal page but is hosted on a completely different domain (`.ga` is the country code for Gabon). |
| **4. Spelling and Grammar Errors** | There is a spelling mistake in the closing: "Sincerly," instead of "Sincerely." While minor, professional companies like PayPal rarely make such errors in automated emails. |
| **5. Generic Salutation** | The email begins with "Dear Valued Customer," instead of using the recipient's actual name. Legitimate services typically personalize their communications. |
| **6. Request for Credentials** | The ultimate goal of the email is to get the user to click a link and enter their login credentials on a fake page, thereby stealing them. |

---

## 4. Summary of Findings

The email sample displays multiple definitive signs of a phishing attack. Key indicators include a spoofed sender address, discrepancies in the email headers, the use of urgent and threatening language, and a deceptive link pointing to a malicious website. The combination of these elements confirms that this email is a fraudulent attempt to steal user credentials.

## 5. Conclusion

This analysis demonstrates the importance of scrutinizing suspicious emails. Users should be trained to look for these red flags before clicking any links or providing personal information.
