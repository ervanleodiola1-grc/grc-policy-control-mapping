# Compliance Gap Analysis & Remediation Plan

**Document ID:** GAP-SEC-003  
**Version:** 1.0  
**Effective Date:** October 24, 2026  
**Owner:** Information Security & Compliance  
**Target Audience:** Executive Leadership, Engineering Leads, IT Operations  

---

## 1. Executive Summary
Following the release of the **Access Control Policy (POL-SEC-002)**, an internal baseline assessment was conducted to evaluate MedTech Innovations' current technical posture against mandatory controls. 

While core safeguards (such as Okta MFA and enterprise SSO) are operational, **three key compliance gaps** were identified that expose the organization to security risks and audit findings under HIPAA and ISO 27001. This document details those gaps, assigns risk ratings, and defines actionable remediation plans with strict completion timelines.

---

## 2. Identified Compliance Gaps & Risk Matrix

| Gap ID | Description | Primary Framework Standard | Baseline Risk Rating | Target Completion |
| :--- | :--- | :--- | :--- | :--- |
| **GAP-01** | Manual Offboarding Process for Third-Party Contractors | NIST CSF `PR.AA-06`<br>ISO 27001 `A.5.18` | **HIGH** | 30 Days |
| **GAP-02** | Absence of Centralized Privileged Access Management (PAM) | NIST CSF `PR.AA-05`<br>ISO 27001 `A.8.2` | **HIGH** | 60 Days |
| **GAP-03** | Informal & Unautomated Quarterly Access Reviews | NIST CSF `DE.CM-01`<br>HIPAA `164.308(a)(1)` | **MEDIUM** | 45 Days |

---

## 3. Detailed Gap Breakdowns & Remediation Action Plans

### GAP-01: Manual Offboarding Process for Third-Party Contractors
* **Current State:** Offboarding for contractors relies on manual email notifications from HR to IT. Consequently, contractor access to secondary systems (e.g., GitHub, AWS staging) has occasionally remained active for up to 72 hours post-termination.
* **Impact:** Involuntary terminations could allow former contractors to extract proprietary source code or access sensitive testing environments containing simulated PHI.
* **Corrective Action Plan:**
  1. Configure Okta Lifecycle Management to automatically bind vendor access accounts to explicit expiration dates (maximum 90 days).
  2. Implement webhook automation between BambooHR and Okta to instantly revoke access across all downstream SaaS apps upon HR status updates.
* **Owner:** Lead Systems Engineer
* **Target SLA:** Involuntary offboarding < 1 hour; Voluntary offboarding < end-of-day.

---

### GAP-02: Absence of Centralized Privileged Access Management (PAM)
* **Current State:** Engineering leads currently maintain persistent administrative credentials to production AWS environments without requiring just-in-time (JIT) approval or short-lived session tokens.
* **Impact:** Violates the principle of least privilege and increases exposure if an engineering workstation is compromised via phishing or malware.
* **Corrective Action Plan:**
  1. Implement AWS IAM Identity Center with temporary, short-lived session credentials (maximum 4-hour duration).
  2. Require secondary approval via PagerDuty/Slack for any production environment privilege escalation (Just-In-Time access).
* **Owner:** Cloud Infrastructure / DevOps Team Lead
* **Target SLA:** Full rollout within 60 days.

---

### GAP-03: Informal & Unautomated Quarterly Access Reviews
* **Current State:** Quarterly access reviews are tracked manually via spreadsheets, causing delays, inconsistent audit evidence, and unverified manager sign-offs.
* **Impact:** Inability to demonstrate continuous compliance to external SOC 2 / ISO 27001 auditors; risk of "privilege creep" over time.
* **Corrective Action Plan:**
  1. Integrate Vanta (Compliance Automation Tool) with Okta and AWS to auto-generate quarterly entitlement reports.
  2. Establish a mandatory sign-off workflow requiring Department Heads to review and approve access lists directly in the compliance portal.
* **Owner:** GRC / Security Compliance Lead
* **Target SLA:** Fully operational prior to Q1 SOC 2 audit.

---

## 4. Remediation Progress Tracking & Monitoring

Remediation progress will be reviewed bi-weekly in the Information Security Steering Committee meeting. Gaps will remain open until technical evidence (such as Okta configuration logs or architectural diagrams) is reviewed and signed off by the Chief Information Security Officer (CISO).
