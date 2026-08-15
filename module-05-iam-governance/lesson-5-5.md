---
description: User Access Reviews (UAR) and Segregation of Duties (SoD) Conflicts
---

# 5.5 · User Access Reviews (UAR) and Segregation of Duties (SoD) Conflicts

{% hint style="success" %}
**Module 5: Identity & Access** — 4LOD: 1st Line (Access Control Execution) & 2nd Line (Policy Oversight) · Persona: IAM Engineers, Directory Services Admins, Access Governance Officers
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *User Access Reviews (UAR) and Segregation of Duties (SoD) Conflicts — Identity Access Management Iam (2026)*
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

User Access Reviews (UAR) are the recurring certification that role assignments are still justified. They must be manager-driven (managers certify their own team), scoped by risk (privileged accounts more frequently than standard), and end in an action (revoke, retain, or reassign) — never in a signature with no downstream effect.

Segregation of Duties (SoD) conflicts — one identity holding two entitlements that should not co-exist (e.g. create-vendor and approve-payment) — are surfaced during UAR and treated as findings.

## ServiceNow Implementation Notes

ServiceNow IRM Access Analytics + Access Governance modules run quarterly UAR campaigns. Configure SoD rules once and every campaign inherits them.


## Apply

- Design a quarterly UAR calendar with escalation paths for non-responding managers.

## Done When

- You have delivered the module deliverable: a PAM policy and a quarterly UAR procedure document.


---

[← 5.4 Identity Lifecycle: Joiners, Movers, Leavers (JML) Workflows](lesson-5-4.md) · [Next: Module 6 · Data Protection & Privacy →](../module-06-data-protection-and-privacy/README.md)
