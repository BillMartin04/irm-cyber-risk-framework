---
description: Applying IRM in banking and financial services.
---

# Banking and Financial Services

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Banking and Financial Services — video placeholder
{% endembed %}

## Overview

Banking and financial services face the most complex and overlapping regulatory landscape of any industry — Basel III/IV operational risk capital requirements, OCC/Federal Reserve safety-and-soundness expectations, FFIEC examination guidance, and increasingly, SEC cyber-risk disclosure rules. IRM on ServiceNow is purpose-built for this environment: it provides a single, auditable system of record that connects first, second, and third lines of defense without duplicating data across siloed spreadsheets.

## Key concepts

* **Operational risk (OpRisk)** — Basel defines operational risk as the risk of loss resulting from inadequate or failed internal processes, people, systems, or external events. For a bank, this means mapping every critical process to its inherent and residual risk, tracking loss events, and maintaining documented control evidence — all of which ServiceNow IRM's Risk Register and Control Objectives modules support natively.
* **Three lines of defense** — The first line (business units) owns risk; the second line (risk and compliance functions) provides oversight and challenge; the third line (internal audit) provides independent assurance. ServiceNow Entity Profiles and scoped access roles map directly to this model, ensuring each line sees only what it should and can evidence its own activities.
* **Third-party/vendor risk (TPRM)** — Regulators — OCC Bulletin 2013-29, FFIEC guidance, and the EU's DORA regulation — require banks to demonstrate continuous oversight of critical third-party relationships. ServiceNow IRM's Third-Party Risk module allows vendor risk profiles, inherent-risk tiering, assessment questionnaires, and findings to be linked to the enterprise risk taxonomy.
* **CRI Profile** — The Cyber Risk Institute Profile (CRI Profile) is the financial-services sector adaptation of NIST CSF, co-developed by major U.S. banks and endorsed by the FSSCC. It maps directly to FFIEC CAT and OCC expectations. ServiceNow's CRI Profile content pack populates a baseline control library that banks can adopt, tailor, and use as the spine of their IRM program.
* **Regulatory examination management** — Examiners (OCC, Federal Reserve, FDIC, state regulators) issue Matters Requiring Attention (MRAs) and Matters Requiring Immediate Attention (MRIAs). These map to Findings and Issues in ServiceNow IRM, complete with remediation plans, due dates, ownership, and evidence attachments.
* **Continuous monitoring / KRIs** — Key Risk Indicators in ServiceNow IRM (the Indicators module) can be sourced from automated data feeds — transaction volumes, failed authentication counts, patch latency metrics — giving the second line a live risk dashboard rather than a quarterly snapshot.

## The ServiceNow IRM Model for Banking

The table below maps common banking risk domains to the specific ServiceNow IRM constructs used to manage them.

| Banking Risk Domain | ServiceNow IRM Construct | Example Artifact |
|---|---|---|
| Operational risk capital (AMA/SMA) | Risk Register → Risk Statements | Inherent/residual risk scores tied to Basel event types |
| Regulatory exam findings | Issues & Findings | MRA tracker with remediation milestone dates |
| Third-party concentration risk | Third-Party Risk Profile | Critical vendor heat map with inherent risk tier |
| IT/cyber risk | CRI Profile → Control Objectives | 150+ CRI Profile diagnostic statements |
| Business continuity | Advanced Risk → Scenario Analysis | BCP scenario with RTOs linked to critical processes |
| Policy compliance | Policy & Compliance module | Regulation-to-policy-to-control mapping |
| KRI monitoring | Indicators (KRI) module | Automated feed from SIEM: mean time to detect |

## Implementing Three Lines of Defense in ServiceNow

A practical implementation for a mid-size bank looks like this:

1. **Define the Entity hierarchy.** Create Entity Profiles for each business unit (e.g., Retail Banking, Treasury, Mortgage Origination, Payments). Each entity owns its risk profile and is assigned a designated first-line risk owner.
2. **Populate the Risk Register.** Import or build Risk Statements aligned to the bank's OpRisk taxonomy (credit, market, liquidity, operational, strategic, reputational). Tag each risk statement with the relevant Basel event type (Internal Fraud, External Fraud, CPBP, BDSF, etc.).
3. **Link Control Objectives.** Map each risk statement to the control objectives that mitigate it. Attach control testing schedules and evidence records. Controls tested by internal audit become second- and third-line assurance data points.
4. **Configure the Scoped Assessments.** Schedule quarterly self-assessments (RCSA — Risk and Control Self-Assessment) to push risk and control questions to first-line owners. Results feed directly into the risk register without re-keying data.
5. **Activate KRI feeds.** Connect KRI indicators to automated data sources where possible (ServiceNow IntegrationHub connectors, MID Server-based data pulls). Set thresholds with amber/red breach alerts that route to the second-line risk team.
6. **Map to CRI Profile.** Overlay the CRI Profile diagnostic statements as the control objective framework to align with FFIEC examination expectations and facilitate automated control scoring.

{% hint style="warning" %}
Regulators increasingly expect banks to demonstrate **continuous** monitoring — not just point-in-time assessments. Design your KRI feeds and automated control tests to produce evidence that is timestamped and immutable in ServiceNow's audit history.
{% endhint %}

## In the video

* Walking through a banking-specific Entity hierarchy in ServiceNow IRM — business unit to subsidiary to legal entity.
* Configuring an RCSA (Risk and Control Self-Assessment) workflow for a first-line business unit.
* Mapping the CRI Profile diagnostic statements to control objectives and running a gap assessment.
* Demonstrating an MRA tracker in the Issues & Findings module with regulatory exam workflow.
* Live demo of a KRI dashboard showing breach alerts and escalation routing.

## Key takeaways

* Banking IRM is non-negotiable — regulators examine your risk management framework as a core safety-and-soundness requirement, not a checkbox exercise.
* ServiceNow IRM maps to the three lines of defense model directly through Entity Profiles, scoped roles, and workflow-driven assessments.
* The CRI Profile is the fastest path to FFIEC/OCC alignment for U.S. banks — adopt it as your baseline control library rather than building from scratch.
* Third-party risk and regulatory examination management (MRA tracking) are two areas where a unified IRM platform pays for itself quickly versus spreadsheet-based programs.
* KRI automation is the difference between a lagging and a leading risk program — prioritize data feeds over manual KRI updates.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
