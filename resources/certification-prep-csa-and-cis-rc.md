---
description: Prep resources for CSA and CIS-RC.
---

# Certification Prep (CSA and CIS-RC)

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Certification Prep (CSA and CIS-RC) — video placeholder
{% endembed %}

## Overview

Two certifications directly validate your ServiceNow IRM expertise: the **Certified System Administrator (CSA)** and the **Certified Implementation Specialist — Risk and Compliance (CIS-RC)**. The CSA is the prerequisite for CIS-RC and validates platform fundamentals; CIS-RC validates deep implementation knowledge of the GRC application suite. Both are proctored, closed-book exams with ~60 questions and a 105-minute time limit. This section provides a structured study plan and identifies exactly where this handbook's content maps to each exam's objectives.

## CSA Exam: Scope and Topics

The CSA exam covers ServiceNow platform fundamentals — not IRM-specific content. It is a prerequisite for all CIS specialization exams. Passing requires fluency in:

| Topic Area | Key Concepts to Know |
|---|---|
| Platform navigation | Application navigator, lists, filters, forms, related lists, UI16/Next Experience |
| Data model | Tables, fields, dictionary, relationships, glide records, reference fields |
| User administration | Users, groups, roles, ACLs, impersonation |
| Workflow and Flow Designer | Flow Designer activities, triggers, conditions; legacy Workflow Editor awareness |
| Business Rules & Client Scripts | When each fires (before/after/async), client-side vs. server-side execution |
| Import sets and transform maps | Data import, coalesce, transform map configuration |
| Reporting and dashboards | Report types, dashboard composition, scheduled reports |
| Service Catalog | Catalog items, variables, workflows, fulfillment |
| Update sets | Retrieve, preview, commit, conflict resolution |
| CMDB basics | CI classes, relationships, CMDB health |

**Study resources for CSA:**
- ServiceNow's Now Learning platform (free self-paced courses for credentialed accounts)
- ServiceNow documentation (docs.servicenow.com) — Platform Administration section
- Practice exams from ServiceNow's official exam preparation guides
- This handbook's update set import procedure and navigation cheat sheets cover the update set and navigation exam objectives directly

## CIS-RC Exam: Scope and Topics

The CIS-RC exam validates implementation-level knowledge of the ServiceNow GRC suite — Policy and Compliance, Risk Management, and Audit Management. It is the primary certification for IRM practitioners. Topics include:

| Domain | Weight (approx.) | Key Concepts |
|---|---|---|
| GRC Data Model | 15% | Entity types, Profiles, Content Library, Control Objectives, Indicators, Risk Statements |
| Policy & Compliance | 20% | Policies, Citations, Control Objectives, Compliance Tasks, Evidence, Attestation |
| Risk Management | 25% | Risk Register, Risk Assessments, Risk Statements, Risk Acceptance, Inherent/Residual scoring |
| Advanced Risk | 10% | Quantitative risk, Monte Carlo scenarios, risk appetite, CRI Profile |
| Audit Management | 15% | Audit engagements, audit plans, workpapers, findings, issue integration |
| Issues & Findings | 10% | Issue creation, remediation plans, evidence, escalation workflows |
| Configuration & Administration | 5% | Scoped app structure, application properties, content pack installation |

**Topics where this handbook provides direct coverage:**
- Risk Register and Risk Statements structure — covered in the Foundations and Banking sections
- Control Objectives and the CRI Profile — covered in the Banking use case and Advanced Risk chapters
- KRI/Indicator configuration — dedicated module in this handbook
- Entity Profiles and hierarchy — covered in the core data model content
- Issues & Findings and the POAM workflow — covered in Government/CAM section

## Recommended Study Plan

**Phase 1 — Platform Foundations (2–3 weeks): CSA prep**
1. Complete the ServiceNow CSA learning path on Now Learning (approximately 20 hours of guided content).
2. Work through this handbook's update set import exercises — they directly reinforce the update set and navigation exam objectives.
3. Take at least two practice CSA exams. Target 85%+ before scheduling the real exam.

**Phase 2 — GRC Deep Dive (3–4 weeks): CIS-RC prep**
1. Work through every video in this handbook from Foundations through Advanced Risk. Follow along in your PDI.
2. Use the companion update sets to install the configurations — active implementation is the most effective exam prep for CIS-RC.
3. Study the ServiceNow GRC product documentation: focus on the data model, configuration tables, and scoped application properties.
4. Review the CIS-RC exam blueprint (available on ServiceNow's certification site) and map every objective to a handbook chapter or video.

**Phase 3 — Practice and Gap-Fill (1–2 weeks)**
1. Take CIS-RC practice exams (available through Now Learning and third-party prep communities).
2. For every question you miss, trace it to the specific handbook section or ServiceNow documentation page and review it.
3. Focus additional time on the Audit Management domain if you have not used that module in practice — it is frequently underrepresented in self-study.

{% hint style="info" %}
Both exams allow you to flag questions for review and return to them. On CIS-RC, if a question references a specific configuration step you are unsure of, skip it, finish the rest, and return with the remaining time — the exam rewards breadth of knowledge over deep recall on any single item.
{% endhint %}

## In the video

* Walkthrough of the CSA exam structure — question types, topic distribution, and what the hardest questions tend to test.
* Mapping this handbook's chapters and video exercises directly to CIS-RC exam objectives.
* Live demo of a PDI-based practice exercise covering the Risk Assessment and Issues domains — the two highest-weight CIS-RC areas.
* Tips for using ServiceNow's Now Learning platform effectively alongside this handbook.

## Key takeaways

* CSA is the prerequisite for CIS-RC — complete it first, but your platform-building work in this handbook counts as practical CSA preparation.
* CIS-RC is an implementation exam, not a conceptual one — the best preparation is actually building the configurations in a PDI alongside the videos.
* The Risk Management and Policy & Compliance domains account for roughly 45% of CIS-RC questions — prioritize them if time is limited.
* ServiceNow's official exam blueprint is the authoritative study guide — map every objective to a resource before scheduling the exam.
* Flashcards for GRC terminology (available in the `/cert-prep/` folder of the GitHub repo) are the highest-efficiency study tool for the final week before the exam.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
