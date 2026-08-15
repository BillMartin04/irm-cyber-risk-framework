---
description: The Four Lines of Defense model this entire course is aligned to.
---

# The 4LOD Model — Course-Wide Frame


{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *The 4LOD Model — Course-Wide Frame — Cyber Risk Course Roadmap Explained (2026)*
**Channel:** [TechTalk with Bill](https://www.youtube.com/@techtalkwithbill)
**Length:** 8–12 min · **Status:** 🎬 In production — subscribe to be notified when this video is published.

▶ [Subscribe to be notified](https://www.youtube.com/@techtalkwithbill?sub_confirmation=1) · ⭐ [Star the repo](https://github.com/BillMartin04/irm-cyber-risk-framework)
{% endhint %}

Every module in this course lists which line or lines of defense it primarily serves. Read this page first — it is the shared vocabulary the rest of the course assumes.

## The four lines

- **1st Line — Operational Ownership.** The business unit or IT team that owns the day-to-day activity. First line runs the controls: they patch the servers, provision the identities, close the incidents. In the CMDB, they are the **CI owners** and the **Business Application owners**.
- **2nd Line — Risk Oversight & Compliance.** The risk-management, compliance, and information-security functions that set policy, monitor first-line performance, and challenge first-line decisions. In ServiceNow IRM, the 2nd line typically owns the **Risk records**, **Control Objectives**, and **Assessment cadence**.
- **3rd Line — Independent Assurance.** Internal Audit. Reports to the Audit Committee, independent of management. Tests both first- and second-line control effectiveness. Uses the same evidence as management but interprets it independently.
- **4th Line — Governing Body.** The Board and its committees, plus external regulators and external auditors. Owns strategic risk appetite, receives independent assurance, and holds executive management to account. Traditionally omitted from the Three Lines model; naming it explicitly is what makes 4LOD stronger.

## Why 4LOD matters for design

Every control, KRI, policy, and risk in a mature program has an accountable line and one or more oversight lines. If two lines collapse into one person (e.g., the CIO also chairs the Audit Committee), you have created a governance defect that will surface at the first regulatory exam.

Use the model in every design decision:

- Who **owns** this activity? (1st line)
- Who **oversees** it? (2nd line)
- Who provides **independent assurance**? (3rd line)
- Who has the **governance authority** to set appetite and approve exceptions? (4th line)

## In the CSDM + IRM stack

- 1st line ↔ CI Owner / Business Application Owner / Service Owner.
- 2nd line ↔ Risk Owner / Compliance Owner / Control Objective Owner.
- 3rd line ↔ Internal Audit Lead / Assessment Reviewer.
- 4th line ↔ Executive Sponsor / Risk Committee Chair / Board.

Every risk record in a well-configured ServiceNow IRM instance should carry all four fields.

## In Lumina Cyber Risk (open source)

The Lumina schema exposes `first_line_owner`, `second_line_oversight`, `third_line_assurance`, and `fourth_line_governance` directly on the risk scenario. Open the [seed data](https://github.com/BillMartin04/lumina-cyber-risk) to see a working example.

[← Course Home](../README.md)
