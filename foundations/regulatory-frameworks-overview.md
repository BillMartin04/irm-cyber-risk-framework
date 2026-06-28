---
description: The major frameworks that drive requirements.
---

# Regulatory Frameworks Overview

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Regulatory Frameworks Overview — video placeholder
{% endembed %}

## Overview

No IRM program operates in a vacuum. Every risk register, control library, and assessment cycle is shaped by one or more external frameworks — regulatory mandates, industry standards, or international norms that define what "good" looks like. The challenge most organizations face is not a shortage of frameworks; it is that they face multiple, overlapping ones simultaneously and need a coherent way to harmonize them without maintaining seven parallel control libraries. This page surveys the frameworks most commonly encountered in IRM programs, explains what each one demands, and shows how they map to each other and to the ServiceNow IRM control model.

## Key concepts

* **Framework vs. regulation** — A framework (NIST CSF, ISO 27001, CRI Profile) is a voluntary standard that defines best practices. A regulation (GDPR, PCI DSS, DORA) is a mandatory legal requirement with enforcement consequences. In practice, regulated organizations treat both with similar rigor — regulators reference frameworks as the expected baseline even when they are technically voluntary.
* **Authority Document** — In ServiceNow IRM, every external requirement source — whether a regulation, standard, or framework — is loaded as an Authority Document. Citations from each document are mapped to Control Objectives, establishing traceability from regulatory requirement to implemented control.
* **Control harmonization** — When multiple frameworks require the same control behavior (e.g., access review appears in ISO 27001, NIST 800-53, PCI DSS, and SOC 2), a single Control Objective linked to multiple citations from multiple Authority Documents satisfies all requirements from one control. This is the core efficiency argument for IRM over spreadsheet-based compliance management.
* **Gap assessment** — Mapping an organization's current control library against a new framework's requirements to identify controls that are missing, partially implemented, or untested. In ServiceNow IRM, running a Compliance Assessment against an Authority Document produces this gap view automatically.

## Framework comparison table

| Framework | Type | Scope | Key focus areas | Primary audience | Enforced by |
|-----------|------|-------|-----------------|-----------------|-------------|
| **NIST CSF** | Voluntary standard | All sectors | Identify, Protect, Detect, Respond, Recover functions | US organizations; adopted globally | NIST (no enforcement); referenced by US regulators |
| **NIST SP 800-53** | Voluntary standard | Federal and commercial | 20 control families; 1,000+ controls | US federal agencies; financial services, defense supply chain | FISMA for federal; referenced by OCC, FDIC |
| **ISO 27001** | International standard | All sectors | Information Security Management System (ISMS); Annex A controls | Global; required by enterprise contracts and some regulators | Certification bodies; contractual |
| **SOC 2** | Attestation standard | Service organizations | Trust Service Criteria: Security, Availability, Confidentiality, Processing Integrity, Privacy | SaaS, cloud, and technology service providers | AICPA; customer contracts |
| **PCI DSS** | Industry standard | Payment card data handlers | 12 requirements across network security, access control, encryption, monitoring | Any organization storing, processing, or transmitting cardholder data | PCI SSC; enforced through card brand contracts and fines |
| **GDPR** | Regulation | EU data controllers and processors | Data subject rights, lawful basis, data protection by design, breach notification (72 hours) | Any organization processing EU personal data | National Data Protection Authorities; fines up to 4% of global turnover |
| **Basel III / Operational Risk** | Regulatory framework | Banks and financial institutions | Operational risk capital calculation; risk event taxonomy (7 categories including CPBP, EPWS, IF) | Prudentially regulated banks | National banking regulators (OCC, Fed, PRA, ECB, APRA) |
| **DORA (EU Digital Operational Resilience Act)** | Regulation | EU financial entities and ICT third-party providers | ICT risk management, incident reporting, third-party ICT risk, DORA-specific testing (TLPT) | Banks, insurers, investment firms, and their critical ICT providers operating in the EU | European Supervisory Authorities (EBA, ESMA, EIOPA); national competent authorities |
| **CRI Profile** | Sector framework | Financial services | Prioritized diagnostic statements mapped to NIST CSF; four implementation tiers; 277 diagnostic statements | US and international financial institutions | No direct enforcement; adopted by regulators as baseline expectation |
| **FFIEC CAT** | Regulatory guidance | US depository institutions | Inherent risk profile + cybersecurity maturity; five domains | US banks, credit unions, regulated by FFIEC member agencies | OCC, Fed, FDIC, NCUA examinations |

## How frameworks map to controls

The following table shows how a common control area — **Access Management** — maps across the major frameworks. This illustrates how a single well-designed Control Objective covers multiple framework requirements simultaneously:

