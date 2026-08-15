---
description: Cross-Framework Crosswalks and Mapping Techniques
---

# 3.5 · Cross-Framework Crosswalks and Mapping Techniques

{% hint style="success" %}
**Module 3: Frameworks & Baselines** — 4LOD: 2nd Line (Control Frameworks & Compliance) · Persona: Security Architects, GRC Consultants, Compliance Engineers
{% endhint %}

{% hint style="info" %}
**Watch — 3.5 · Cross-Framework Crosswalks and Mapping Techniques**

A short video lesson accompanies this page. Video links are placeholders until the recording is published to the [TechTalk with Bill YouTube channel](https://www.youtube.com/@techtalkwithbill). Subscribe to be notified when this lesson goes live.
{% endhint %}
## Read

A Unified Control Framework (UCF) is a single internal control library, tagged with citations to every external framework the organisation must comply with. Its purpose is simple: one control, tested once, satisfies many frameworks. Without a UCF, organisations retest the same control against NIST, ISO, SOC 2, and PCI separately — burning capacity that should have gone to remediation.

The UCF is the artefact that separates a mature GRC function from a compliance department. It is also the artefact that most obviously shows up as a ServiceNow IRM implementation win.

## ServiceNow Implementation Notes

In ServiceNow IRM, the UCF is expressed as the Control Objective library with Citations to Authority Documents. Every Control Objective should carry citations to every framework it satisfies. Every recurring Test on that Objective then produces evidence for all cited frameworks.

## Live in Action — Lumina Cyber Risk (Open Source)

The Lumina data model implements the UCF pattern with a `control` object linked to many `authority_document_citation` objects. Inspect the seed data to see the cross-framework linkage in action.

## Apply

- Take one control and map it to NIST CSF 2.0, ISO 27001:2022 Annex A, and SOC 2 CC series simultaneously.

## Done When

- You have delivered the module deliverable: a UCF spreadsheet with at least one control mapped to three frameworks.


---

[← 3.4 Industry-Specific Baselines: PCI DSS v4.0, HIPAA Security Rule, SOC 2 Type II](lesson-3-4.md) · [Next: Module 4 · CMDB & Asset Governance →](../module-04-cmdb-and-asset-governance/README.md)
