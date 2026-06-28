---
description: Produce an audit-ready evidence trail.
---

# Audit and Evidence Collection

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Audit and Evidence Collection — video placeholder
{% endembed %}

## Overview

Regulatory examinations in financial services are won or lost on evidence. When an OCC examiner or internal audit team asks whether your access control review is operating effectively, the answer is not a policy document — it is a timestamped artifact proving the review occurred, who performed it, what they found, and what was done about exceptions. ServiceNow's Audit Management module, integrated with IRM's Control and Risk frameworks, provides the infrastructure to collect, attach, and retain evidence at the time of control testing, then surface that evidence during engagement reviews without heroic last-minute preparation.

## Key concepts

* **Audit Engagement** — The top-level record (table: sn\_audit\_engagement) representing a single audit or examination cycle. An Engagement has a scope, audit team members, a status, and a collection of Audit Tasks.
* **Audit Task** — A discrete work item within an Engagement (table: sn\_audit\_task) assigned to an auditor or control tester. Tasks map to specific controls or risk areas and have a testing approach, sample size, and due date.
* **Evidence** — A record or attachment (table: sn\_audit\_evidence) that proves a control operated as designed during the test period. Evidence can be a file attachment (screenshot, log extract, report PDF), a record reference (linking to a specific transaction record in ServiceNow), or a URL to an external artifact.
* **Finding** — A documented control gap or exception identified during testing (table: sn\_audit\_finding). Findings carry a severity rating (Critical, High, Medium, Low), a root cause, and one or more Recommendations with target remediation dates.
* **Attestation** — A self-certification submitted by a control owner confirming that a control is operating, with supporting narrative. In IRM, attestations are collected through Policy Management's attestation workflow and can be linked to Audit Tasks as supporting evidence.
* **Work Papers** — The organized collection of Audit Tasks, evidence, findings, and auditor notes that constitute the complete record of an engagement. ServiceNow Audit Management maintains these in a structured, reviewable format accessible to the audit committee.
* **Continuous Controls Monitoring (CCM)** — The practice of running automated tests against control data on a recurring schedule, generating evidence and flagging exceptions without waiting for a formal audit cycle. In IRM, CCM uses Indicators and scheduled scripts to test controls between engagement cycles.

## Running an audit engagement end-to-end

This walkthrough follows a Type I SOX compliance audit for a publicly traded bank's IT General Controls (ITGCs), specifically the access management control domain.

### 1. Create the Audit Engagement

Navigate to **Audit Management > Engagements > New**. Set:

* **Name:** SOX ITGC Audit — Access Management — FY Q3
* **Type:** Compliance
* **Audit period:** 90-day quarter
* **Assigned auditors:** Lead IT auditor + two staff auditors
* **Related controls:** Link the engagement to the Access Management control objective in the Control Library

The engagement record becomes the container for all downstream work. Every task, piece of evidence, and finding created during this engagement is automatically scoped to it.

### 2. Create Audit Tasks and assign testing

Click **New Task** for each control under test. For the access management domain in a typical bank, this means tasks for:

| Control | Testing approach | Sample size |
|---|---|---|
| Privileged access reviews — core banking | Inspect quarterly review sign-off records | 25 users |
| New hire access provisioning timeliness | Test against HR joiner records | 30 joiners |
| Termination access revocation | Test deprovisioning within 24 hours | 30 leavers |
| MFA enforcement — remote access | Inspect system configuration + exception report | 100% population |
| Access recertification completeness | Verify all certifications completed before deadline | Full population |

Assign each task to a specific auditor and set a due date 10 days before the engagement close date (leaving time for finding review and management response).

### 3. Collect and attach evidence

For each Audit Task, the assigned auditor collects evidence and attaches it directly to the task record. ServiceNow supports multiple evidence types:

* **File attachments** — Upload the quarterly access review sign-off PDF directly to the task. The attachment is timestamped and associated with the auditor's user record.
* **Record references** — Link directly to the source ServiceNow records (e.g., the HR Offboarding task records for the 30 leavers tested) so reviewers can drill into the original data.
* **Screenshots** — For configuration evidence (MFA enforcement settings, firewall rules), a screenshot attached to the task with a date/time stamp is a widely accepted format.
* **Control Attestations** — If the control owner submitted a quarterly attestation through IRM's Policy Management module, the attestation record can be linked to the task as corroborating evidence.

{% hint style="warning" %}
Evidence must be collected at the time of testing, not reconstructed afterward. A common audit finding in financial services is evidence that was clearly assembled post-facto — date stamps inconsistent with the test period, versions that predate the test window. ServiceNow's timestamping makes this problem visible; it also makes honest evidence collection defensible.
{% endhint %}

### 4. Document findings and recommendations

When testing reveals an exception, the auditor creates a **Finding** record linked to the task. For example:

> *Finding: Access Recertification — 3 of 25 privileged accounts were not recertified within the required 30-day window. Root cause: Recertification tasks were sent to departed managers whose successors were not notified. Recommendation: Update recertification task routing to include the manager's designated backup.*
> *Severity: Medium. Target remediation date: 45 days.*

Findings are visible to control owners immediately. Control owners can post management responses, attach evidence of remediation, and request closure once remediation is complete. The auditor verifies and closes or re-opens accordingly.

### 5. Produce the audit report

Audit Management generates a structured summary of the engagement: tasks completed, evidence attached, findings by severity, and remediation status. Export this to PDF for the Audit Committee package. Because all underlying data is in ServiceNow, any Audit Committee member with appropriate access can drill through from the PDF summary back to the original evidence — a level of transparency that spreadsheet-based audit management cannot provide.

## In the video

* Navigating the Audit Management module and creating an engagement scoped to ITGC controls.
* Creating audit tasks with testing approaches and sample sizes.
* Attaching evidence — file upload, record reference, and attestation link.
* Creating a finding with root cause and recommendation, and showing the management response workflow.
* Generating the audit report and showing how it links back to the original evidence.
* Demonstrating a Continuous Controls Monitoring scheduled job that pre-populates evidence for routine controls between formal audit cycles.

## Key takeaways

* Evidence attached at the time of testing is the only evidence that holds up under examiner scrutiny — ServiceNow's timestamping and user attribution make this defensible.
* Linking Audit Tasks to Control Library records means every finding is automatically connected to the risk it relates to, giving the CRO and CISO line-of-sight from audit exception to residual risk impact.
* Management response workflow in Audit Management closes the loop between auditors and control owners without email chains — the entire dialogue is in the platform and visible to the audit committee.
* Continuous Controls Monitoring reduces point-in-time audit reliance; for high-frequency transactional controls (access reviews, patch compliance), automated evidence collection is more reliable than quarterly manual testing.
* A well-maintained Audit Management history is your best preparation for regulatory examinations — examiners can see not just current control status but the trend of findings and remediation velocity over multiple cycles.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
