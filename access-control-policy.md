# Access Control Policy

**Document ID:** POL-SEC-002  
**Version:** 1.0  
**Effective Date:** October 24, 2026  
**Owner:** Information Security & Compliance  
**Target Audience:** All Employees, Contractors, and Third-Party Vendors  

---

## 1. Purpose
The purpose of this Access Control Policy is to establish rules for granting, managing, and revoking access to MedTech Innovations' information systems, networks, and sensitive data (including Protected Health Information, or PHI). Proper access controls minimize unauthorized access, data loss, and regulatory non-compliance under HIPAA and ISO 27001 standards.

---

## 2. Scope
This policy applies to:
- All full-time and part-time employees, contractors, interns, and third-party vendors.
- All hardware, cloud infrastructure (AWS), applications (SaaS/internal), and databases owned or managed by MedTech Innovations.
- All access methods, including local, remote (VPN/Zero Trust), and direct physical access.

---

## 3. Core Policy Rules

### 3.1 Least Privilege & Need-to-Know
1. **Default Deny:** Access to all systems and data is explicitly denied by default unless formally requested and approved.
2. **Role-Based Access Control (RBAC):** Users will be assigned pre-defined roles based strictly on their job function (e.g., Engineer, Support Specialist, Compliance Auditor).
3. **Elevated Privileges:** Administrative or root privileges must be restricted to authorized Infrastructure & IT personnel and require dual-authorization for activation.

### 3.2 Authentication & Password Standards
1. **Multi-Factor Authentication (MFA):** Mandatory for all users accessing company resources, cloud environments, and internal applications without exception. Hardware tokens or authenticator apps (TOTP) are preferred over SMS.
2. **Password Parameters:**
   - Minimum length: **16 characters** for standard accounts, **20 characters** for administrative accounts.
   - Requirement: Passwords must contain a combination of uppercase, lowercase, numbers, and symbols.
   - Reuse: Passwords cannot match any of the previous 10 passwords used.
3. **Password Managers:** Employees must store work credentials in the enterprise-approved password manager. Plaintext storage of credentials is strictly prohibited.

### 3.3 Account Lifecycle Management

#### Onboarding (Provisioning)
1. Account creation requires a formal request submitted by HR or the hiring manager via the internal ticketing system.
2. Access requests must explicitly state the role, required systems, and business justification.
3. Written approval from the System Owner is required prior to account activation.

#### Modifications & Role Changes
1. When an employee changes roles, HR must initiate a privilege review. Unnecessary access rights from the previous role must be revoked within **2 business days**.

#### Offboarding (Deprovisioning)
1. **Involuntary Terminations:** IT and HR must execute emergency deprovisioning **immediately** (SLA: < 1 hour) upon notification.
2. **Voluntary Terminations:** Access must be fully revoked no later than **5:00 PM local time on the employee’s final working day**.
3. HR must confirm all issued credentials, keys, and hardware have been returned or disabled.

### 3.4 Third-Party & Vendor Access
1. Third-party vendors must have a signed Business Associate Agreement (BAA) and Non-Disclosure Agreement (NDA) on file prior to receiving system access.
2. Vendor accounts must be assigned an explicit **expiration date** (maximum 90 days) and require renewal approval from the Security Officer.
3. All vendor remote access must be monitored via centralized audit logs.

### 3.5 Session Security & Workstation Controls
1. Systems must automatically initiate a password-protected lock screen after **15 minutes** of inactivity.
2. Users must manually lock workstations (`Win + L` or `Cmd + Ctrl + Q`) whenever leaving their desks.

---

## 4. Monitoring & Enforcement

### 4.1 Audit Logging & Periodic Access Reviews
1. All authentication attempts, access grants, and privilege escalation events must be logged centrally.
2. **Quarterly Access Reviews:** System Owners and the Security Team must review all active accounts and privileges every 90 days to identify stale accounts or privilege creep.

### 4.2 Non-Compliance & Violations
Failure to adhere to this policy may result in disciplinary action up to and including termination of employment, termination of contract, or legal prosecution under relevant regulatory frameworks.

---

## 5. Framework References & Compliance Mapping

| Regulatory / Framework Standard | Specific Control Mapping |
| :--- | :--- |
| **NIST CSF v2.0** | `PR.AA-01` (Identity Management), `PR.AA-02` (Authentication), `PR.AA-05` (Access Rights) |
| **ISO 27001:2022** | Control `A.5.15` (Access Control), Control `A.5.18` (Access Rights), Control `A.8.5` (Secure Authentication) |
| **HIPAA Security Rule** | `45 CFR § 164.312(a)(1)` (Access Control), `45 CFR § 164.312(d)` (Person/Entity Authentication) |
