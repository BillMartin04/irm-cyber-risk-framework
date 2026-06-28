---
description: A tour of the IRM workspace and navigation.
---

# Navigating the IRM Module

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Navigating the IRM Module — video placeholder
{% endembed %}

## Overview

Knowing where things live in ServiceNow IRM is the difference between a practitioner who moves with confidence and one who spends half their time hunting through menus. The platform has evolved significantly — the modern IRM experience uses dedicated Workspaces alongside the classic Application Navigator, and understanding both surfaces is important. This lesson tours every major area you will use: the Risk Management Workspace, the Policy & Compliance module, the Audit Management application, and the shared record types that underpin all three.

## Key concepts

- **Application Navigator** — The left-hand sidebar in ServiceNow that lists all installed applications and their modules. In a standard IRM deployment, you will find separate navigator groups for Risk Management, Policy and Compliance, Audit Management, and Advanced Risk. Each group contains list views for that application's core records.
- **Risk Management Workspace** — The role-based workspace for second-line risk practitioners. It surfaces open risks by score, KRI alerts, assessment queues, and overdue remediation tasks in a single dashboard. Unlike the Application Navigator list views, the workspace is designed for daily risk monitoring rather than record configuration.
- **Risk Register** — Accessed via Risk Management > Risks or directly from the workspace dashboard. The register is a list of all active risk records. Each record opens to show the risk statement, entity scope, inherent and residual scores, linked controls, active assessments, and associated indicators.
- **Entities and Profiles** — Found under Risk Management > Entities. An Entity record is the scope anchor — it could be a legal entity, business unit, application, or third-party vendor. Opening an entity shows all risks, controls, indicators, and assessments associated with it.
- **Control Objectives and Controls** — Under Policy and Compliance > Control Objectives and Controls. Control Objectives are the desired outcomes; Controls are the specific activities. Controls can also be accessed from the Risk Register — each risk record shows its linked mitigating controls inline.
- **Assessments** — Under Risk Management > Assessments (for risk assessments) and Policy and Compliance > Assessments (for control attestations). The assessment record shows scope, assigned respondents, scoring criteria, and status. Completed assessments feed back into risk scores automatically.
- **Indicators** — Under Risk Management > Indicators. Each indicator record defines a KRI, its data source (automated feed or manual entry), thresholds (green/yellow/red), and the risk records it monitors. Breached indicators trigger workflow notifications to risk owners.
- **Issues and Findings** — Under Risk Management > Issues (for risk-driven gaps) and Audit Management > Findings (for audit-generated gaps). Both record types link to the underlying control or risk. An Issue has an owner, a due date, remediation tasks, and a closure workflow that requires evidence of remediation.
- **Policy & Compliance module** — Contains Policies, Policy Statements, Authority Documents, and the compliance assessment workflow. This is where your regulatory library lives — FFIEC IT Examination Handbook, OCC Heightened Standards, NIST CSF — and where policy-to-control mappings are maintained.

## The navigation flow in practice

A second-line operational risk manager at a mid-size bank might follow this daily navigation pattern:

1. **Start in the Risk Management Workspace** — Review the KRI alert dashboard for any indicators breached overnight. One alert shows the "failed wire transfer volume" indicator has crossed its yellow threshold.
2. **Navigate to the Indicator record** — Click through from the alert to the Indicator record. Confirm the threshold breach, review the data source, and check whether the linked risk record's residual score needs to be recalculated.
3. **Open the linked Risk record** — See the risk statement ("there is a risk that payment processing errors result in financial loss and regulatory breach"), review current controls, and check whether any controls have a recent failed attestation.
4. **Pivot to the Assessment queue** — Navigate to Risk Management > Assessments to find the quarterly self-assessment assigned to the Payments Operations entity. Confirm it is on track and review any partially completed responses.
5. **Check open Issues** — Navigate to Risk Management > Issues, filtered to "Overdue." Follow up on two issues from last quarter's assessment that are past their remediation due date.

That entire workflow — monitoring, investigation, assessment management, and remediation tracking — happens without leaving ServiceNow or opening a single spreadsheet.

## Finding records across modules

One of the most useful navigation techniques in ServiceNow IRM is using the global search bar and related lists. Every risk record has a Related Items tab that shows linked controls, assessments, indicators, issues, and policy statements. Every control record shows the risks it mitigates, the authority document requirements it satisfies, and the assessments that have tested it. Learning to navigate by following relationships — rather than by module-hopping — is the mark of an experienced IRM practitioner.

{% hint style="info" %}
**Tip**: Use the ServiceNow list view column chooser to add "Residual Score" and "Last Assessment Date" to your default Risk Register view. Those two columns answer the most common questions in a risk committee meeting without clicking into individual records.
{% endhint %}

## In the video

- A live tour of the Application Navigator for IRM — every major module group.
- Switching between the Risk Management Workspace and the classic navigator view.
- Opening a risk record and tracing its connections to controls, assessments, and indicators.
- The Policy & Compliance module layout — where authority documents, policies, and controls live.
- Navigating from a KRI breach alert to the underlying risk record and open issues.

## Key takeaways

- ServiceNow IRM navigation splits between the Application Navigator (module-level access) and the Risk Management Workspace (day-to-day monitoring dashboard for risk practitioners).
- Core record types — Risk Register, Entities, Controls, Assessments, Indicators, Issues — each have their own list views but are heavily cross-linked; navigating by relationships is more efficient than module-hopping.
- The Assessment queue and Issues list are the two most operationally important views for a second-line risk team managing a banking GRC program.
- Global search and Related Items lists are the fastest way to surface connected records without memorizing exact navigation paths.
- Mastering navigation before attempting configuration prevents the most common orientation mistakes in new IRM implementations.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
