---
description: Reusable templates and downloads.
---

# Templates and Downloads

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Templates and Downloads — video placeholder
{% endembed %}

## Overview

The templates in this collection are designed to accelerate the early stages of an IRM implementation — before your ServiceNow platform is fully configured and while you are still defining scope, taxonomy, and operating model. They are also useful as input documents for populating ServiceNow records via import sets, or as standalone artifacts for organizations that need deliverables in Office format for stakeholder review and sign-off.

## Template Catalog

| Template | Format | Use Case |
|---|---|---|
| Risk Register Starter | XLSX | Initial risk identification workshop; import set source for Risk Statements |
| Control Objective Library (NIST CSF) | XLSX | Control library baseline for non-regulated environments; maps to CSF Functions and Categories |
| Control Objective Library (CRI Profile) | XLSX | Control library baseline for financial services; maps to CRI Profile tiers and FFIEC CAT |
| RCSA Questionnaire | XLSX/DOCX | Risk and Control Self-Assessment for first-line business units; pre-formatted for stakeholder distribution |
| Third-Party Risk Assessment Questionnaire | XLSX | Vendor due diligence questionnaire; Tier 1 (Critical) and Tier 2 (High) versions |
| Risk Appetite and Tolerance Statement | DOCX | Board/executive-level risk appetite framework with editable risk tolerance thresholds |
| Information Security Policy Template | DOCX | Baseline IS policy covering access control, incident response, change management, and acceptable use |
| POAM Tracker | XLSX | Plan of Action and Milestones template aligned to NIST RMF structure; FedRAMP-compatible columns |
| IRM RACI Matrix | XLSX | Responsibility matrix for IRM program roles — first/second/third line and IT ownership |
| Assessment Report Template | DOCX/PPTX | Executive-ready risk assessment findings report with risk heat map placeholder and remediation summary |
| Vendor Risk Tiering Criteria | XLSX | Criteria-based scoring sheet for initial vendor risk tier classification |
| KRI Design Worksheet | XLSX | Structured worksheet for defining a KRI: metric name, data source, calculation method, thresholds, owner |

## Key concepts

* **Import set compatibility** — The XLSX templates for Risk Register, Control Objective Library, and POAM Tracker include column headers that match the import set transform maps included in the companion update sets. You can populate the spreadsheet in a workshop, then load it directly into ServiceNow without manual re-entry.
* **Versioning** — Templates are versioned alongside the handbook. The version number appears in the filename (e.g., `risk-register-starter-v1.2.xlsx`). Check the GitHub repository for the latest version before using in a new engagement.
* **Adapting for your organization** — Every template is structured as a starting point, not a final artifact. Column headers, risk categories, control families, and assessment criteria should be adapted to reflect your organization's risk taxonomy and the regulatory frameworks you operate under.
* **Executive report templates** — The Assessment Report Template (PPTX version) is formatted for a 15-minute executive briefing — one slide for context, one for the risk heat map, one for top findings, one for remediation plan summary. It has been used in actual board-level risk committee presentations.

{% hint style="info" %}
When using the RCSA Questionnaire with first-line business units, pilot it with one business unit before broad rollout. Business users will surface ambiguous questions that an IRM practitioner would not anticipate — a pilot cycle improves response quality significantly.
{% endhint %}

## In the video

* Downloading and populating the Risk Register Starter template in an IRM scoping workshop.
* Using the import set transform map to load completed Risk Register data directly into ServiceNow.
* Adapting the Assessment Report PPTX template for a quarterly risk committee briefing.
* Demonstrating the KRI Design Worksheet as a pre-configuration planning tool before building Indicator records in ServiceNow.

## Key takeaways

* Templates accelerate the design phase and serve as import sources for populating ServiceNow records at scale.
* The XLSX import set-compatible templates (Risk Register, Control Library, POAM Tracker) directly reduce data-entry effort during initial implementation.
* Always adapt templates to your organization's taxonomy before distributing to stakeholders — generic labels create confusion in workshops.
* The Executive Assessment Report template (PPTX) is consistently the highest-value deliverable for communicating IRM program status to senior leadership.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