| Control area: Access Management | Framework reference |
|--------------------------------|---------------------|
| Least privilege access | NIST CSF PR.AC-4; NIST 800-53 AC-6; ISO 27001 A.9.1.2; PCI DSS Req. 7; SOC 2 CC6.3 |
| Privileged access management (PAM) | NIST 800-53 AC-2, AC-17; ISO 27001 A.9.4.4; PCI DSS Req. 8.6; DORA Art. 9(4)(e) |
| Periodic access review / recertification | ISO 27001 A.9.2.5; SOC 2 CC6.2; PCI DSS Req. 7.2; NIST 800-53 AC-2(j) |
| Multi-factor authentication | NIST CSF PR.AC-7; PCI DSS Req. 8.4; DORA Art. 9(4)(d); SOC 2 CC6.1 |
| Joiner/Mover/Leaver process | ISO 27001 A.9.2.1–9.2.6; SOC 2 CC6.2; Basel CPBP event type (unauthorized access) |

In ServiceNow IRM, a single Control Objective called "Access Management — Least Privilege" can be linked to all of these citations from their respective Authority Documents. When the control is tested, the test result satisfies the compliance requirement across all frameworks simultaneously — eliminating duplicate testing.

## DORA: the framework to watch for financial services

DORA entered into force on 17 January 2025 and applies to all EU-regulated financial entities and their critical ICT third-party providers. For IRM practitioners in financial services, DORA introduces requirements that map directly into the IRM platform:

* **ICT Risk Management Framework** — A documented, board-approved ICT risk management framework. In IRM terms: a formal Risk Taxonomy with ICT-specific Risk Statements, a Control Objective library, and documented risk appetite for ICT risk. Maps to the Risk Register and Authority Document structures in ServiceNow.
* **ICT Incident Classification and Reporting** — Mandatory reporting of major ICT incidents to national competent authorities within 4 hours (initial notification) and 72 hours (intermediate report). Issues and Findings records in IRM, linked to the incident management workflow, support the evidence trail.
* **Third-Party ICT Risk** — A register of all contractual arrangements with ICT third-party providers, with risk assessments for critical and important functions. Maps directly to Third-Party Risk Management in ServiceNow IRM — vendor Entities, risk assessments, and contractual register.
* **Digital Operational Resilience Testing (DORT)** — Annual testing of ICT tools and systems, and Threat-Led Penetration Testing (TLPT) for significant entities every three years. Test results feed into the IRM control testing record.

{% hint style="warning" %}
**DORA third-party scope is broad.** DORA applies not just to the regulated financial entity but to ICT third-party providers that are deemed "critical" by the European Supervisory Authorities. If your organization is a cloud provider, software vendor, or data analytics provider serving EU financial institutions, you may be in scope for DORA oversight and examination.
{% endhint %}

## Basel operational risk and IRM

Basel III's operational risk framework is foundational for banks' IRM programs. The Basel taxonomy of seven operational risk event types provides the primary categorization that Risk Statements in a banking IRM program are written against:

| Basel event type | Code | Cyber risk relevance |
|-----------------|------|----------------------|
| Internal Fraud | IF | Insider threat, unauthorized transactions |
| External Fraud | EF | Ransomware, phishing, account takeover |
| Employment Practices and Workplace Safety | EPWS | Data misuse by employees |
| Clients, Products and Business Practices | CPBP | Data privacy violations, unauthorized data sharing |
| Damage to Physical Assets | DPA | Physical destruction of data centers |
| Business Disruption and System Failures | BDSF | DDoS, system outages, critical infrastructure failure |
| Execution, Delivery and Process Management | EDPM | Configuration errors, failed change management, data integrity failures |

Risk Statements in a banking IRM program should carry a Basel event type classification. This enables capital attribution under the standardized approach and satisfies regulator expectations for an integrated operational risk taxonomy.

## In the video

* A walkthrough of each major framework — what it requires, who it applies to, and how demanding its control library is relative to others.
* How to load an Authority Document in ServiceNow IRM and link its citations to Control Objectives.
* A live example of a single Control Objective satisfying requirements from three different frameworks simultaneously.
* DORA's specific IRM implications and what financial services firms need to configure differently to be DORA-ready.

## Key takeaways

* Most regulated organizations face multiple overlapping frameworks simultaneously; the IRM approach (single Control Objective, multiple citations) eliminates duplicate testing.
* Authority Documents in ServiceNow IRM are the mechanism for translating external requirements into internal control obligations with full traceability.
* DORA is the most significant new framework for EU financial services IRM programs, with specific requirements for ICT risk management, incident reporting, and third-party risk registers.
* Basel operational risk taxonomy provides the primary risk categorization for banking IRM programs; Risk Statements should carry Basel event type classifications.
* Framework maturity differences are significant: ISO 27001 has ~93 Annex A controls; NIST 800-53 has 1,000+; SOC 2 Trust Service Criteria number in the dozens. Match framework selection to organizational maturity and regulatory context.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
