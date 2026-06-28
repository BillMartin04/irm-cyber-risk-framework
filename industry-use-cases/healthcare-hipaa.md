---
description: Applying IRM in healthcare under HIPAA.
---

# Healthcare (HIPAA)

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Healthcare (HIPAA) — video placeholder
{% endembed %}

## Overview

The HIPAA Security Rule imposes a legally mandated risk analysis and risk management process on every Covered Entity and Business Associate that creates, receives, maintains, or transmits electronic Protected Health Information (ePHI). Unlike most frameworks where risk assessments are best practice, under HIPAA they are a regulatory requirement — OCR (Office for Civil Rights) enforcement actions and breach investigations routinely cite failure to conduct an adequate risk analysis as a primary finding. ServiceNow IRM operationalizes this requirement with a repeatable, auditable program rather than a periodic consulting engagement.

## Key concepts

* **HIPAA Security Rule (45 CFR §164.308–§164.312)** — The Security Rule is organized into Administrative Safeguards (§164.308), Physical Safeguards (§164.310), and Technical Safeguards (§164.312), plus Organizational Requirements and Documentation. Each safeguard contains Required and Addressable implementation specifications. IRM maps these to Control Objectives — Required specs have mandatory controls; Addressable specs require a documented rationale if not implemented.
* **Risk Analysis (§164.308(a)(1)(ii)(A))** — HIPAA requires an accurate and thorough assessment of the potential risks and vulnerabilities to the confidentiality, integrity, and availability of ePHI. ServiceNow's Risk Assessment module formalizes this as a scoped assessment against a healthcare-specific risk register, producing a risk score for each ePHI system or process.
* **Risk Management (§164.308(a)(1)(ii)(B))** — The risk management requirement is the remediation side: implementing security measures sufficient to reduce risks to a reasonable and appropriate level. In ServiceNow IRM, this means Issues with assigned owners, remediation plans, target dates, and evidence of closure.
* **Protected Health Information (PHI/ePHI)** — Any individually identifiable health information transmitted or maintained electronically. The scope of a risk analysis is defined by where ePHI exists — mapping ePHI data flows to Entity Profiles in ServiceNow (EHR systems, medical devices, cloud services, Business Associates) is the foundational step.
* **Business Associate Agreements (BAAs)** — Vendors who access ePHI on a Covered Entity's behalf must have a signed BAA. ServiceNow's Third-Party Risk module tracks BAA status, inherent risk tier, and periodic vendor assessments alongside the enterprise risk register.
* **Breach Notification Rule (45 CFR §164.400–§164.414)** — Covered Entities must notify affected individuals, HHS, and sometimes media within 60 days of discovery of a breach of unsecured PHI. ServiceNow Issues & Findings can be configured to trigger a breach notification workflow on discovery.
* **OCR Resolution Agreements** — OCR publishes enforcement actions. Recent settlements consistently cite inadequate risk analysis, lack of access controls, and failure to monitor systems with ePHI access. These directly inform the control objective priorities in an IRM healthcare deployment.

## Structuring a HIPAA Risk Analysis in ServiceNow IRM

A HIPAA-compliant risk analysis in ServiceNow follows this sequence:

1. **Map ePHI scope.** Create Entity Profiles for each system, application, and third-party relationship that touches ePHI — EHR, revenue cycle management, medical imaging (PACS), cloud backups, telehealth platforms, and Business Associates. This is the asset inventory underpinning the risk analysis.
2. **Build the Risk Register.** Populate Risk Statements aligned to HIPAA Security Rule safeguards and common threat/vulnerability pairs. Example risk statements:
   - *Unauthorized access to ePHI due to excessive user account privileges (§164.308(a)(4))*
   - *Loss of ePHI availability due to inadequate backup and recovery controls (§164.308(a)(7))*
   - *Interception of ePHI in transit due to absence of encryption (§164.312(e)(1))*
3. **Link Control Objectives.** Map each risk statement to the specific safeguard and implementation specification it mitigates. Tag Required vs. Addressable. For Addressable specs where a control is not implemented, document the rationale in the control record — this is the evidence OCR will look for.
4. **Score inherent and residual risk.** Use a consistent scoring methodology (Likelihood × Impact). NIST SP 800-30 provides a healthcare-appropriate scoring approach that is widely accepted by OCR auditors.
5. **Issue remediation tasks.** Any risk rated High or Critical generates an Issue with an assigned owner, remediation steps, and a target closure date. Evidence of remediation (screenshots, configuration exports, policy sign-offs) attaches to the Issue record.
6. **Document the analysis.** HIPAA requires the risk analysis to be documented and retained for six years. ServiceNow's audit history and report export functionality satisfy this documentation requirement automatically.

| HIPAA Safeguard | Typical Control Objective | ServiceNow Module |
|---|---|---|
| Access Management (§164.308(a)(4)) | Role-based access to ePHI systems | Policy & Compliance → Control Objectives |
| Audit Controls (§164.312(b)) | Automated log review for ePHI access | Indicators (KRI): log review rate |
| Workforce Training (§164.308(a)(5)) | Annual security awareness training completion | Control Evidence (training completion records) |
| Business Associate Mgmt (§164.308(b)) | BAA execution and periodic vendor review | Third-Party Risk module |
| Contingency Planning (§164.308(a)(7)) | Tested backup and DR procedures | Risk Register + Advanced Risk scenarios |
| Transmission Security (§164.312(e)) | TLS/encryption for ePHI in transit | Control Objectives → Technical Safeguards |

{% hint style="info" %}
OCR's audit protocol (available on hhs.gov) is a direct mapping of the Security Rule to audit inquiries. Use it to validate that your ServiceNow control objective library covers every specification OCR will examine.
{% endhint %}

## In the video

* Building an ePHI Entity inventory in ServiceNow — mapping systems, applications, and Business Associates to Entity Profiles.
* Configuring a HIPAA-specific Risk Register with Risk Statements aligned to the three safeguard categories.
* Running a scoped risk assessment against the ePHI entity inventory and producing the documented risk analysis output.
* Demonstrating the Issue workflow for high-risk findings — owner assignment, remediation plan, and evidence attachment.
* Showing how KRI indicators (access log review rate, patch latency for ePHI systems) provide continuous monitoring between point-in-time risk analyses.

## Key takeaways

* HIPAA risk analysis is a legal requirement, not a best practice — OCR enforcement actions make inadequate risk analysis one of the top cited violations.
* ServiceNow IRM transforms the risk analysis from a periodic consulting engagement into a continuously maintained, auditable program.
* ePHI scoping is the most critical first step — you cannot analyze risk for systems you have not inventoried.
* Required vs. Addressable distinctions must be documented in control records — documented rationale for non-implementation is a defensible position; silence is not.
* Third-party/Business Associate risk management belongs inside the same IRM program — a BAA alone does not satisfy the Security Rule's business associate requirements.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
