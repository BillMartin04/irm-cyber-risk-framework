---
description: Map controls to the CRI Profile and frameworks.
---

# CRI Profile and Framework Mapping

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
CRI Profile and Framework Mapping — video placeholder
{% endembed %}

## Overview

Banks and financial institutions operate under a dense overlay of cybersecurity frameworks: NIST CSF, ISO 27001, FFIEC CAT, NIST 800-53, and the sector-specific FSSCC Cyber Risk Institute (CRI) Profile. Each framework has its own structure, terminology, and control language, yet the underlying controls a bank implements are largely the same across all of them. The challenge — and the opportunity — in ServiceNow IRM is to build a single, harmonized control library that maps to all applicable frameworks simultaneously. When a control is attested or fails, the result propagates across every framework it is mapped to. This lesson explains the CRI Profile, how it relates to NIST CSF and ISO 27001, and how to implement cross-framework mapping in ServiceNow.

## Key concepts

- **FSSCC Cyber Risk Institute (CRI) Profile** — A financial-sector-specific cybersecurity framework developed by the Financial Services Sector Coordinating Council. It is based on the NIST Cybersecurity Framework but extended with financial-sector context, diagnostic statements, and a maturity tiering system calibrated to institution size and complexity. The CRI Profile is the closest thing to a universal cyber risk baseline for U.S. financial institutions.
- **CRI Profile Structure** — The Profile organizes cyber risk management into six NIST CSF-aligned Functions (Identify, Protect, Detect, Respond, Recover, plus Governance as a standalone function in later versions), with Categories, Subcategories, and Diagnostic Statements beneath them. Each Diagnostic Statement is a testable, specific control requirement.
- **NIST CSF** — The National Institute of Standards and Technology Cybersecurity Framework. The foundational structure underlying the CRI Profile. NIST CSF uses the same Function/Category/Subcategory hierarchy. CRI Profile Subcategories map 1:1 or 1:many to NIST CSF Subcategories.
- **ISO 27001** — The international standard for information security management systems. ISO 27001 Annex A controls map to NIST CSF and CRI Profile categories, though the organizational structure is different. A well-maintained control library in ServiceNow will include ISO 27001 clause mappings alongside NIST CSF references.
- **Authority Documents in ServiceNow** — Each regulatory framework is loaded as an Authority Document record in ServiceNow's Policy & Compliance application. Authority documents contain the framework's requirements at the citation level (e.g., NIST CSF PR.AC-1 or CRI Profile Diagnostic Statement 2.1.3). Controls are linked to these citations.
- **Control Objectives** — Intermediate records that aggregate related control citations from one or more authority documents. A Control Objective for "Access Management" might pull in NIST CSF PR.AC, CRI Profile Section 2, and ISO 27001 A.9 simultaneously.
- **Unified Control Library** — The goal of cross-framework mapping: a single set of control records, each linked to its relevant citations across multiple frameworks. When a control is assessed, all linked framework citations are updated — no duplicate control records, no duplicate attestations.
- **Gap Analysis** — A compliance assessment run against an authority document to identify which framework requirements are not currently covered by any control in the library. ServiceNow generates a gap list showing uncovered citations, enabling prioritized control development.

## The CRI Profile in practice: structure and banking relevance

The CRI Profile is structured in tiers that reflect institution complexity. Tier 1 covers community banks and credit unions with limited cyber complexity; Tier 4 covers globally systemically important banks (G-SIBs). The tiering is important because it determines which Diagnostic Statements are in scope for your institution — not all requirements apply at every tier.

A Diagnostic Statement at the Tier 2 level for a mid-size regional bank might read: "The organization defines and manages privileged access based on role and least privilege principles, with access reviews conducted no less than quarterly." This maps to:

- **NIST CSF**: PR.AC-4 (Access permissions and authorizations are managed), PR.AC-6 (Identities are proofed and bound to credentials)
- **ISO 27001**: A.9.2.3 (Management of privileged access rights), A.9.2.5 (Review of user access rights)
- **NIST 800-53**: AC-6 (Least Privilege), AC-2 (Account Management)

