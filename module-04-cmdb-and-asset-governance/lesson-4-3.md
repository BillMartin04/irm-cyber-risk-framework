---
description: Criticality Scoring and Business Impact Analysis (BIA) for Assets
---

# 4.3 · Criticality Scoring and Business Impact Analysis (BIA) for Assets

{% hint style="success" %}
**Module 4: CMDB & Asset Governance** — 4LOD: 1st Line (Operational Ownership & IT Assets) · Persona: Enterprise Architects, CMDB Administrators, IT Operations Leads
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *Criticality Scoring and Business Impact Analysis (BIA) for Assets — Servicenow Cmdb (2026)*
**Channel:** [TechTalk with Bill](https://www.youtube.com/@techtalkwithbill)
**Length:** 10–15 min · **Status:** 🎬 In production — subscribe to be notified when this video is published.

**Chapters** (planned)
- 00:00 Intro & why this lesson matters
- 01:30 Definitions and first principles
- 03:30 Four-Lines-of-Defense mapping
- 05:30 ServiceNow implementation walkthrough
- 08:00 Live in action inside Lumina (open source)
- 10:30 Apply this at your organisation this week
- 12:00 Done-When checklist & next lesson

▶ [Subscribe to be notified](https://www.youtube.com/@techtalkwithbill?sub_confirmation=1) · ⭐ [Star the repo](https://github.com/BillMartin04/irm-cyber-risk-framework) · 💬 [Suggest a topic](https://github.com/BillMartin04/irm-cyber-risk-framework/issues)
{% endhint %}
## Read

Business Impact Analysis (BIA) is the discipline of scoring assets not by technical characteristics but by their contribution to business outcomes. A workstation running a legacy application that produces a regulator's quarterly report can be more critical than a rack of production database servers. Criticality scoring must reflect that.

The scoring model should combine at least: business function dependency, data classification carried, regulatory scope, revenue attribution, and recovery time objective (RTO). Assets scored purely on technical dimensions produce misleading risk aggregation.

## ServiceNow Implementation Notes

Use the Business Application record in ServiceNow as the anchor for BIA. RTO / RPO / MTPD live there. Downstream CIs inherit criticality from the Business Application they support.


## Apply

- Score your top ten Business Applications with a documented criticality model.

## Done When

- Every asset in your top-tier risk register has a defensible criticality score.


---

[← 4.2 CMDB Architecture and Data Health (CSDM Alignment)](lesson-4-2.md) · [4.4 Shadow IT Identification, Tracking, and Triage Protocols →](lesson-4-4.md)
