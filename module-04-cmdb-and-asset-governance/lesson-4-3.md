---
description: Criticality Scoring and Business Impact Analysis (BIA) for Assets
---

# 4.3 · Criticality Scoring and Business Impact Analysis (BIA) for Assets

{% hint style="success" %}
**Module 4: CMDB & Asset Governance** — 4LOD: 1st Line (Operational Ownership & IT Assets) · Persona: Enterprise Architects, CMDB Administrators, IT Operations Leads
{% endhint %}

{% hint style="info" %}
**Watch — 4.3 · Criticality Scoring and Business Impact Analysis (BIA) for Assets**

A short video lesson accompanies this page. Video links are placeholders until the recording is published to the [TechTalk with Bill YouTube channel](https://www.youtube.com/@techtalkwithbill). Subscribe to be notified when this lesson goes live.
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
