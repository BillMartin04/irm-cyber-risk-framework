---
description: Least Privilege and Role-Based Access Control (RBAC)
---

# 5.1 · Least Privilege and Role-Based Access Control (RBAC)

{% hint style="success" %}
**Module 5: Identity & Access** — 4LOD: 1st Line (Access Control Execution) & 2nd Line (Policy Oversight) · Persona: IAM Engineers, Directory Services Admins, Access Governance Officers
{% endhint %}

{% hint style="info" %}
**Watch — 5.1 · Least Privilege and Role-Based Access Control (RBAC)**

A short video lesson accompanies this page. Video links are placeholders until the recording is published to the [TechTalk with Bill YouTube channel](https://www.youtube.com/@techtalkwithbill). Subscribe to be notified when this lesson goes live.
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
