---
description: Threat, Vulnerability, and Impact Identification Methodologies
---

# 2.1 · Threat, Vulnerability, and Impact Identification Methodologies

{% hint style="success" %}
**Module 2: Risk Registers** — 4LOD: 2nd Line (Risk Management Oversight) · Persona: Risk Analysts, Information Security Managers, Compliance Specialists
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *Threat, Vulnerability, and Impact Identification Methodologies — Cyber Risk Register (2026)*
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

Threats, vulnerabilities, and impacts are three different objects in the risk model, and analysts who blur them produce risk registers no one can act on. A **threat** is an actor or event capable of causing harm. A **vulnerability** is a weakness that a threat could exploit. An **impact** is the business consequence if exploitation succeeds. A risk statement is the product of all three — it needs a threat source, an exploited weakness, and a described business consequence.

The identification methodologies that produce these three objects are also different. Threat identification is intelligence-led and typically borrows from MITRE ATT&CK, ISACs, and vendor telemetry. Vulnerability identification is scan- and assessment-led. Impact identification is business-led and depends heavily on the Business Impact Analysis you will meet in Module 4.

## ServiceNow Implementation Notes

In ServiceNow IRM, the Risk record binds these three together. A useful discipline is to require every Risk to name at least one Threat Source, at least one Vulnerability (linked to a CI or process), and at least one Impact Category (financial, regulatory, reputational, operational). Instances that only capture a free-text description are almost always producing risks that cannot be aggregated at the board level.


## Apply

- Take three of your current risk register entries and decompose each into threat, vulnerability, and impact. Notice which entries collapse — those are candidates to rewrite.

## Done When

- You can write a risk statement in threat / vulnerability / impact form without a template.


---

[← Module 2 Overview](README.md) · [2.2 Qualitative vs Quantitative Risk Analysis Techniques →](lesson-2-2.md)
