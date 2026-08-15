---
description: 'The GRC Ecosystem: Governance, Risk Management, and Compliance Definitions'
---

# 1.1 · The GRC Ecosystem: Governance, Risk Management, and Compliance Definitions

{% hint style="success" %}
**Module 1: GRC Foundations** — 4LOD: 4th Line (Governing Body) & 2nd Line (Risk Oversight) · Persona: Aspiring GRC Analysts, IT Auditors, Junior Risk Officers
{% endhint %}

{% hint style="info" %}
**Watch — 1.1 · The GRC Ecosystem: Governance, Risk Management, and Compliance Definitions**

A short video lesson accompanies this page. Video links are placeholders until the recording is published to the [TechTalk with Bill YouTube channel](https://www.youtube.com/@techtalkwithbill). Subscribe to be notified when this lesson goes live.
{% endhint %}
## Read

Governance, Risk, and Compliance are three distinct disciplines that too many organisations still treat as one team on one spreadsheet. **Governance** is the exercise of authority: it defines who owns which decisions, what risk appetite the board is willing to underwrite, and how leaders will be held accountable when things go wrong. **Risk Management** is the disciplined identification, analysis, and treatment of the events that could stop the organisation from meeting its objectives. **Compliance** is the operational assurance that the organisation is meeting its externally imposed obligations — laws, regulations, and contractual duties — and can demonstrate it.

The three functions are related but not interchangeable. Governance sets the boundaries. Risk management prices the choices inside those boundaries. Compliance proves the choices survive external scrutiny. When leaders collapse the three into one function, the failure mode is predictable: the compliance calendar consumes all available capacity, real risk decisions stop being made, and governance quietly delegates itself to a control tester.

In this course we will consistently separate the three lenses. Every risk you assess will be tagged to a governance owner and a compliance framework. Every compliance control you implement will be tied back to a risk it is supposed to reduce. That discipline is what turns a GRC function from a cost centre into an executive advisory capability.

## ServiceNow Implementation Notes

ServiceNow IRM implements this separation in the data model. Governance sits in the **Policy and Compliance** application (policies, control objectives, authority documents). Risk lives in **Risk Management** (risk statements, risk register, risk assessments). Compliance is expressed through **Regulatory Change Management** and citation mapping to authority documents.

A common implementation mistake is to force everything through a single Assessment record. In a healthy CSDM-aligned deployment, the Risk record is the enduring artefact and Assessments are the recurring evidence pass. Governance ownership is asserted through the Business Application, Service, and CI hierarchy — not through free-text fields on the risk itself.

## Live in Action — Lumina Cyber Risk (Open Source)

The open-source [Lumina Cyber Risk portal](https://github.com/BillMartin04/lumina-cyber-risk) demonstrates the same separation with a small, readable data model: `governance_policy`, `risk_scenario`, `compliance_obligation`. Every scenario references at least one policy owner and at least one obligation, so you can walk the graph in either direction.

Open the Lumina repo alongside this lesson and inspect the seed data. It is deliberately small so the boundaries are obvious.

## Apply

- Write a one-sentence definition of Governance, Risk, and Compliance for your own organisation.
- For your last three security decisions, tag each one as primarily G, R, or C. Notice how many were driven by C.
- Identify one control that exists in your compliance calendar without a clearly owned risk statement. That is a candidate to retire.

## Done When

- You can explain to a non-technical executive what each of G, R, and C actually decides.
- You have a working example of one control in your organisation tied to one risk and one authority document.


---

[← Module 1 Overview](README.md) · [1.2 Internal GRC Analyst vs External Strategic Advisor Roles →](lesson-1-2.md)
