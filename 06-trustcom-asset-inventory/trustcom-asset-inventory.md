# TrustCom Asset Inventory & Classification Scheme
*Simulated case study — all people, data, and events are fictional. Worked example, Module 6 mini-project (portfolio #6).*

## Why this exists
You cannot protect what you do not know you have. An asset you cannot see is an asset you cannot classify, patch, back up, or audit. This inventory is TrustCom's single list of what it owns, who owns it, what data it holds, and how that data must be handled.

## Classification scheme (set by Sofia Laurent, Compliance Lead)
| Class | Meaning | Handling rules |
|---|---|---|
| Public | Safe for anyone to see | No restrictions. Example: press releases, marketing pages |
| Internal | For staff only, low harm if leaked | Staff systems only, no public posting |
| Confidential | Harm if leaked | Labelled, encrypted in transit and at rest, shared only with named people, label must travel with the file |
| Restricted | Serious harm if leaked (regulated or financial data) | Confidential rules plus: access logged, DLP monitored, owner approval for any external share |

**The key thing:** the label is not decoration. The label is what tells every later control — encryption, DLP, access rules — how hard to work. An unlabelled file gets treated like a public one by the tools, no matter what is inside it.

## Asset inventory (owner: Abena Frimpong, GRC Analyst; approved by Yaw Owusu, CTO)

| ID | Asset | Type | Owner | Data held | Class | Location | Status / note |
|---|---|---|---|---|---|---|---|
| A-001 | Customer card-payment database | Database | Yaw Owusu | Cardholder data | Restricted | Cloud, encrypted at rest | Live. Access logged; DLP monitored |
| A-002 | Press releases & marketing pages | Data set | Sofia Laurent | Public announcements | Public | Website CMS | Live. Same system as A-001's host — different data, different class, different controls |
| A-003 | Payroll spreadsheet | File | Abena Frimpong | Staff salaries, bank details | Confidential | Finance share | **Finding F-1:** found unlabelled during this review — see below |
| A-004 | Training-room network segment | Network | Yaw Owusu | None (infrastructure) | Internal | Office LAN | Live. Access limited by time of day, off midnight–6 AM |
| A-005 | Legacy FTP server | Server | Yaw Owusu | File transfers | Internal | Office server room | Decommission planned (see risk register R-004) |
| A-006 | Staff laptops (fleet of 25) | Hardware | Abena Frimpong | Mixed, up to Confidential | Confidential | With staff | Live. Full-disk encryption enforced |
| A-007 | Unknown device found on office network scan | Hardware | Unassigned | Unknown | Unknown | Office LAN | **Finding F-2:** quarantined on discovery — see below |

## Findings from building this inventory
- **F-1 — Unlabelled payroll file (A-003).** The payroll spreadsheet held Confidential data but carried no label, so when it was emailed out, no tool flagged it: the label is what makes the protection travel with the file. Fixed: file labelled Confidential, handling rules re-briefed to Finance. Lesson: classification that lives only in people's heads protects nothing.
- **F-2 — Unknown asset (A-007).** A network scan found a device that was on no list. An unknown asset cannot be classified, patched, or monitored, so it was quarantined first and identified second. Lesson: the inventory is only trustworthy if discovery (scans) is checked against it on a schedule — a list nobody re-checks goes stale, and a stale list is worse than none because people trust it.
- **Known limit — DLP.** TrustCom's DLP watches data leaving by email and upload. It cannot see a photograph of a screen taken on a personal phone. The control is real, but claiming it "covers everything" would be a false claim; the gap is recorded here, not hidden.

## Review rule
Inventory re-checked against a network scan quarterly by Abena Frimpong; new assets get an owner and a class before they go live; changes signed off by Yaw Owusu. Rows are never deleted — retired assets are marked decommissioned so the history stays auditable.
