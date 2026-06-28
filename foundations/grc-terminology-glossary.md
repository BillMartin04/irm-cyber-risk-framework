---
description: Core GRC and risk vocabulary.
---

# GRC Terminology Glossary

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
GRC Terminology Glossary — video placeholder
{% endembed %}

## Overview

GRC practitioners, platform administrators, and technology teams often use the same words to mean different things — or different words to mean the same thing. This glossary defines the terms used consistently throughout this handbook and maps the most important ones to their corresponding ServiceNow IRM record types. Precision in vocabulary is not pedantry: when a risk officer says "control" and an auditor says "control," they need to be referring to the same construct or risk governance breaks down. Use this page as a reference throughout your reading and return to it whenever a term is unclear.

## Core GRC / cyber-risk terms

| Term | Definition | ServiceNow IRM record |
|------|-----------|----------------------|
| **Risk** | The potential for loss or harm arising from a threat exploiting a vulnerability in an asset or process. Expressed as likelihood × impact in quantitative models, or as a scored category in qualitative models. | Risk Statement (`sn_risk_risk`) |
| **Risk Statement** | A structured declaration of a specific risk, typically in the form: \[Threat/Event\] could affect \[Asset/Process\], resulting in \[Business Impact\]. Statements are the atomic unit of the Risk Register. | Risk Statement |
| **Risk Register** | The authoritative, curated list of an organization's material risks, each represented as a Risk Statement with an owner, likelihood/impact scores, treatment decision, and linkage to controls. | Risk Register (view of Risk Statements) |
| **Inherent Risk** | The raw level of risk exposure that exists before any controls are applied. Provides a baseline for prioritizing control investment. | Inherent score fields on Risk Statement |
| **Residual Risk** | The risk exposure that remains after controls are applied and operating effectively. If residual risk exceeds risk appetite, additional treatment is required. | Residual score fields on Risk Statement |
| **Risk Appetite** | The amount and type of risk the organization is prepared to accept in pursuit of its strategic objectives, as defined and approved at the board level. Expressed as a qualitative statement or quantitative threshold. | Risk Appetite record; thresholds on Risk Statements |
| **Risk Tolerance** | The acceptable variance around the risk appetite threshold — how far actual risk exposure can deviate from appetite before escalation is triggered. | Threshold bands on Indicators/KRIs |
| **Risk Treatment** | The decision made about how to address a risk above appetite: Mitigate (add/improve controls), Transfer (insurance, contract), Accept (formal documented acceptance), or Avoid (exit the activity). | Treatment plan on Risk Statement |
| **Control** | A safeguard or countermeasure that modifies the likelihood or impact of a risk. Can be preventive, detective, or corrective. Controls are tested periodically to verify they are operating as designed. | Control (`sn_compliance_control`) |
| **Control Objective** | A high-level statement of intent describing what a group of related controls is meant to achieve. Sits above individual controls in the control hierarchy and is typically mapped to authority document citations. | Control Objective (`sn_compliance_policy`) |
| **Control Test / Test of Design (ToD)** | An assessment of whether a control is appropriately designed to achieve its objective. A poorly designed control cannot be effective regardless of how well it is operated. | Test (`sn_audit_test`) |
| **Control Test / Test of Effectiveness (ToE)** | An assessment of whether a control is operating as designed over a defined period. Requires sampling evidence of actual control execution. | Test result on Control record |
| **Authority Document** | A source of external requirements — a regulation, standard, or framework (e.g., ISO 27001, NIST CSF, PCI DSS) — from which control obligations are derived. In ServiceNow, authority documents are linked to Control Objectives via citation records. | Authority Document (`sn_compliance_authority_document`) |
| **Citation** | The specific clause, requirement, or section within an authority document that mandates or recommends a control. Control Objectives are mapped to one or more citations, establishing traceability from requirement to control. | Citation (`sn_compliance_citation`) |
| **Policy** | An internally mandated statement of organizational intent that drives specific control behaviors. Policies are published, attested to, and enforced. They derive their requirements from authority documents and translate them into internal rules. | Policy (`sn_compliance_policy`) |
| **Attestation** | A formal, documented confirmation by a responsible party that a policy, control, or compliance requirement has been reviewed and is being adhered to. In ServiceNow, attestations are workflow-driven tasks assigned to named owners on a schedule. | Attestation Task |
| **Entity** | In ServiceNow IRM, an Entity is any business object — a business unit, application, vendor, process, product — that can bear risk. Entities are scoped within Profiles and are the subject of risk assessments. | Entity (`sn_risk_entity`) |
| **Profile** | A Profile in ServiceNow IRM groups related Entities of the same type (e.g., all retail banking applications, all critical vendors). Risk Statements and assessment campaigns are scoped to Profiles, enabling consistent risk coverage across similar Entities. | Profile (`sn_risk_profile`) |
| **Indicator / KRI** | A Key Risk Indicator — a measurable metric that signals whether a risk is trending toward or away from appetite. Indicators in ServiceNow IRM auto-score and feed back into Risk Statement residual risk calculations when thresholds are breached. | Indicator (`sn_risk_indicator`) |
| **Issue** | A confirmed gap, failure, or deficiency — either self-identified or raised by audit. Issues are linked to the Risk Statement and Control they relate to, and carry a remediation owner, target date, and status. | Issue (`sn_risk_issue`) |
| **Finding** | An observation from internal audit or a regulatory examiner documenting a control deficiency or policy violation. Findings are more formal than self-identified Issues and typically require executive-level remediation accountability. | Finding (`sn_audit_finding`) |
| **Risk Assessment** | A structured, time-bounded evaluation of the likelihood and impact of one or more risks against a defined scope (Entity, Profile, or program). In ServiceNow IRM, assessments are run as campaigns that route questionnaires to risk and control owners. | Risk Assessment (`sn_risk_risk_assessment`) |
| **Continuous Authorization and Monitoring (CAM)** | An IRM operating model in which control effectiveness and risk posture are evaluated on an ongoing basis rather than at scheduled intervals, using automated evidence collection and real-time Indicator scoring. Supported in ServiceNow through Advanced Risk features. | CAM configuration in Advanced Risk |
| **CRI Profile** | The Cyber Risk Institute (CRI) Profile is a sector-specific cybersecurity framework widely adopted in financial services. It maps NIST CSF, NIST 800-53, and other standards into a prioritized set of diagnostic statements for financial institutions. | Authority Document in IRM (CRI Profile citations) |
| **Three Lines of Defense** | The governance model assigning risk accountability to: first line (operational ownership), second line (risk management oversight), and third line (internal audit assurance). Shapes role assignment and workflow routing throughout IRM. | Role-based access and workflow in ServiceNow |
| **Operational Risk** | The risk of loss resulting from inadequate or failed internal processes, people, systems, or external events. Basel II/III classifies cyber risk as a subcategory of operational risk. The primary risk category for IRM programs in banking. | Risk category on Risk Statements |
| **Third-Party Risk (TPRM)** | The risk exposure arising from relationships with vendors, suppliers, and service providers who have access to organizational data, systems, or processes. Managed through third-party risk assessments linked to vendor Entities in IRM. | Third-party Entity and Profile in IRM |
| **Risk Posture** | The current state of an organization's risk exposure, typically expressed as a heat map or aggregate score across the risk register. Driven by current residual risk scores and the status of treatment plans and open Issues. | IRM risk posture dashboard |
| **Segregation of Duties (SoD)** | A control principle requiring that no single person can execute a complete transaction or process from initiation to approval. SoD violations are a common finding in access control reviews and link to IT general control objectives in IRM. | Control Objective (access management category) |
| **GRC** | Governance, Risk, and Compliance — the discipline and the category of technology tools that manage organizational governance frameworks, risk identification and treatment, and compliance with laws, regulations, and standards. | Umbrella term for the ServiceNow IRM/GRC suite |

