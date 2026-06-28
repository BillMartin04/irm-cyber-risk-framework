---
description: Run control attestations and compliance checks.
---

# Compliance Assessments

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Compliance Assessments — video placeholder
{% endembed %}

## Overview

Compliance assessments in ServiceNow IRM test whether your controls are designed and operating effectively against a defined set of requirements. Unlike risk assessments — which score the probability and impact of risk events — compliance assessments ask a specific question about each control: is it in place, is it working, and can we demonstrate it? The answers feed directly into your residual risk picture, your regulatory reporting, and your audit evidence library. For a bank managing dozens of regulatory requirements simultaneously, the ability to run, track, and aggregate compliance attestations in a single platform — rather than across a stack of emailed spreadsheets — is one of the most tangible efficiency gains ServiceNow IRM delivers.

## Key concepts

- **Control Attestation** — A formal declaration by a control owner that a control is operating as designed within a specified period. ServiceNow generates an attestation task, routes it to the assigned control owner, collects a Pass/Fail/Partial response with comments and evidence, and timestamps the result on the control record.
- **Control Objective** — The desired state a set of controls is meant to achieve (e.g., "All customer data at rest is encrypted with AES-256"). A Control Objective can have multiple controls contributing to it; the compliance assessment evaluates each control and rolls up to an objective-level status.
- **Assessment Scope** — For compliance assessments, scope is typically defined by framework (e.g., all controls mapped to FFIEC Cybersecurity Assessment Tool), by entity (e.g., controls scoped to the Mortgage Origination business unit), or by regulatory requirement (e.g., controls tagged to PCI DSS Requirement 8).
- **Design Effectiveness vs Operating Effectiveness** — Design effectiveness asks whether the control, as documented, is capable of meeting its objective. Operating effectiveness asks whether it is actually being executed as designed. ServiceNow assessments can be configured to test either or both, with separate response fields and evidence requirements.
- **Compliance Posture** — The aggregate view of control assessment results across a framework or entity. In the ServiceNow Policy & Compliance dashboard, compliance posture is expressed as a percentage of controls passing, with drill-down by objective, category, or regulatory requirement.
- **Policy Statements and Authority Documents** — The regulatory source material that controls are mapped to. An authority document in ServiceNow represents a regulatory framework (FFIEC, NIST CSF, ISO 27001); policy statements are the specific requirements within it. Controls inherit their compliance obligations from these mappings.
- **Evidence Attachment** — Each attestation response in ServiceNow allows the control owner to attach supporting evidence — screenshots, logs, reports, or documents — directly to the assessment record. Evidence is timestamped, attributed to the attester, and immediately available for audit review.

## Running a compliance assessment: annual cyber controls attestation

The following scenario describes a bank's annual cybersecurity controls attestation for its FFIEC Cybersecurity Assessment Tool (CAT) obligations.

**Configure the assessment scope**

Navigate to Policy and Compliance > Assessments > New. Select "Compliance Assessment" as the type. Set the authority document to "FFIEC Cybersecurity Assessment Tool" and the scope to "All entities — Cybersecurity controls." ServiceNow pulls in all controls mapped to the FFIEC CAT — in a typical mid-size bank deployment, this is 80 to 120 control records across five FFIEC maturity domains.

**Assign control owners**

Each control record has a designated owner — the person responsible for operating the control. ServiceNow assigns attestation tasks to each control owner automatically based on this field. In a bank with controls distributed across IT, Operations, Compliance, and Risk, this means 15 to 20 different respondents receive tasks without any manual distribution.

**Set the attestation window**

Configure the assessment start and end dates. Set automated reminders at 14 days, 7 days, and 2 days before the deadline. Control owners receive email notifications with direct links to their task queues; no logins to SharePoint or email attachments required.

**Capture attestation results**

Each control owner completes their task by selecting a status (Effective, Partially Effective, Ineffective, Not Applicable), providing a brief narrative explanation, and attaching evidence. For a Partially Effective or Ineffective response, ServiceNow prompts for a root cause description and optionally initiates an Issue record.

**Review and challenge**

The second-line Compliance team has a reviewer role. They can view all completed attestations, add comments, challenge a self-reported "Effective" rating where other evidence (KRI data, recent incidents, audit findings) suggests a different picture, and return individual items for re-attestation.

**Aggregate and report**

Once all attestations are completed and reviewed, the assessment status moves to "Final." The compliance posture dashboard updates to show the FFIEC CAT results by domain:

| FFIEC CAT Domain | Controls Tested | Effective | Partially Effective | Ineffective |
|---|---|---|---|---|
| Cyber Risk Management & Oversight | 18 | 15 | 2 | 1 |
| Threat Intelligence & Collaboration | 12 | 11 | 1 | 0 |
| Cybersecurity Controls | 42 | 38 | 3 | 1 |
| External Dependency Management | 16 | 13 | 2 | 1 |
| Cyber Incident Management & Resilience | 14 | 14 | 0 | 0 |

This output is generated directly from the assessment records — no manual compilation.

**Link failures to risk and remediation**

The two Ineffective and eight Partially Effective controls automatically generate Issues in ServiceNow, pre-linked to the underlying control records and risk entries. Remediation owners are assigned, due dates are set, and the compliance posture dashboard will update in real time as issues are resolved and re-attestation occurs.

{% hint style="warning" %}
**Common mistake**: Running compliance assessments without first ensuring your controls are mapped to authority documents. Without those mappings, you collect attestation results but cannot demonstrate regulatory coverage — the primary purpose of the exercise. Map your framework before you run the assessment.
{% endhint %}

## In the video

- Creating a compliance assessment scoped to a specific authority document in ServiceNow.
- The control owner experience: completing an attestation task with evidence attachment.
- The second-line reviewer experience: challenging a self-reported result.
- Reading the compliance posture dashboard by domain and identifying gaps.
- How failed attestations automatically create Issues linked to control and risk records.

## Key takeaways

- ServiceNow compliance assessments test both design and operating effectiveness of controls, capturing responses, evidence, and reviewer comments on a single timestamped record.
- Assessment scope tied to authority documents enables regulatory coverage mapping — you can demonstrate which controls address which regulatory requirements, which regulators increasingly require.
- The aggregate compliance posture view is the primary output: a percentage-based breakdown of control effectiveness by framework domain, entity, or requirement category.
- Failed attestations automatically trigger Issue creation and remediation workflows — the assessment is the beginning of the remediation cycle, not the end.
- Evidence attached to attestation records at completion time is immediately available for regulatory exam or internal audit review, eliminating the reactive evidence-gathering scramble.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
