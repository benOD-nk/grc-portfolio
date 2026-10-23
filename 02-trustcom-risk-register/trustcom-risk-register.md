# TrustCom Risk Register
*Simulated case study — all people, data, and events are fictional. Worked example, Module 2 mini-project.*

| ID | Risk description | Cause | Likelihood | Impact | Rating | Treatment | Owner | Due date | Status | Residual & sign-off |
|---|---|---|---|---|---|---|---|---|---|---|
| R-001 | Customer database breached via stolen admin credentials | No MFA on admin accounts | High | High | Critical | Mitigate: enforce MFA on all admin accounts | Abena Frimpong | Oct 30, 2026 | In progress | Low — pending Yaw's sign-off |
| R-002 | Ransomware encrypts file shares via phishing email | No awareness training; backups untested | High | High | Critical | Mitigate: quarterly phishing training + tested offline backups | Abena Frimpong | Nov 15, 2026 | Open | — |
| R-003 | Breach response costs (forensics, notification, legal) | No financial protection in place | Medium | High | High | Transfer: cyber insurance policy | Yaw Owusu | Nov 30, 2026 | Open | — |
| R-004 | Breach via legacy FTP server | Unpatched, internet-facing service | Medium | Medium | Medium | Avoid: decommission FTP server entirely | Yaw Owusu | Oct 31, 2026 | Open | — |
| R-005 | 2-hour analytics outage during maintenance window | Planned maintenance downtime | Low | Low | Low | Accept: documented, signed by Yaw Owusu | Yaw Owusu | Oct 16, 2026 | Closed | Low — accepted & signed |

## Notes
- All four treatments are represented: mitigate (R-001, R-002), transfer (R-003), avoid (R-004), accept (R-005).
- Ratings show the work: likelihood × impact → rating, no softened numbers.
- Rows close; they are never deleted. R-005 stays on the register as accepted.
- Register reviewed quarterly by Abena Frimpong; changes signed off by Yaw Owusu.
