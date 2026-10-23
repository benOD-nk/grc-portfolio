# User Access Review & Access Control Model Analysis — TrustCom (Simulated)

> **Simulated project.** TrustCom is a fictional 25-person SaaS company. All people, systems and data in this project are invented for portfolio demonstration. No real client information is used.

## What this project is
A user access review of TrustCom's payment and admin systems, performed the way a GRC analyst performs it in practice: pull the access list, reconcile it against people and roles, classify how each access decision is made, and turn every exception into a finding with an owner, a fix, and a retest.

## Method
1. Requested the system-generated user access list for the Payment System, Admin Portal, Evidence Library and Support Desk.
2. Reconciled every account against the staff list and leaver records (joiner–mover–leaver check).
3. Mapped each role against the Role Matrix to test separation of duties.
4. Classified each access path by model using one question: **what made the decision?** — role alone (RBAC), one fixed condition on the resource (Rule-Based), a label and clearance (MAC), the resource owner (DAC), or several attributes combined (ABAC).
5. Logged five findings with severity, evidence source, owner and due date; tracked remediation to retest.

## Deliverable
`trustcom-access-review.xlsx` — 4 sheets:
- **User Access List** — 11 accounts reviewed with reviewer notes
- **Role Matrix** — Viewer / Processor / Approver permissions and the unauthorised "Super Role" variant
- **Findings Log** — 5 findings (F1–F5) with risk area, evidence and remediation
- **Remediation Tracker** — action taken, retest method and result for each finding

`access-control-model-map.md` — each TrustCom access path mapped to its access control model, with the reasoning shown.

## Findings at a glance
| ID | Finding | Severity |
|----|---------|----------|
| F1 | Leaver account still active 3 months after exit | High |
| F2 | "Super Role" can create AND approve payments (separation of duties broken) | High |
| F3 | Client evidence folder shared as "anyone with the link" | Medium |
| F4 | Legacy admin account excluded from Conditional Access | High |
| F5 | Vendor access 24/7 against a Mon–Fri 9–5 contract window | Medium |

All five remediated and retested — see the Remediation Tracker sheet.

## Framework mapping
ISO/IEC 27001:2022 Annex A — 5.15 Access control · 5.16 Identity management · 5.17 Authentication information · 8.2 Privileged access rights · 8.3 Information access restriction.

## Skills demonstrated
Access review execution · RBAC role analysis · separation of duties · least privilege · evidence handling (system exports over screenshots) · finding writing (risk, evidence, remediation) · remediation tracking and retest.

## Resume bullet
Performed a simulated user access review for a 25-person SaaS company: reconciled system access lists against HR records and a role matrix, identified five access control findings (dormant leaver account, separation-of-duties conflict, link-based oversharing, privileged account excluded from conditional access, vendor access outside contracted hours) and tracked remediation through to retest.
