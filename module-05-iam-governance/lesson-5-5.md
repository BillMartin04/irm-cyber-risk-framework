---
description: User Access Reviews (UAR) and Segregation of Duties (SoD) Conflicts
---

# 5.5 · User Access Reviews (UAR) and Segregation of Duties (SoD) Conflicts

{% hint style="success" %}
**Module 5: Identity & Access** — 4LOD: 1st Line (Access Control Execution) & 2nd Line (Policy Oversight) · Persona: IAM Engineers, Directory Services Admins, Access Governance Officers
{% endhint %}

{% hint style="info" %}
**Watch — 5.5 · User Access Reviews (UAR) and Segregation of Duties (SoD) Conflicts**

A short video lesson accompanies this page. Video links are placeholders until the recording is published to the [TechTalk with Bill YouTube channel](https://www.youtube.com/@techtalkwithbill). Subscribe to be notified when this lesson goes live.
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
