---
description: Mapping the Three Lines onto the platform.
---

# Three Lines of Defense in ServiceNow

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Three Lines of Defense in ServiceNow — video placeholder
{% endembed %}

## Overview

The Three Lines of Defense model is the standard governance architecture in banking and financial services: the first line owns and operates business risk, the second line provides oversight and sets the framework, and the third line (internal audit) provides independent assurance. ServiceNow IRM is purpose-built to support this structure — not just as a conceptual metaphor, but as a concrete design for role-based access, record ownership, and workflow routing. Understanding how each line is represented in the platform is essential before you configure a single risk record.

## Key concepts

- **First Line — Business Process Owners** — In ServiceNow, first-line users own Entity records and the risks and controls assigned to their business units. They execute control self-assessments (CSAs), attest that controls are operating, and respond to risk questionnaires. A Payments Operations manager completing a quarterly CSA in ServiceNow is acting as a first-line owner.
- **Second Line — Risk and Compliance Functions** — Second-line users (typically in Risk Management, Compliance, or Information Security) own the Risk Register structure, the Control Objectives, and the assessment methodology. They configure scoring models, define risk appetite thresholds, review first-line attestation results, and escalate Issues. In IRM, the second line also manages Indicators and KRIs — they own the alert logic and receive notifications when thresholds are breached.
- **Third Line — Internal Audit** — The Audit Management application within ServiceNow serves the third line. Auditors create Audit Engagements, link them to controls from the shared control library, generate Findings as a result of testing, and track remediation through Issues. Critically, audit accesses the same control and risk records the first and second lines use — there is no duplicate data entry.
- **Segregation of Duties** — ServiceNow's role-based access control (RBAC) enforces line independence. A first-line business owner cannot modify the scoring methodology; a second-line risk manager cannot close an audit Finding without an auditor's approval. Role design is as important as data design in an IRM implementation.
- **Entities and Profiles** — Each business unit, application, or process is an Entity in ServiceNow. Entities anchor the Three Lines: the first line manages risk at the entity level, the second line monitors aggregate entity risk profiles, and the third line schedules audits based on entity risk scores.

## How the three lines interact in ServiceNow

The table below maps the core activities of each line to the ServiceNow IRM records and workflows they use.

| Activity | Line | ServiceNow Record / Workflow |
|---|---|---|
| Own and operate a business process | First | Entity/Profile, Control self-assessment |
| Attest that a control is operating | First | Assessment response, Control attestation |
| Define risk appetite and scoring | Second | Risk Appetite records, Scoring methodology |
| Monitor KRIs and breaches | Second | Indicators, Automated alerts |
| Oversee the Risk Register | Second | Risk records, Risk Review workflow |
| Raise and track issues from gaps | Second | Issues, Remediation tasks |
| Plan and execute audit engagements | Third | Audit Engagement, Audit scope |
| Test controls and generate findings | Third | Control test records, Findings |
| Track audit finding remediation | Third (verify) / First (action) | Issues linked to Findings |

## A banking example: access control testing across three lines

Consider access controls for a bank's core banking application. Here is how the Three Lines interact in ServiceNow:

1. **First line (IT Operations)**: The application owner attests quarterly in ServiceNow that privileged access reviews are completed and that terminated-employee accounts are removed within 24 hours. This produces a control attestation record with evidence attached.
2. **Second line (Information Security Risk)**: The CISO's team monitors the "overdue access reviews" KRI in ServiceNow. When the indicator breaches its yellow threshold — say, 8% of reviews are more than five days late — an automated alert is sent to the risk owner and the residual risk score is recalculated.
3. **Third line (Internal Audit)**: During the annual IT audit, auditors pull the same access control record from the shared control library, review the attestation history, sample a subset of access reviews from the evidence vault, and — when they find a gap — raise a Finding. That Finding is automatically linked to the existing risk record in the Register, not entered into a separate audit spreadsheet.

The result: the second line sees the audit Finding in the same platform where it monitors KRIs. The first line receives a remediation task through ServiceNow's workflow engine. No emails, no separate tracking spreadsheet, no reconciliation meeting.

{% hint style="warning" %}
**Design principle**: Role design in ServiceNow must mirror the organizational Three Lines structure before you go live. Assigning second-line roles to first-line users — or vice versa — breaks the independence model and creates audit findings in itself. Get your RBAC design reviewed before user acceptance testing.
{% endhint %}

## In the video

- A live demonstration of the same control record viewed from first-line, second-line, and audit perspectives in ServiceNow.
- How the platform's RBAC prevents a first-line user from modifying risk scores.
- Tracing an audit Finding from creation through remediation closure without leaving ServiceNow.
- Common role-mapping mistakes and how to avoid them in a bank implementation.

## Key takeaways

- ServiceNow IRM maps the Three Lines to distinct role profiles, record ownership, and workflow permissions — the structure is not metaphorical, it is enforced by the platform.
- First-line users operate at the Entity level via CSAs and control attestations; second-line users own the risk framework and monitor KRIs; third-line auditors work within Audit Management but access shared control records.
- The shared data model eliminates the duplicate data entry between risk management and audit that creates reconciliation overhead in traditional tooling.
- RBAC design is a critical implementation decision — role boundaries must mirror actual organizational lines to maintain independence and satisfy regulatory expectations.
- The closed loop from KRI alert → second-line review → audit finding → first-line remediation → verified closure is the primary value demonstrator for bank risk executives evaluating the platform.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
