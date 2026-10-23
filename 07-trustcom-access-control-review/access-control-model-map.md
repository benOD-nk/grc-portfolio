# Access Control Model Map — TrustCom (Simulated)

One question classifies every path: **what made the decision?**

| Access path at TrustCom | What made the decision? | Model |
|---|---|---|
| Payment System roles (Viewer / Processor / Approver) | The person's job role alone; membership in the role grants everything | **RBAC** — Role-Based |
| Print server rejects jobs over 100 pages | One fixed condition on the job itself, applied to everybody including the CEO | **Rule-Based** |
| Confidential client reports cannot be emailed externally; label cannot be lowered by the author | The document's classification label; the system enforces it and the owner cannot override | **MAC** — Mandatory |
| Evidence Library folder shared by its owner with named people — or by link | The folder owner's personal choice of who gets in | **DAC** — Discretionary |
| Admin Portal sign-in (MFA + compliant company device + Canada + admin role) | Several attributes evaluated together at sign-in: role AND authentication AND device AND location | **ABAC** — Attribute-Based |
| Vendor (NorthPeak) login window, Mon–Fri 09:00–17:00 | The clock alone, for every vendor user | **Time-of-day restriction** |

## The distinctions this map proves
- **Role alone = RBAC.** Role plus anything else (device, place, time, assignment) = **ABAC**.
- **One blanket condition on the resource = Rule-Based**, even when the condition (an IP range, a browser, a page limit) looks like an "attribute."
- **No label, no MAC** — and when a label exists, the owner cannot share around it; that is what separates MAC from DAC.
- **Least privilege answers "how much." Time-of-day answers "when."** Different questions, different answers.

Project: User Access Review & Access Control Model Analysis — TrustCom (simulated). Workbook: `trustcom-access-review.xlsx`.
