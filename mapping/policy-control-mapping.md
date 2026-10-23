# Policy-to-Control Mapping

**Framework:** NIST Cybersecurity Framework (CSF) 2.0
**Policies mapped:** Password and Authentication, Access Control, Incident Response
**Status:** Draft. Control IDs checked against nist.gov where marked ✅.

| # | Policy | Section | Requirement (plain English) | NIST CSF 2.0 ID | Function | Verified |
|---|---|---|---|---|---|---|
| 1 | Password | 3.4 | Reject passwords found on breached or common lists | PR.AA-03 | Protect | ☐ |
| 2 | Password | 4.1 | Require MFA for email, VPN, cloud apps, and admins | PR.AA-03 | Protect | ☐ |
| 3 | Password | 5.1 | Use a company-approved password manager | PR.AA-01 | Protect | ☐ |
| 4 | Password | 5.3 | Store passwords only as salted hashes | PR.DS-01 | Protect | ☐ |
| 5 | Access Control | 3.1 | Users get only the access they need (least privilege) | PR.AA-05 | Protect | ☐ |
| 6 | Access Control | 3.3 | Every user has a unique account | PR.AA-01 | Protect | ☐ |
| 7 | Access Control | 4.1 | Access requests are approved by a manager | PR.AA-05 | Protect | ☐ |
| 8 | Access Control | 5.3 | Admin activity is logged and reviewed monthly | DE.CM-03 | Detect | ☐ |
| 9 | Access Control | 6.1 | Managers review team access every 6 months | PR.AA-05 | Protect | ☐ |
| 10 | Access Control | 7.2 | All access is disabled when someone leaves | PR.AA-01 | Protect | ☐ |
| 11 | Incident Response | 4.2 | An Incident Response Lead coordinates the response | GV.RR-02 | Govern | ☐ |
| 12 | Incident Response | 6 | Incidents are rated by severity (Low to Critical) | RS.MA-03 | Respond | ☐ |
| 13 | Incident Response | 7.1 | Contain the incident to limit damage | RS.MI-01 | Respond | ☐ |
| 14 | Incident Response | 7.4 | Restore from clean backups before returning to use | RC.RP-03 | Recover | ☐ |
| 15 | Incident Response | 9.1 | Hold a review meeting after significant incidents | ID.IM-03 | Identify | ☐ |
| 16 | Incident Response | 10.2 | Test the response process yearly with a tabletop exercise | ID.IM-02 | Identify | ☐ |

## Notes

- Rows 2, 5, 7, and 9 show that one control can be supported by several policy sections, and one section can support more than one control.
- Some mappings are judgment calls. I mapped lines based on my own reading of the framework, and a different reviewer might choose differently.
- Policy sections not mapped yet (for example, the account lockout rule and remote access) are candidates for a future update.
