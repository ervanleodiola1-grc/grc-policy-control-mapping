# Company Profile: MedTech Innovations, Inc.

**Document ID:** DOC-SEC-001  
**Version:** 1.0  
**Effective Date:** October 24, 2026  
**Classification:** Internal / Portfolio Documentation  

---

## 1. Executive Summary
MedTech Innovations, Inc. is a fast-growing, mid-sized healthcare technology startup delivering a SaaS-based remote patient monitoring (RPM) platform. The platform ingests real-time biometric data from wearable medical devices and transmits it securely to hospital networks and clinical care teams. 

Because the platform processes Protected Health Information (PHI) and Personally Identifiable Information (PII) for over 150,000 active patients across North America, maintaining strict data confidentiality, integrity, and availability is vital to the business.

---

## 2. Business & Operational Context

| Attribute | Details |
| :--- | :--- |
| **Industry** | Health Technology / Cloud SaaS |
| **Headquarters** | Austin, Texas (Fully Remote Workforce) |
| **Employee Count** | ~50 full-time employees, 10 third-party contractors |
| **Primary Customers** | Regional hospital networks, private cardiology clinics, care management groups |
| **Key Service** | Cloud-based Patient Data Dashboard & Alerting System |

---

## 3. Regulatory & Compliance Requirements

MedTech Innovations must comply with a combination of statutory regulations and industry security frameworks:

1. **HIPAA / HITECH Act:** Mandates administrative, physical, and technical safeguards for Protected Health Information (PHI) under the HIPAA Security Rule (45 CFR Part 160 and Part 164, Subparts A and C).
2. **NIST CSF v2.0:** Serves as the primary operational cybersecurity framework for managing and reducing cybersecurity risk across five core functions (Govern, Identify, Protect, Detect, Respond, Recover).
3. **ISO/IEC 27001:2022:** Forms the baseline for the company’s Information Security Management System (ISMS) to support customer vendor risk assessments and SOC 2 Type II audits.

---

## 4. Technical Architecture & Tech Stack

```text
  [ Wearable Devices ] ──(TLS 1.3)──> [ AWS API Gateway ]
                                              │
                                     [ AWS EC2 / EKS ]
                                              │
                       ┌──────────────────────┴──────────────────────┐
                       ▼                                             ▼
             [ AWS S3 Bucket ]                              [ PostgreSQL Database ]
             (Encrypted Patient Logs)                       (Encrypted PHI Records)
