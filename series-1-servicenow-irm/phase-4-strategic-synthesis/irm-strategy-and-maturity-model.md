---
description: Tie it together into a strategy and maturity roadmap.
---

# IRM Strategy and Maturity Model

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
IRM Strategy and Maturity Model — video placeholder
{% endembed %}

## Overview

An IRM maturity model provides a structured lens for evaluating where a risk management program stands today and what investments are needed to reach the next level. For financial services organizations, maturity assessment serves a dual purpose: it is an internal planning tool and an external communication vehicle. Boards want to understand their risk program's effectiveness; regulators want to see evidence of continuous improvement. A five-level maturity model — anchored to real platform capabilities in ServiceNow IRM — gives both audiences a credible, measurable framework.

## Key concepts

* **Maturity Level** — A stage descriptor that characterizes the predominant approach to IRM at a given point in time. Levels are cumulative: each level builds on the capabilities of the level below.
* **Capability Domain** — A distinct dimension of IRM capability evaluated independently (e.g., Risk Identification, Control Management, Monitoring). Assessing each domain separately produces a more honest picture than a single composite score that masks weak areas.
* **Risk Appetite Integration** — A hallmark of higher maturity levels. At Level 1, risk appetite exists in a board policy document that nobody references operationally. At Level 4, risk appetite thresholds are embedded directly in KRI configurations, and the platform enforces them automatically.
* **Three Lines of Defense Alignment** — The degree to which first-line business units, second-line risk functions, and third-line internal audit operate from a shared platform and shared data set. Low maturity means each line maintains its own records; high maturity means all three lines contribute to and consume the same IRM environment.
* **Continuous Controls Monitoring (CCM)** — The automated, ongoing testing of controls outside of formal audit cycles. Moving from periodic to continuous monitoring is one of the most impactful maturity leaps a financial institution can make, and ServiceNow IRM's Indicators and Flow Designer automation make it achievable without a custom development project.
* **Strategic Risk Reporting** — Board and executive reporting that contextualizes risk posture against business strategy, not just against compliance checklists. At higher maturity levels, the CRO can show the board how operational risk metrics correlate with business performance indicators.

## IRM Maturity Model: Levels 1–5

The following table describes each level across five capability domains. Use this as a self-assessment checklist: for each domain, identify which level description best matches your current state.

| Level | Governance & Culture | Risk Identification | Control Management | Monitoring & Reporting | Third-Party & Audit |
|---|---|---|---|---|---|
| **1 — Ad Hoc** | Risk management is reactive; no formal program; responsibilities informal. | Risks identified after incidents; no structured Risk Register; spreadsheet-based. | Controls documented in policy documents only; no testing cadence; no evidence. | No regular reporting; risk updates produced manually for audits only. | Vendor risk managed through contracts only; no assessments; no audit program. |
| **2 — Defined** | IRM policy and charter exist; roles assigned (CRO, Risk Owners); program documented but not consistently followed. | Risk Register created in a structured tool (ServiceNow); risk statements documented with likelihood and impact ratings. | Control library established and linked to risks; annual control testing scheduled; some evidence collected. | Quarterly risk reports produced; KRIs defined but thresholds informal; dashboard exists but manually refreshed. | Vendor inventory maintained; Tier 1 vendors assessed annually; internal audit plan documented. |
| **3 — Managed** | Risk appetite statement approved by board; three lines of defense operating with defined handoffs; IRM training program active. | Risk assessments run on a scheduled cycle; entity-level risk profiles completed; risk taxonomy standardized across the enterprise. | Controls tested against defined testing procedures; evidence attached to control records in ServiceNow; failed controls generate Issues with remediation tracking. | Performance Analytics configured; KRI thresholds linked to Risk Appetite Statement; automated notifications on threshold breaches; dashboards role-differentiated. | Vendor tiering completed; Tier 1 and 2 vendors on structured assessment cycles; VRM Engagements in ServiceNow; vendor findings tracked to closure. Audit engagements in Audit Management with evidence attached. |
| **4 — Quantified** | Risk appetite integrated into platform KRI configurations; risk decisions documented with quantitative inputs; board receives live dashboards, not static PDFs. | Scenario analysis and stress testing inform risk ratings; Advanced Risk module in use; CRI Profile active for cyber risk; risk-to-strategy mapping documented. | Continuous Controls Monitoring running for high-frequency controls; control effectiveness trending tracked over time; compensating controls evaluated quantitatively. | Real-time executive dashboards; KRI trend analysis informs CRO decisions; automated risk re-assessment triggered by material issue closure; regulatory reporting automated. | Continuous monitoring via external cyber scoring (BitSight/SecurityScorecard); triggered reviews fire automatically on score deterioration; audit findings linked to residual risk ratings; CCM replaces periodic testing for automated controls. |
| **5 — Optimizing** | IRM is embedded in strategic planning and product/service launch decisions; risk culture measurable and reported to board; program continuously benchmarked against industry peers. | Predictive risk indicators in use; emerging risk program feeds new threats into the Risk Register before they materialize; scenario library maintained and updated quarterly. | Control design reviewed against emerging threats annually; control rationalization program active (removing redundant controls, consolidating coverage gaps). | Risk intelligence feeds inform real-time posture adjustments; IRM metrics linked to business performance KPIs; board risk committee decisions traceable to risk data. | Fourth-party risk monitoring active; vendor ecosystem risk mapped; audit program covers emerging risk areas (AI model risk, crypto custody) not just historical control domains. |

