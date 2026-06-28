---
description: Assess vendors and third-party risk.
---

# Vendor and Third-Party Risk

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Vendor and Third-Party Risk — video placeholder
{% endembed %}

## Overview

Third-party risk is consistently among the top five operational risk concerns cited in OCC, Federal Reserve, and FDIC examination findings for financial institutions. The reason is structural: banks and asset managers have outsourced critical functions — core banking, payment processing, cloud infrastructure, fraud detection — to vendors whose failures can directly impair their ability to serve customers and meet regulatory obligations. ServiceNow's Vendor Risk Management (VRM) module, part of the IRM suite, provides a structured lifecycle for identifying, tiering, assessing, and continuously monitoring third-party relationships at scale.

## Key concepts

* **Vendor (Supplier)** — In ServiceNow VRM, vendors are stored as Company records with a Vendor Risk profile attached. Each profile captures tiering, relationship owner, criticality classification, and the list of associated Engagements (assessment instances).
* **Engagement** — The core VRM record (table: sn\_vendorrisk\_engagement) representing a single assessment cycle for a vendor. An Engagement has a type (Initial Due Diligence, Periodic Review, Triggered Review), a due date, a status, and a collection of Questionnaire responses.
* **Vendor Tiering** — A criticality classification that drives assessment frequency and depth. Tier 1 vendors provide services critical to core banking functions or handle sensitive customer data; they receive annual in-depth assessments. Tier 2 and 3 vendors receive lighter-touch reviews on a less frequent cycle.
* **Assessment Questionnaire** — A structured set of questions sent to the vendor via the VRM portal or email. Question sets can be mapped to control frameworks (e.g., SOC 2 control areas, NIST CSF categories, or your internal Third-Party Risk Policy) and scored automatically upon response submission.
* **Inherent Risk Scoring** — Before sending a questionnaire, VRM calculates an inherent risk score based on factors like data access, geographic location, regulatory status, and service criticality. This score determines which questionnaire template is sent and which controls to test.
* **Residual Risk** — After questionnaire responses are scored and any compensating controls noted, VRM calculates a residual vendor risk score. High residual scores auto-escalate for human review before the Engagement can be closed.
* **Issues and Findings** — When questionnaire responses reveal gaps (e.g., the vendor has no documented incident response plan, or their SOC 2 report is more than 14 months old), VRM creates Issue records linked to the vendor and the relevant control, tracking remediation to closure.
* **Continuous Monitoring** — VRM integrates with external threat intelligence feeds (e.g., BitSight, SecurityScorecard) to pull vendor cyber risk scores into ServiceNow automatically, updating the vendor's risk profile between assessment cycles.

## The VRM lifecycle in a banking context

The following walkthrough covers the end-to-end VRM process for onboarding a new fintech payment processor — a scenario that is both common and high-risk in retail banking.

### 1. Create the Vendor record and set the tier

Navigate to **Vendor Risk > Vendors > New**. Enter the vendor's legal name, primary contact, and country of incorporation. On the **Risk Profile** tab, set:

* **Service type:** Payment Processing
* **Data classification:** Confidential (PII + financial account data)
* **Tier:** 1 (because this vendor processes customer payment transactions)

Save the record. VRM will now flag this vendor for annual Tier 1 assessments.

### 2. Initiate an Initial Due Diligence Engagement

Click **New Engagement** on the vendor record. Set the type to *Initial Due Diligence* and assign it to the Third-Party Risk Manager responsible for fintech relationships. VRM calculates the inherent risk score automatically and selects the appropriate questionnaire template — in this case, the full Payment Processing template covering NIST CSF, PCI DSS control areas, and your internal Vendor Risk Policy.

### 3. Send the questionnaire

Click **Send Questionnaire**. VRM emails the vendor a link to the self-service portal where they complete the assessment and attach supporting evidence (SOC 2 Type II report, penetration test summary, business continuity plan). The portal supports document uploads and provides vendor contacts with a clean interface that requires no ServiceNow license.

Set a **response due date** 10 business days out. Flow Designer automation (see the Automated Risk Responses page) will send reminders at day 5 and escalate at day 10 if the vendor has not submitted.

### 4. Review responses and score

When the vendor submits, VRM automatically scores each response against the expected answer key and flags any that fall below the minimum threshold. The Third-Party Risk Manager reviews flagged responses and can:

* Accept the response with a compensating control noted
* Create a **Finding** requiring remediation by a specific date
* Downgrade the vendor's residual risk score, triggering an escalation to the CRO

For a payment processor with a clean SOC 2 Type II report and strong PCI DSS evidence, most responses will auto-approve and the residual score will land in the acceptable range.

### 5. Link vendor risk to the enterprise Risk Register

This is the step most VRM implementations skip, and it is the reason regulators push back. On the completed Engagement record, navigate to **Related Risks** and link the vendor's residual risk to the corresponding enterprise risk statement — for example, "Operational Risk: Payment Processing Failure due to Third-Party Dependency." This link means the enterprise risk's residual rating now accounts for vendor health, and the board dashboard (built in the previous page) will reflect deteriorating vendor risk without additional manual intervention.

### 6. Schedule periodic reviews

Set the vendor's **Next Assessment Date** to 12 months from the Engagement close date. VRM will automatically create the next Engagement record 30 days before that date and trigger the outreach workflow.

{% hint style="info" %}
For Tier 1 vendors that process payment or custody data, also configure **Continuous Monitoring** by connecting a BitSight or SecurityScorecard integration. When the external cyber score drops below your threshold, VRM creates a Triggered Review Engagement automatically — no waiting for the annual cycle.
{% endhint %}

## Tiering framework for financial services

| Tier | Criteria | Assessment frequency | Questionnaire depth |
|---|---|---|---|
| 1 | Core banking functions; PII/financial data; systemic failure impact | Annual full assessment + continuous monitoring | Full framework (NIST, SOC 2, BCP, PCI) |
| 2 | Important but non-critical services; limited data access | Biennial full + annual attestation | Targeted (InfoSec + BCP sections) |
| 3 | Low criticality; no sensitive data; replaceable within 30 days | Triennial or risk-triggered only | Abbreviated (InfoSec basics) |
| 4 | Commodity vendors (utilities, office supplies) | Registration only | None required |

## In the video

* Navigating the ServiceNow VRM module and vendor record structure.
* Creating a Tier 1 vendor profile and initiating an Initial Due Diligence Engagement.
* Sending the questionnaire through the vendor portal and reviewing auto-scored responses.
* Creating Findings for gaps and linking remediation tasks to Issues.
* Connecting vendor residual risk to the enterprise Risk Register.
* Configuring the periodic review schedule and showing how a Triggered Review fires when a cyber score drops.

## Key takeaways

* Vendor tiering is the foundation of an efficient VRM program — not every vendor needs the same depth of assessment, and over-assessing Tier 3 vendors burns capacity that should go to Tier 1.
* The Engagement record is the audit artifact: it captures the questionnaire, responses, evidence, scores, and findings in one immutable record that examiners can review directly.
* Linking vendor risk back to the enterprise Risk Register closes the loop between third-party risk and enterprise risk posture — without this link, VRM operates as an isolated silo.
* Continuous monitoring via external cyber scoring services changes VRM from a point-in-time exercise to a live surveillance capability, which is increasingly expected by DORA, OCC, and Fed examiners.
* Flow Designer automation for overdue questionnaire reminders and triggered reviews eliminates the manual calendar-watching that causes third-party risk programs to fall behind.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
