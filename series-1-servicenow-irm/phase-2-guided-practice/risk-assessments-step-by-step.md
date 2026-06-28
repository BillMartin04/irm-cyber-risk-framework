---
description: Run a guided risk assessment in ServiceNow.
---

# Risk Assessments Step-by-Step

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Risk Assessments Step-by-Step — video placeholder
{% endembed %}

## Overview

A risk assessment in ServiceNow IRM is a structured workflow that systematically evaluates a defined set of risks — scoped to an entity, a business process, a vendor, or a framework — against your organization's scoring methodology and risk appetite. The platform manages assignment, collection, aggregation, and reporting; your job is to scope it correctly, ensure the right people are scoring, and interpret the results. This lesson walks through a complete assessment cycle using a retail banking example: a quarterly operational risk assessment for the Payments Processing business unit.

## Key concepts

- **Assessment scope** — The set of risks or controls that will be evaluated in this cycle. Scope can be defined by entity (e.g., Payments Processing), by risk category (e.g., all Operational Risk records), by framework, or by a manually selected subset. Scope definition drives who receives assessment tasks and what they are asked to score.
- **Scoring methodology** — The likelihood-impact matrix (or other quantitative method) configured in the platform that converts scorer inputs into a numeric risk score. Most banking implementations use a 5x5 matrix with calibrated anchor descriptions for each cell.
- **Inherent vs residual risk** — Inherent risk is the raw exposure before any controls are applied; residual risk is the remaining exposure after controls. ServiceNow calculates residual automatically when control effectiveness ratings are combined with inherent scores.
- **Risk appetite** — A threshold record in ServiceNow that defines acceptable residual risk levels by category. When a completed assessment produces a residual score above appetite, the platform flags the risk for escalation and can trigger an automatic review workflow.
- **Assessment respondents** — The users assigned to score risks in the assessment. In a Three Lines model, first-line business owners typically score likelihood and control effectiveness; second-line risk managers review and may override scores before the assessment is finalized.
- **Assessment templates** — Pre-configured assessment structures that specify which risk or control records to include, which scoring fields to present, and which methodology to apply. Templates make recurring assessments (quarterly, annual) repeatable without reconfiguration.

## Step-by-step: running a quarterly operational risk assessment

The following steps walk through a standard quarterly assessment for the Payments Processing entity at a regional bank.

**Step 1 — Navigate to the assessment module**

Go to Risk Management > Assessments > Create New Assessment. Select "Risk Assessment" as the type. Give the assessment a meaningful name: "Q3 2026 — Payments Processing Operational Risk Assessment."

**Step 2 — Set the scope**

In the Scope field, select the Payments Processing entity. The platform will automatically pull in all active risk records associated with that entity — in this example, 24 operational risk records covering transaction processing, system availability, fraud, and third-party payment processors. Review the auto-populated list and remove any risks that are out of scope for this cycle (e.g., risks under remediation with a scheduled review date in Q4).

**Step 3 — Select the scoring methodology**

Choose the "Standard Banking Op Risk 5x5" methodology from the dropdown. Confirm the likelihood and impact anchor descriptions are appropriate for the payment processing context — "Highly Likely" for this business unit should reflect the volume and frequency profile of a high-transaction-rate operation.

**Step 4 — Assign respondents**

Add the Payments Operations Manager as the primary respondent for likelihood and control effectiveness scores. Add the Operational Risk Manager (second line) as the reviewer. Set a response due date 10 business days out; the platform will send automated reminders at five days and two days before the deadline.

**Step 5 — Launch the assessment**

Click "Launch." ServiceNow generates individual assessment tasks for each assigned respondent and sends notification emails with direct links to their scoring queues. Each respondent sees only their assigned risks and the fields they are authorized to complete.

**Step 6 — Monitor progress**

From the Assessment record's Progress tab, monitor completion rates. At any point you can see which risks have been scored, which are pending, and which respondents have not yet started. Use the "Send Reminder" action to nudge specific respondents without leaving the platform.

**Step 7 — Review draft scores**

Once the first-line respondent completes scoring, the assessment status moves to "Pending Review." Open the scoring summary to review each risk's likelihood, impact, and control effectiveness inputs. Where scores appear inconsistent with other data sources (KRI values, recent incidents, audit findings), add a comment and return the specific item to the respondent for clarification.

**Step 8 — Finalize and interpret results**

Approve the final scores. ServiceNow calculates residual risk scores for each risk record and updates the Risk Register automatically. The aggregate view shows residual scores mapped against risk appetite thresholds. Risks above the red threshold are flagged for escalation to the risk committee. In this example, two risks — "Third-party payment processor outage" and "Real-time gross settlement system dependency" — breach the appetite threshold and are elevated to the quarterly risk committee agenda.

**Step 9 — Generate the output**

Export the assessment results as a structured report or access the live Risk Register dashboard for the Payments Processing entity. The report shows inherent scores, control effectiveness, residual scores, appetite comparison, and any escalation flags — ready for the risk committee package without manual formatting.

{% hint style="info" %}
**Efficiency note**: For recurring quarterly assessments, save the completed assessment as a template. Next quarter, launch the same assessment, update the date, confirm the risk scope is current, and launch — the methodology, respondents, and structure carry forward automatically.
{% endhint %}

## In the video

- Creating an assessment record and setting scope against the Payments Processing entity.
- The respondent experience: what a first-line business owner sees in their scoring task.
- Reviewing draft scores as a second-line risk manager and adding review comments.
- Interpreting the aggregate results dashboard against the risk appetite thresholds.
- Exporting the assessment output for a risk committee briefing.

## Key takeaways

- A ServiceNow risk assessment workflow covers the full cycle — scope definition, task assignment, automated reminders, score aggregation, appetite comparison, and output — without any manual file management.
- Scope definition is the most consequential step: over-scoping wastes respondent time; under-scoping produces an incomplete risk view.
- Inherent and residual scores are calculated fields, not manual entries — they update automatically when control effectiveness ratings change.
- Risks that breach appetite at assessment completion trigger escalation workflows in the platform; no manual flagging required.
- Saving recurring assessments as templates is the primary time-saving mechanism for quarterly and annual assessment cycles.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
