---
description: Automate workflows and responses.
---

# Automated Risk Responses

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Automated Risk Responses — video placeholder
{% endembed %}

## Overview

Manual risk management does not scale. A mid-size bank might run 400 controls across three lines of defense, track 50 KRIs, manage 200 active vendors, and field a dozen audit requests simultaneously. When a KRI breaches its red threshold at 2 a.m. on a Saturday, someone needs to know, and someone needs to act. ServiceNow's Flow Designer provides the automation layer that makes this possible — triggered by data changes in the Risk Register, KRI values, Control states, or external integration events, flows route work, create records, send notifications, and enforce SLAs without human intervention.

## Key concepts

* **Flow Designer** — ServiceNow's low-code/no-code automation builder. Flows are composed of a trigger, zero or more conditions, and a sequence of actions. Unlike legacy Workflow (now largely deprecated), Flow Designer is table-agnostic and integrates natively with IRM tables like sn\_risk\_risk, sn\_risk\_indicator\_value, and sn\_compliance\_control.
* **Trigger** — The event that starts a flow. IRM-relevant triggers include: Record Created, Record Updated (field change), Scheduled (time-based), and Inbound Webhook (for external system pushes such as SIEM alerts).
* **Condition** — A filter applied after the trigger to determine whether the flow should run. Example: only fire when residual\_rating changes *to* High and entity\_type = "Core Banking System."
* **Action** — A discrete step the flow executes: Create Record, Update Record, Send Email, Send Notification, Ask for Approval, or call a Sub-flow. IRM ships with several packaged actions for creating Issues and linking them to risks.
* **Issue** — A structured record in IRM (table: sn\_risk\_issue) that documents a risk event, control failure, or threshold breach. Issues carry owner, severity, due date, and remediation tasks. Auto-creating Issues from flow triggers ensures nothing falls through the cracks.
* **SLA (Service Level Agreement)** — Flow Designer can attach SLA definitions to tasks created by automation, enforcing escalation when remediation is not completed within the agreed window.
* **Sub-flows and Reusability** — Complex logic (e.g., the standard "KRI breach response" process) can be packaged as a Sub-flow and invoked from multiple parent flows, keeping maintenance centralized.

## Building an automated KRI breach response in Flow Designer

This walkthrough builds the most common IRM automation in banking: a flow that fires when a KRI breaches its red threshold, creates a remediation Issue, assigns it to the risk owner, and escalates if not acknowledged within 24 hours.

### Step 1: Create the flow

Navigate to **Flow Designer > New Flow**. Name it *IRM — KRI Red Threshold Breach Response*. Set the **Run As** field to a service account with IRM write permissions (never a named user account).

### Step 2: Configure the trigger

Select **Record Updated** as the trigger type. Set the table to **sn\_risk\_indicator\_value** (the Indicator Values table that stores each KRI snapshot). Add a field condition:

* Field: **Color State**
* Changed: **To** Red

This fires only when a KRI transitions *into* red, not on every update.

### Step 3: Add a condition to scope the flow

Not every KRI breach warrants the same response. Add a **Condition** step:

```
indicator.category = "Operational Risk" OR indicator.category = "Cyber Risk"
```

This prevents the flow from firing on informational or diagnostic indicators that are not board-reportable.

### Step 4: Create the Issue record

Add an **Action > Create Record** step pointing to the **sn\_risk\_issue** table. Populate:

* **Short description:** Auto-populate from the KRI name and breach value (use pill tokens from the trigger data)
* **Severity:** High
* **Assigned to:** Pull from the related Risk Register record's *Risk Owner* field via a **Lookup Records** step
* **Related risk:** Link back to the parent Risk record
* **Due date:** `NOW() + 5 business days` (using the Date utility action)

### Step 5: Send a notification

Add a **Send Email** action (or **Send Notification** for in-platform alerts). Recipients: the assigned risk owner, their manager (pulled via the User's manager field), and a distribution list for the Risk Management team. Use a templated email that includes the KRI name, current value, threshold, and a deep link to the newly created Issue.

### Step 6: Attach an SLA

Add an **Ask for Approval** or use the **SLA** sub-flow to enforce a 24-hour acknowledgment window. If the risk owner does not update the Issue within 24 hours, an escalation action notifies the CRO and creates a separate escalation task.

### Step 7: Test and activate

Use Flow Designer's built-in **Test** function to fire the flow against a synthetic Indicator Value record. Review the execution log to confirm the Issue was created, the notification was sent, and the SLA was applied. Once validated, set the flow to **Active**.

{% hint style="info" %}
Keep a separate flow for **Control Failure Auto-Response** (trigger: Control test result changes to Ineffective) and another for **Risk Re-assessment Triggers** (trigger: a Material Issue is closed, prompting re-evaluation of the related risk's residual score). These three flows — KRI breach, control failure, risk re-assessment — cover the majority of automated IRM scenarios in banking.
{% endhint %}

## Additional automation patterns

| Scenario | Trigger | Key action |
|---|---|---|
| Vendor assessment overdue | Scheduled — daily at 6 a.m. | Notify vendor contact + relationship owner; create overdue task |
| New regulatory finding added | Record Created on sn\_audit\_finding | Create linked Issue; assign to Control owner |
| Risk rating deteriorates (Medium → High) | Record Updated — residual\_rating | Re-route for CRO review via Approval action |
| Policy attestation deadline approaching | Scheduled — 14 days before due | Send reminder to all attestation respondents |
| SIEM alert threshold exceeded | Inbound Webhook from SIEM | Create cyber risk Issue; set severity based on SIEM score |

## In the video

* Walking through Flow Designer's interface and IRM-specific trigger options.
* Building the KRI red-threshold flow step by step, including lookup actions to pull the risk owner.
* Demonstrating the Issue auto-creation and notification in a live instance.
* Showing the SLA escalation path and how it surfaces in the CRO's queue.
* Testing the flow and reviewing the execution log.

## Key takeaways

* Flow Designer replaces manual monitoring by reacting to data changes in IRM tables in real time — no polling, no missed alerts.
* The KRI → Issue → SLA chain is the backbone of an automated risk response program and directly demonstrates control effectiveness to regulators.
* Always scope flows with conditions to avoid noise; a flow that fires too broadly generates alert fatigue and gets disabled by operations teams.
* Sub-flows enable reuse: build "Create IRM Issue" and "Notify Risk Owner" as sub-flows once, then call them from every parent flow.
* Document each active flow in your Control library as an automated control — it counts as evidence of your monitoring program during audits.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