In ServiceNow, a single "Privileged Access Management" control record is linked to all four citations. One attestation. One result. Four framework postures updated simultaneously.

## Implementing cross-framework mapping in ServiceNow

**Step 1 — Load authority documents**

Navigate to Policy and Compliance > Authority Documents. ServiceNow ships with pre-built authority document content for NIST CSF, ISO 27001, NIST 800-53, FFIEC CAT, and others. The CRI Profile may require a content import if your organization has a subscription to the CRI content pack. Confirm your platform version and content subscriptions before implementation.

**Step 2 — Build or import Control Objectives**

Create Control Objectives that represent the logical groupings of your control environment. For cyber risk, common objectives include: Identity and Access Management, Endpoint Security, Network Security, Data Protection, Third-Party Risk, Incident Response, and Business Continuity.

**Step 3 — Link controls to citations**

For each Control record, navigate to the "Authority Document Citations" related list. Add citations from each applicable authority document. The table below shows an example for a "Multi-Factor Authentication" control:

| Authority Document | Citation | Requirement Text (abbreviated) |
|---|---|---|
| CRI Profile v2.0 | 2.1.4 | MFA required for all privileged and remote access |
| NIST CSF | PR.AC-7 | Users, devices, and other assets are authenticated |
| ISO 27001 | A.9.4.2 | Secure log-on procedures |
| FFIEC CAT | Cybersecurity Controls D3.PC.Im.B.1 | Multi-factor authentication for remote access |
| NIST 800-53 | IA-2(1) | Identification and Authentication — MFA for privileged accounts |

**Step 4 — Run a gap analysis**

Navigate to Policy and Compliance > Compliance > Run Assessment. Select "Gap Analysis" as the type and choose the CRI Profile as the authority document. ServiceNow compares every CRI Profile Diagnostic Statement against your control library and returns a list of uncovered citations. For a Tier 2 bank running this for the first time, expect 20–40% of Diagnostic Statements to be uncovered — meaning no existing control record is mapped to them.

**Step 5 — Prioritize coverage**

Sort the gap list by CRI Profile tier applicability and by your organization's risk priorities. Build new control records (or map existing controls) to address high-priority gaps. Focus first on Tier 2 mandatory statements before moving to enhanced or aspirational tiers.

**Step 6 — Maintain the mapping over time**

Framework versions change. The CRI Profile updates periodically; NIST CSF released version 2.0 in 2024 with a new Govern function. When a new version of an authority document is released, ServiceNow allows you to import the updated version alongside the existing one, identify changed or new citations, and update control mappings accordingly — without disrupting active assessments running against the prior version.

{% hint style="info" %}
**Regulator perspective**: OCC and Federal Reserve examiners increasingly ask banks to demonstrate cross-framework coverage — specifically, how NIST CSF requirements are satisfied by your control environment. Having that mapping built in ServiceNow means you can generate a cross-reference report in minutes, not days.
{% endhint %}

## In the video

- Navigating to Authority Documents and reviewing the CRI Profile content structure in ServiceNow.
- Opening a Control record and adding citations from CRI Profile, NIST CSF, and ISO 27001.
- Running a gap analysis against the CRI Profile and reading the results.
- How a single control attestation updates posture across multiple framework dashboards simultaneously.
- The compliance posture dashboard view filtered by framework, showing cross-mapped coverage.

## Key takeaways

- The CRI Profile is the financial-sector adaptation of NIST CSF, with tiered requirements calibrated to institution complexity — the right baseline for U.S. bank cyber risk management programs.
- The goal of framework mapping in ServiceNow is a unified control library: one control record linked to multiple framework citations, eliminating duplicate attestation work.
- ServiceNow's Authority Document structure stores framework requirements at the citation level, enabling precise control-to-requirement traceability for regulatory examinations.
- Gap analysis against the CRI Profile is the fastest way to identify uncovered control requirements and prioritize new control development.
- Cross-framework mapping is a living exercise — framework updates require periodic review of citation mappings, but ServiceNow's versioned authority document model makes this manageable.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
