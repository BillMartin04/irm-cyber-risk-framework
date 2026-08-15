---
description: Stage 1 and Stage 2 External Certification Audit Preparation
---

# 18.5 · Stage 1 and Stage 2 External Certification Audit Preparation

{% hint style="success" %}
**Module 18: ISO 27001 Lead Implementer** — 4LOD: 2nd Line (Lead Implementation) & 3rd Line (Independent Audit) · Persona: Lead Implementers, Lead Auditors, Quality Assurance Directors
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *Stage 1 and Stage 2 External Certification Audit Preparation — Iso 27001 Lead Implementer (2026)*
**Channel:** [TechTalk with Bill](https://www.youtube.com/channel/UCMf7pje1x5iZkkEF-Y3PLSA)
**Length:** 12–18 min · **Status:** 🎬 In production — subscribe to be notified when this video is published.

**Chapters** (planned)
- 00:00 Intro & why this lesson matters
- 01:30 Definitions and first principles
- 03:30 Four-Lines-of-Defense mapping
- 05:30 ServiceNow implementation walkthrough
- 08:00 Live in action inside Lumina (open source)
- 10:30 Apply this at your organisation this week
- 12:00 Done-When checklist & next lesson

▶ [Subscribe to be notified](https://www.youtube.com/channel/UCMf7pje1x5iZkkEF-Y3PLSA?sub_confirmation=1) · ⭐ [Star the repo](https://github.com/BillMartin04/irm-cyber-risk-framework) · 💬 [Suggest a topic](https://github.com/BillMartin04/irm-cyber-risk-framework/issues)
{% endhint %}
## Read

This lesson covers **Stage 1 and Stage 2 External Certification Audit Preparation** as part of the ISO 27001 Lead Implementer module. The line-of-defense frame for this material is 2nd Line (Lead Implementation) & 3rd Line (Independent Audit), which is why the primary audience is Lead Implementers. Practitioners in adjacent lines of defense should also work through it — the biggest failure mode of a GRC program is when one line assumes another line has covered a control it has not.

The mature operating pattern here is to treat the topic as a **repeatable design artefact**, not a one-time exercise. That means documented inputs, a defined decision authority, a governed output artefact, and a review cadence. Every enterprise-grade GRC program in this space eventually converges on that shape.

The reading below covers the concept, the operating pattern that makes it defensible under audit, and the specific traps that catch teams building this capability for the first time.

## ServiceNow Implementation Notes

In a ServiceNow IRM deployment, the artefact that carries this capability should be modelled as a first-class record linked back to the Risk register and the Control Objective library. If your instance is holding this content in free-text description fields on unrelated records, you have a structural defect that will surface at the first audit.

Design it once, promote it into the Control Objective library, and let recurring Assessments produce the evidence over time.

## Live in Action — Lumina Cyber Risk (Open Source)

The [Lumina Cyber Risk portal](https://github.com/BillMartin04/lumina-cyber-risk) demonstrates the same pattern in an open-source, minimally-sized data model. Use it as a reference implementation when the enterprise instance is too large to prototype in directly.

## Apply

- Sketch this artefact for your own organisation using one real risk from your register as the worked example.
- Identify the accountable owner (by name, not by role) and the review cadence you will enforce.
- Add the artefact to your GRC operating calendar so it does not silently drop off.

## Done When

- You can produce this artefact for a new risk in less than an hour.
- You know who signs off on it and when it next needs to be refreshed.


---

[← 18.4 Conducting Internal Audits per ISO 19011](lesson-18-4.md) · [Next: Module 19 · Capstone →](../module-19-capstone/README.md)
