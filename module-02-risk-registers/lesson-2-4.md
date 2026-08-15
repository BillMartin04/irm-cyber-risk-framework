---
description: Designing and Structuring an Enterprise Risk Register
---

# 2.4 · Designing and Structuring an Enterprise Risk Register

{% hint style="success" %}
**Module 2: Risk Registers** — 4LOD: 2nd Line (Risk Management Oversight) · Persona: Risk Analysts, Information Security Managers, Compliance Specialists
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *Designing and Structuring an Enterprise Risk Register — Cyber Risk Register Explained (2026)*
**Channel:** [TechTalk with Bill](https://www.youtube.com/channel/UCMf7pje1x5iZkkEF-Y3PLSA)
**Length:** 10–15 min · **Status:** 🎬 In production — subscribe to be notified when this video is published.

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

An enterprise risk register is not a spreadsheet. It is a dynamic system with a scoring model, an owner per record, a review cadence, an exception pathway, and a reporting rollup. The register you carry into a board meeting should be the same register your first-line owners are updating in real time — not a hand-copied executive summary that has drifted from operational reality.

The design choices that matter most: the scoring formula (inherent, residual, target), the ownership model (single accountable owner plus oversight roles), and the aggregation logic (how risks roll up to business services, business applications, and enterprise strategic objectives).

## ServiceNow Implementation Notes

Build the register on top of the CMDB and CSDM. Risks should be linked to Business Applications and Services; Assessments should populate them; Issues should discharge them. When the register is grounded in the CMDB, the aggregation reports write themselves.

## Live in Action — Lumina Cyber Risk (Open Source)

Lumina ships a minimal register schema with inherent and residual scoring plus a first / second / third / fourth-line ownership row. Fork it and adapt the fields to your organisation.

## Apply

- Redesign one row of your register so it carries inherent score, residual score, target score, and an aggregation to at least one business service.

## Done When

- Your register can be filtered by business service and by strategic objective, not just by category.


---

[← 2.3 Risk Appetite, Tolerance Levels, and Threshold Definitions](lesson-2-3.md) · [2.5 Risk Treatment Strategies: Accept, Mitigate, Transfer, Avoid →](lesson-2-5.md)
