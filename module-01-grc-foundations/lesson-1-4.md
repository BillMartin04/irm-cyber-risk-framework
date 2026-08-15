---
description: The Four Lines of Defense (4LOD) Model in Practice
---

# 1.4 · The Four Lines of Defense (4LOD) Model in Practice

{% hint style="success" %}
**Module 1: GRC Foundations** — 4LOD: 4th Line (Governing Body) & 2nd Line (Risk Oversight) · Persona: Aspiring GRC Analysts, IT Auditors, Junior Risk Officers
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *The Four Lines of Defense (4LOD) Model in Practice — Grc Governance Risk Compliance (2026)*
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

The classic Three Lines of Defense model — first-line operations, second-line risk oversight, third-line independent audit — is being displaced in modern regulated industries by the **Four Lines of Defense (4LOD)** model. The fourth line is the **governing body**: the board and its committees, along with external assurance functions such as regulators and external auditors. Naming the fourth line explicitly forces a design conversation: where does board-level risk appetite actually get set, and who is empowered to challenge management at that level.

This entire course is aligned to the 4LOD model. Every module lists the line or lines of defense it primarily serves. When you finish the course, you should be able to look at any control, policy, or KRI in your organisation and immediately name which line owns it, which line oversees it, and which line assures it. That mapping is the foundation of a defensible GRC program.

## ServiceNow Implementation Notes

Inside ServiceNow IRM, 4LOD is expressed through role assignment on Risks, Assessments, and Issues: an owner (1st line), a risk manager (2nd line), an internal auditor (3rd line), and an executive sponsor / risk committee (4th line). If your instance only carries one owner field on each record, you are missing the oversight signal that makes IRM defensible.

## Live in Action — Lumina Cyber Risk (Open Source)

Lumina exposes 4LOD in the risk-scenario view: every scenario carries `first_line_owner`, `second_line_oversight`, `third_line_assurance`, and `fourth_line_governance`. Use it as a visual reference for how a real record should be structured.

## Apply

- Draw the 4LOD model for your own organisation. Fill in the actual named human at each line for one specific risk.
- Identify a control where the same person appears in more than one line. That is a governance defect — capture it.

## Done When

- You can explain 4LOD to a peer without notes.
- You have one worked example that names every line for a real control.


---

[← 1.3 Organizational Structures: Board, CISO, CIO, and Audit Committees](lesson-1-3.md) · [1.5 Establishing a GRC Charter and Stakeholder Engagement Plan →](lesson-1-5.md)
