---
description: Reference architecture diagrams.
---

# Architecture Diagrams

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Architecture Diagrams — video placeholder
{% endembed %}

## Overview

The architecture diagrams in this repository are the visual companion to the handbook's written content. They are not decorative — they are precise reference artifacts that document the ServiceNow IRM data model, the relationships between platform constructs, integration patterns, and the operating model that governs how risk, control, and compliance data flows through the platform. Every diagram is available in editable draw.io format and exported PNG/SVG so you can adapt them for your own organization's documentation.

## Diagram Catalog

| Diagram | Description | Format |
|---|---|---|
| IRM Core Data Model | Entity hierarchy → Risk Register → Control Objectives → Assessments → Issues data relationships | draw.io, PNG |
| Three Lines of Defense Operating Model | First/second/third line roles, data ownership, and workflow routing in ServiceNow IRM | draw.io, PNG |
| CRI Profile Control Structure | CRI Profile tiers → diagnostic statements → control objectives mapping | draw.io, PNG |
| Third-Party Risk Data Flow | Vendor onboarding → risk tiering → assessment → findings → remediation lifecycle | draw.io, PNG |
| KRI / Indicator Architecture | Data source → IntegrationHub connector → Indicator record → threshold alert → escalation | draw.io, PNG |
| CAM / POAM Workflow | Assessment finding → Issue creation → POAM milestone → closure → AO risk summary | draw.io, PNG |
| Integration Architecture | ServiceNow IRM integration patterns with SIEM, vulnerability scanners, and GRC data feeds | draw.io, PNG |

## Key concepts

* **IRM Core Data Model** — The most important diagram in the set. It shows how Entities (the asset/business unit inventory) sit at the center of the model, with Risk Statements, Control Objectives, Indicators, and Issues radiating outward as linked records. Understanding this model is prerequisite to implementing any module correctly.
* **Entity hierarchy** — Entities are organized hierarchically: Organization → Business Unit → Department → Application/System → Vendor. The diagram shows how risk scores roll up through the hierarchy and how scoped assessments target a specific entity node.
* **Integration patterns** — The integration architecture diagram distinguishes between pull integrations (ServiceNow queries an external system on a schedule), push integrations (an external system sends data to ServiceNow via API), and MID Server-based integrations (for on-premises data sources). Knowing which pattern applies to a given data source determines the IntegrationHub spoke selection.
* **RACI overlay** — The Three Lines of Defense operating model diagram includes a RACI overlay showing which platform roles (risk_manager, control_owner, compliance_reader, audit_user) correspond to each line-of-defense responsibility.

## How to Use the Diagrams

1. **Download the `.drawio` file** from `/diagrams/` in the GitHub repository.
2. **Open in draw.io** — either at app.diagrams.net (browser-based, no install required) or the desktop app.
3. **Edit for your organization** — Replace generic labels (e.g., "Business Unit A") with your actual entity names. Add your specific integration sources. Adjust the RACI to match your org structure.
4. **Export for documentation** — Export as PNG (for presentations and documents) or SVG (for scalable web use). Keep the `.drawio` source file version-controlled alongside the exports.

{% hint style="info" %}
The IRM Core Data Model diagram is the single most useful artifact for onboarding new GRC team members and explaining the ServiceNow IRM platform to executives. Keep it current as your implementation evolves.
{% endhint %}

## In the video

* Walkthrough of the IRM Core Data Model — reading the entity-relationship structure and tracing a risk from Entity to Finding.
* Using the Three Lines of Defense operating model diagram to explain platform role assignments to a risk committee.
* Opening a draw.io file, customizing labels, and exporting for a presentation deck.

## Key takeaways

* The IRM Core Data Model diagram is the foundation — understand it before implementing any module.
* All diagrams are provided in editable draw.io format; adapt them for your organization's documentation rather than redrawing from scratch.
* The integration architecture diagram is the starting point for planning data feed connections to SIEM, vulnerability scanners, and CMDB.
* Keep diagram source files in version control alongside your update sets for a complete implementation audit trail.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
