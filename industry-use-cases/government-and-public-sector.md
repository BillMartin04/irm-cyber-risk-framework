---
description: Applying IRM in government and public sector.
---

# Government and Public Sector

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Government and Public Sector — video placeholder
{% endembed %}

## Overview

Federal agencies, state/local governments, and cloud service providers pursuing FedRAMP authorization operate under the most prescriptive risk management framework in existence: the NIST Risk Management Framework (RMF), anchored by NIST SP 800-53. The ATO (Authority to Operate) process — and its evolution into Continuous Authorization and Monitoring (CAM) — demands a living, continuously-maintained risk posture, not a point-in-time audit artifact. ServiceNow IRM's Continuous Authorization and Monitoring (CAM) module is purpose-built to replace the static POAM spreadsheet with a dynamic, workflow-driven system of record.

## Key concepts

* **NIST SP 800-53 (Rev. 5)** — The definitive catalog of security and privacy controls for federal information systems. Rev. 5 introduced privacy controls as a co-equal concern and restructured controls into 20 families (AC, AT, AU, CA, CM, CP, IA, IR, MA, MP, PE, PL, PM, PS, PT, RA, SA, SC, SI, SR). ServiceNow's NIST 800-53 content pack maps all control families to Control Objectives, each with assessment procedures.
* **NIST Risk Management Framework (RMF)** — The six-step process: (1) Prepare, (2) Categorize, (3) Select, (4) Implement, (5) Assess, (6) Authorize, plus Continuous Monitoring. ServiceNow IRM's workflow and assessment engine maps directly to Steps 4–6 and the ongoing monitoring step.
* **FedRAMP** — The Federal Risk and Authorization Management Program standardizes cloud security authorization for cloud service providers (CSPs) selling to federal agencies. FedRAMP baselines (Low, Moderate, High) derive from NIST 800-53 control sets with additional FedRAMP-specific parameters. The FedRAMP Marketplace lists authorized CSPs, and their Packages include the System Security Plan (SSP), Security Assessment Report (SAR), and POAM — all of which have ServiceNow IRM analogs.
* **Authority to Operate (ATO)** — The formal decision by an Authorizing Official (AO) that a system's residual risk is acceptable for operation. The ATO package includes the SSP, Security Assessment Report (SAR), and Plan of Action and Milestones (POAM). ServiceNow IRM produces each of these as reports from live system data rather than static documents.
* **Plan of Action and Milestones (POAM)** — The POAM is the remediation register for open control weaknesses and findings. In ServiceNow IRM, the POAM maps to Issues & Findings with scheduled milestones, owner assignments, and status tracking — fed by assessment results rather than manually re-keyed from spreadsheets.
* **Continuous Authorization and Monitoring (CAM)** — OMB M-22-09 and CISA's Zero Trust guidance push agencies away from triennial ATOs toward ongoing monitoring with real-time risk visibility. ServiceNow's CAM module implements automated control monitoring, KRI feeds, and risk scoring that update the AO's risk picture continuously rather than at 3-year intervals.
* **System Security Plan (SSP)** — The SSP documents the authorization boundary, system components, and implementation details for every selected control. In ServiceNow IRM, Entity Profiles + Control Objectives + Implementation Statements together constitute the SSP data model.
* **Impact Categorization (FIPS 199)** — Federal systems are categorized as Low, Moderate, or High impact based on confidentiality, integrity, and availability consequences of a breach. The categorization drives the 800-53 control baseline selection. ServiceNow Entity Profiles capture FIPS 199 categorization alongside system metadata.

## RMF Implementation in ServiceNow IRM: Steps and Artifacts

| RMF Step | Key Activity | ServiceNow IRM Artifact |
|---|---|---|
| 1 — Prepare | Establish risk management roles, strategy, and organizational common controls | Entity Profiles, Risk Strategy documentation |
| 2 — Categorize | FIPS 199 categorization of system | Entity Profile: impact level field |
| 3 — Select | Choose 800-53 control baseline (Low/Mod/High) | Control Objectives (NIST 800-53 content pack) |
| 4 — Implement | Document control implementation in SSP | Control Objectives → Implementation statements |
| 5 — Assess | Test controls, produce SAR, identify weaknesses | Risk Assessments → Findings |
| 6 — Authorize | AO reviews risk, signs ATO | Risk Register summary → ATO decision record |
| Monitor | Ongoing control monitoring, POAM management, annual reviews | CAM module, Issues & Findings (POAM), KRIs |

## Continuous Authorization and Monitoring in Practice

Traditional ATO processes produced a risk posture frozen at the moment of assessment. The shift to CAM requires that agencies maintain a real-time or near-real-time view of their risk posture. In ServiceNow IRM, this means:

1. **Automate control tests where possible.** Use ServiceNow IntegrationHub connectors to pull evidence from Tenable/Nessus (vulnerability scanning), Splunk (log review), or configuration management databases. Control test results feed directly into the assessment record, timestamped and attributable.
2. **Configure KRI thresholds.** Set up Indicators for metrics such as: percentage of critical vulnerabilities remediated within SLA, mean time to patch, percentage of controls tested within 12 months. Breach of a threshold triggers a workflow to the system owner and ISSO.
3. **Manage the POAM dynamically.** Every finding from a control assessment automatically generates an Issue record. Milestones are tracked in real time; overdue items escalate to the ISSO and AO. The live POAM replaces the quarterly spreadsheet submission.
4. **Annual review reporting.** Generate the updated POAM, control test summary, and risk score trend report from ServiceNow at any point — the AO can review the live risk posture rather than waiting for a scheduled assessment.

{% hint style="info" %}
For FedRAMP-authorized cloud services, the CSP must demonstrate continuous monitoring activities to the JAB or Agency AO on a monthly/annual cadence. A ServiceNow CAM implementation satisfies this evidence requirement with automated report generation directly from the assessment and POAM data.
{% endhint %}

## In the video

* Walking through NIST 800-53 Rev. 5 control families and how they load into ServiceNow as a control baseline.
* Configuring an Entity Profile for a federal system with FIPS 199 categorization and authorization boundary documentation.
* Running a control assessment that generates POAM findings automatically in the Issues & Findings module.
* Demonstrating the CAM dashboard — live control test status, POAM aging, and KRI thresholds.
* Producing an ATO package summary report from live ServiceNow data.

## Key takeaways

* NIST RMF's six steps map almost 1:1 to ServiceNow IRM's data model — Entity Profiles, Control Objectives, Assessments, Findings, and Issues.
* The shift from triennial ATOs to Continuous Authorization and Monitoring (OMB M-22-09) is a forcing function: agencies that rely on spreadsheet-based POAMs will struggle to demonstrate continuous monitoring evidence.
* NIST 800-53 Rev. 5's 20 control families are all available as a content pack in ServiceNow — start there rather than building a custom control library.
* FedRAMP CSPs should align their ServiceNow IRM implementation to the FedRAMP POAM template structure so that monthly ConMon deliverables can be exported directly.
* KRI automation is the practical mechanism for continuous monitoring — manual quarterly data collection does not satisfy the spirit of CAM requirements.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
