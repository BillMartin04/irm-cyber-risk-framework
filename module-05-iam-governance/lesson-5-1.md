---
description: Least Privilege and Role-Based Access Control (RBAC)
---

# 5.1 · Least Privilege and Role-Based Access Control (RBAC)

{% hint style="success" %}
**Module 5: Identity & Access** — 4LOD: 1st Line (Access Control Execution) & 2nd Line (Policy Oversight) · Persona: IAM Engineers, Directory Services Admins, Access Governance Officers
{% endhint %}

{% hint style="info" %}
### 📺 Watch on YouTube

**Video title:** *Least Privilege and Role-Based Access Control (RBAC) — Identity Access Management Iam (2026)*
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

Least Privilege says every identity receives only the access required for its current role, and no more. Role-Based Access Control (RBAC) is the primary mechanism for enforcing it at scale. Well-designed RBAC has a small number of well-named roles, each mapped to a business function, with entitlements curated centrally. Poorly-designed RBAC has hundreds of roles that were created ad hoc and no one is willing to retire.

The GRC governance question is not whether RBAC exists — it always does — but whether it is defensible. Can you show an auditor that every entitlement in a role is justified by a business function? Can you show that role assignments are reviewed on a schedule? Those are the questions the Access Review process (5.5) is designed to answer.



## Apply

- Pick one high-privilege role and inspect its entitlements. Justify each one against a business function or flag it for removal.

## Done When

- You have a documented least-privilege statement for at least one critical role.


---

[← Module 5 Overview](README.md) · [5.2 Privileged Access Management (PAM) Architecture and Vaulting Controls →](lesson-5-2.md)
