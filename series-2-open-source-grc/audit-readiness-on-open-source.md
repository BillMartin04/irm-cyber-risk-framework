---
description: "Producing an audit trail from open-source tools that an examiner or external auditor will accept."
---

# Audit-Readiness on Open Source

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Audit-Readiness on Open Source — video placeholder
{% endembed %}

{% hint style="info" %}
**Companion code and artifacts.** The evidence-package templates, audit-trail exports, and mapping spreadsheets referenced on this page live in the public GitHub repository. The URL below is a placeholder until the repository is published.
{% endhint %}

**GitHub repository:** https://github.com/PLACEHOLDER/open-source-grc

## Overview

The real test of any GRC capability is not the interface — it is whether it survives an audit. This page shows how to produce an audit trail from open-source tooling that an internal auditor, external assurance provider, or regulator will accept. The tooling is different from a commercial platform; the evidence standard is not.

## What auditors actually want

* **Cause, control, consequence, cure** — A traceable chain from each risk to the control that treats it, to the evidence the control operated, to the remediation when it failed.
* **Completeness** — Assurance that the population of risks and controls is complete, not a convenient subset.
* **Independence and integrity** — Confidence that evidence was not altered after the fact and that testing was performed as claimed.
* **Timeliness** — Evidence dated across the audit period, not assembled the night before the examination.

## Producing the audit trail

* **Immutable evidence storage** — Store evidence in a location with versioning and access logging (for example S3 with object lock) so integrity is demonstrable.
* **Timestamped, automated collection** — Control-testing scripts and OpenComply scans that write dated evidence continuously beat manual collection on both effort and credibility.
* **Traceability mapping** — Maintain the risk-to-control-to-evidence mapping (from the Eramba pages or the lightweight stack) as the spine of the evidence package.
* **Change history** — Keep policy and control changes in version control so the auditor can see what changed, when, and by whom.

## Assembling the evidence package

* Export the risk register, control library, and test results into a structured package organized by control.
* Include the attestation records for policies and the versioned policy documents themselves.
* Provide the auditor a single index that ties each control to its evidence artifacts and dates.

## Where open source needs extra effort

* **Aggregated reporting** — You may need to script the roll-ups a commercial platform produces natively.
* **Access governance** — Demonstrating segregation of duties across composable tools requires deliberate configuration.
* **Continuity** — Auditors expect the evidence pipeline to be resilient; document backups and ownership.

## In the video

* Walking an examiner-style trace from a single risk through its control to dated evidence.
* Exporting an evidence package from Eramba and the evidence store into an audit-ready structure.
* Demonstrating evidence integrity with versioned, access-logged storage.

## Key takeaways

* Auditors judge the evidence standard, not the tool — open source can meet it with discipline.
* Immutable, timestamped, automated evidence is both less work and more credible than manual collection.
* The risk-to-control-to-evidence mapping is the backbone of an acceptable audit trail.
* Plan extra effort for aggregated reporting and segregation-of-duties evidence.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