## Conducting a maturity assessment

Run your assessment as a structured workshop with key stakeholders: the CRO, CISO, Head of Internal Audit, and first-line business risk leads. For each domain, review the level descriptions and agree on the current state. Document the evidence that supports your assessment — you will need it when an examiner asks.

### Common findings in regional banks

Based on typical assessment patterns in mid-size financial institutions:

* **Governance** often lands at Level 2–3: the policy and structure exist, but cultural embedding is incomplete — business units treat risk reporting as a compliance exercise, not a management tool.
* **Risk Identification** varies widely: organizations that have completed an enterprise RCSA (Risk and Control Self-Assessment) in ServiceNow are typically at Level 3; those still running RCSA in spreadsheets are at Level 1–2 regardless of how good their policy says they are.
* **Control Management** is commonly the gap: controls are documented but not tested, or tested but without evidence attached to the record. This is the most common examiner finding.
* **Monitoring** tends to be the clearest maturity indicator: the presence of live, threshold-driven KRI dashboards in ServiceNow is a Level 3 signal; the absence of them, regardless of other program elements, is a Level 2 ceiling.
* **Third-Party & Audit** is split: large banks with formal VRM programs may be at Level 4 for vendor risk but Level 2 for audit (engagements run in a separate GRC tool with no connection to the IRM Risk Register).

## Building the IRM strategy roadmap

Once maturity levels are documented by domain, the roadmap writes itself: for each domain, identify the gap between current level and target level, define the platform configurations, process changes, and governance actions required to close the gap, and assign an owner and timeline.

Present the roadmap as a 12/24/36-month view. Regulators and board audit committees respond well to a roadmap that is specific (named projects, owners, completion dates) rather than aspirational (general commitments to "improve risk culture"). ServiceNow's road-map tracking can host the initiative list as Issues or Tasks, keeping the program accountable.

## In the video

* Walking through the five-level maturity model and scoring each domain for a sample regional bank.
* Using ServiceNow IRM data — control test results, KRI trends, audit finding history — as evidence inputs to the assessment.
* Building a 24-month roadmap from a Level 2/3 baseline to a Level 4 target.
* Structuring a board presentation that communicates maturity trajectory without technical jargon.
* Discussing how regulators (OCC, Federal Reserve, DORA) interpret maturity self-assessments and what they look for.

## Key takeaways

* A domain-by-domain assessment produces a more actionable picture than a single composite maturity score — most programs are Level 3 in some areas and Level 1 in others.
* Platform capabilities in ServiceNow IRM map directly to maturity levels: live KRI dashboards = Level 3 monitoring; CCM = Level 4; predictive indicators = Level 5.
* Overstating maturity is a credibility risk with examiners; an honest Level 2 assessment with a credible roadmap is stronger than an unsupported Level 4 claim.
* The IRM strategy roadmap should be a living document, updated annually and reviewed by the board risk committee — not a one-time artifact produced for an examination.
* Achieving Level 4 in ServiceNow IRM is realistic for most financial institutions within 24–36 months; Level 5 requires cultural and strategic embedding that takes longer and cannot be accelerated by platform investment alone.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
