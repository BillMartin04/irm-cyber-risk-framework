---
description: Qualitative vs Quantitative Risk Analysis Techniques
---

# 2.2 · Qualitative vs Quantitative Risk Analysis Techniques

{% hint style="success" %}
**Module 2: Risk Registers** — 4LOD: 2nd Line (Risk Management Oversight) · Persona: Risk Analysts, Information Security Managers, Compliance Specialists
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *Qualitative vs Quantitative Risk Analysis Techniques — Cyber Risk Register Explained (2026)*
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

Qualitative risk analysis uses ordinal scales — High / Medium / Low, or 1–5 heat maps — to produce a fast, cheap, defensible triage. Quantitative risk analysis uses distributions over money and time to produce a decision-grade estimate. Both have a place. The organisations that get into trouble are the ones that use qualitative outputs for decisions that demand quantitative rigour — like whether to fund a $10M cyber insurance renewal.

The mature GRC operating model uses qualitative analysis at scale to triage the register, then applies quantitative analysis (see Module 10 for FAIR) to the small set of top-tier risks where a capital or strategic decision is on the table.

## ServiceNow Implementation Notes

ServiceNow IRM ships with a qualitative 5×5 matrix by default. It is worth the effort to add a second scoring scheme that flags risks eligible for quantitative treatment (e.g., annualised loss expectancy above a threshold). That way the register itself signals which risks should be escalated to a FAIR analysis.


## Apply

- Pick your top ten risks. For each, decide whether qualitative scoring is sufficient or a quantitative pass is required.

## Done When

- You have a documented rule for when a risk gets promoted to quantitative analysis.


---

[← 2.1 Threat, Vulnerability, and Impact Identification Methodologies](lesson-2-1.md) · [2.3 Risk Appetite, Tolerance Levels, and Threshold Definitions →](lesson-2-3.md)
