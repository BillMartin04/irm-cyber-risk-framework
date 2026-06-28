---
description: Turn gaps into tracked issues and remediation.
---

# Issues and Findings Management

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Issues and Findings Management — video placeholder
{% endembed %}

## Overview

Every risk assessment, control attestation, and audit engagement produces gaps — controls that failed, risks above appetite, processes that deviated from policy. The measure of a mature risk program is not whether gaps exist; it is whether those gaps are captured, owned, tracked, and systematically resolved. In ServiceNow IRM, Issues and Findings are the records that close this loop. They convert assessment results and audit observations into managed remediation work with owners, due dates, escalation logic, and verified closure. For a bank with dozens of active assessments, hundreds of controls, and multiple regulatory exam cycles running simultaneously, the alternative — tracking remediation in spreadsheets or email — is operationally untenable.

## Key concepts

- **Issues** — A record in ServiceNow that captures a gap, failure, or identified risk that requires corrective action. Issues can be created manually, automatically from a failed control attestation, from a KRI breach, or from an audit Finding. An Issue has a description, a risk rating, an assigned owner, a due date, one or more remediation tasks, and a closure workflow.
- **Findings** — A specific record type within Audit Management that documents an auditor's observation — a gap identified during audit testing of a control. Findings are linked to the specific control tested, the audit engagement that produced them, and a severity rating. When a Finding is raised, it typically generates a corresponding Issue for remediation tracking.
- **Remediation Tasks** — Child records under an Issue that break the corrective action into discrete, assignable steps. A single Issue for "Privileged access reviews not completed within required timeframe" might have three remediation tasks: (1) complete overdue reviews immediately, (2) implement an automated access review scheduling tool, (3) update the access review procedure document.
- **Issue Owner vs Remediation Task Owner** — The Issue Owner is accountable for the overall resolution of the gap and has visibility into all remediation tasks. Task owners are responsible for completing specific actions. These can be different people — the Issue Owner is often a second-line risk manager or compliance officer; task owners are first-line operational staff.
- **Issue Lifecycle** — ServiceNow Issues move through a defined status workflow: Open → In Remediation → Pending Verification → Closed. The transition from "Pending Verification" to "Closed" requires a verifier (typically the second line or audit) to confirm that the remediation is complete and effective, with evidence.
- **Risk Rating and Escalation** — Issues are rated by severity (Critical, High, Medium, Low) at creation. Critical and High issues can be configured to trigger escalation notifications to senior risk officers or executive committees. Issues approaching their due date without progress trigger automated reminders.
- **Linking Issues to the Risk Register** — Every Issue in ServiceNow can be linked to the specific risk record it relates to. When an Issue is open, it is visible on the risk record's related list, contributing to the qualitative residual risk picture. When the Issue is closed with verified remediation, the risk record reflects the improved control environment.
- **Regulatory Exam Findings** — During OCC, Federal Reserve, or FDIC examinations, examiners may raise Matters Requiring Attention (MRAs) or Matters Requiring Immediate Attention (MRIAs). These can be entered as Findings in ServiceNow (or as Issues directly) and tracked through the same remediation workflow — giving bank management and regulators a single view of remediation status.

## The Issues lifecycle in a banking context

The following scenario illustrates the full lifecycle for a gap identified during a quarterly compliance assessment at a regional bank.

**Source: failed attestation**

The annual FFIEC CAT compliance assessment completes. The IT Security team's attestation for "Vulnerability Management — Critical patches applied within 14 days" returns a status of "Partially Effective." The control owner notes that 12% of critical patches in Q2 were applied outside the 14-day SLA due to a change approval backlog.

**Issue auto-created**

ServiceNow automatically creates an Issue linked to the Vulnerability Management control record. The Issue is rated "High" based on the control's criticality tier. The Issue description is pre-populated from the attestation comment; the control owner is assigned as the Issue Owner. A notification is sent to the Information Security Risk Manager (second line) as reviewer.

**Remediation tasks defined**

The Information Security Risk Manager reviews the Issue and adds three remediation tasks:

1. **Immediate**: Conduct a one-time review of all patches applied in Q2 outside SLA; confirm none introduced unmitigated exposure. Due: 10 business days.
2. **Process**: Revise the change approval workflow to create an expedited track for security patches rated Critical or higher. Due: 30 business days.
3. **Monitoring**: Configure a ServiceNow Indicator to track real-time patch application rates against the 14-day SLA. Due: 45 business days.

Each task is assigned to a specific owner — the first task to the Vulnerability Management team lead, the second to the IT Change Manager, the third to the Risk Analytics team.

**Progress tracking**

From the Issues dashboard (Risk Management > Issues), the Information Security Risk Manager can see all three tasks, their due dates, completion status, and any comments. At 7 days before each task's due date, ServiceNow sends an automated reminder to the task owner. If a task is not updated within 3 days of its due date, an escalation notification is sent to the Issue Owner.

**Verification**

When the remediation task owners mark all three tasks complete and attach evidence (patch compliance report, updated procedure document, screenshot of the new Indicator configuration), the Issue status moves to "Pending Verification." The second-line Information Security Risk Manager reviews the evidence, confirms completeness, and transitions the Issue to "Closed."

**Risk Register update**

The Vulnerability Management control record now reflects a verified, closed Issue. The next quarterly attestation will assess the improved control environment. If the control passes as "Effective," the residual risk score for the linked Operational Risk — IT / Cybersecurity risk record improves accordingly.

## Managing a portfolio of issues

At any given time, a bank running a mature ServiceNow IRM program may have 50 to 200 open Issues across operational risk, compliance, third-party risk, and audit findings. The Issues dashboard provides a portfolio view with filtering by:

- **Source**: Assessment, Audit, KRI breach, Manual
- **Severity**: Critical, High, Medium, Low
- **Entity**: Business unit or process
- **Age**: Days open, approaching due date, overdue
- **Framework**: FFIEC, NIST CSF, CRI Profile, ISO 27001

This view is the primary operational tool for a second-line risk manager's daily work and the primary source of data for the risk committee's "open issues" slide.

{% hint style="warning" %}
**Regulatory exam tip**: When regulatory examiners (OCC, Federal Reserve, FDIC) request a status update on prior examination findings, the Issues portfolio view filtered by "Source: Regulatory Exam" provides an instant, auditable status report. This is significantly more defensible than a manually compiled spreadsheet and demonstrates the bank's active management of regulatory commitments.
{% endhint %}

## In the video

- Creating an Issue manually and from a failed control attestation in ServiceNow.
- Adding remediation tasks with owners and due dates.
- The Issue owner and task owner experience: completing and evidencing a remediation task.
- Moving an Issue from "Pending Verification" to "Closed" as a second-line reviewer.
- The Issues portfolio dashboard: filtering by severity, source, entity, and due date.
- How closed Issues feed back into the Risk Register and control effectiveness ratings.

## Key takeaways

- Issues and Findings are the records that close the loop between assessment results and actual control improvement — without them, a risk assessment is just a snapshot with no consequence.
- The Issues lifecycle in ServiceNow (Open → In Remediation → Pending Verification → Closed) enforces two-step closure: a task owner completes the action, a verifier confirms it is effective.
- Remediation tasks break complex corrective actions into specific, assignable steps with individual owners and due dates — critical for Issues that span multiple teams.
- The Issues portfolio dashboard is the primary daily work surface for second-line risk managers and the primary source for risk committee reporting on open gaps.
- Regulatory examination findings tracked in ServiceNow Issues provide auditable, real-time remediation status — a significant advantage over spreadsheet-based MRA tracking in regulatory exams.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