## How terms relate to each other

The following represents the core data relationships in ServiceNow IRM:

```
Authority Document
    └── Citation
            └── Control Objective
                    └── Control
                            └── Test Result (ToD / ToE)

Profile
    └── Entity
            └── Risk Statement (Risk Register)
                    ├── Inherent Risk Score
                    ├── Control (mitigates)
                    │       └── Residual Risk Score (recalculated)
                    ├── Indicator / KRI (monitors)
                    └── Issue / Finding (tracks gaps)
```

## In the video

* Definitions of the most-used GRC terms, with plain-language examples drawn from a bank's operational risk program.
* How the terms relate to one another — walking through the data model from Authority Document to Risk Statement to residual risk.
* How each term maps to a specific ServiceNow IRM record type, so terminology immediately translates to platform action.
* The three terms practitioners most often confuse: Risk vs. Control, Finding vs. Issue, Inherent vs. Residual risk.

## Key takeaways

* Consistent vocabulary is a prerequisite for effective IRM — every stakeholder must be using the same definitions for the same constructs.
* ServiceNow IRM record types map directly to GRC concepts; knowing the concept helps you configure the right record type.
* The data model hierarchy runs from Authority Document → Control Objective → Control → Test Result, and separately from Profile → Entity → Risk Statement → residual risk calculation.
* Risk appetite and risk tolerance are distinct — appetite is the target, tolerance is the acceptable variance.
* Return to this glossary any time a term in later chapters is unclear; definitions here are used consistently throughout the handbook.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
