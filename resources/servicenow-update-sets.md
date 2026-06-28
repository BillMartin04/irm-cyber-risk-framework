---
description: Downloadable ServiceNow update sets.
---

# ServiceNow Update Sets

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
ServiceNow Update Sets — video placeholder
{% endembed %}

## Overview

Update sets are the primary mechanism for moving ServiceNow configuration between instances. Every major configuration demonstrated in this handbook — Risk Register structure, assessment workflows, KRI feeds, Entity hierarchy setup, Control Objective libraries — is packaged as a downloadable XML update set in the companion GitHub repository. You import the update set into your Personal Developer Instance (PDI) or sandbox, preview it, and commit it to replicate the exact configuration shown in the video.

## Key concepts

* **Update set** — A collection of ServiceNow configuration records (fields, forms, workflows, ACLs, UI actions, business rules, etc.) exported as a single XML file. Update sets do not contain data records — only configuration. This means importing an IRM update set will install the structural configuration without overwriting your existing risk or control data.
* **Preview before commit** — Always preview an update set before committing. The preview step identifies conflicts with existing configuration on your target instance. Review every conflict record individually; do not auto-resolve unless you understand the impact.
* **Batch vs. incremental sets** — Some videos ship a single comprehensive update set for the full module configuration; others ship incremental sets that build on a prior video's set. The README in each `/update-sets/` subfolder specifies the dependency order — import parent sets first.
* **Instance compatibility** — Each update set in the repository is tagged with the ServiceNow release it was built on (e.g., `xanadu`, `yokohama`). Importing an update set from a newer release into an older instance may cause errors. Check the compatibility note in the release tag README before importing.

## Import Procedure

1. Download the XML file from the GitHub repository (specific release tag, not `main`).
2. In ServiceNow, navigate to **System Update Sets → Retrieved Update Sets**.
3. Click **Import Update Set from XML** and upload the file.
4. Open the retrieved update set record and click **Preview Update Set**.
5. Review all conflict records. Address any that affect active production configuration.
6. Click **Commit Update Set** to apply the configuration to your instance.

{% hint style="warning" %}
Never commit an update set directly to a production instance without previewing and testing in a sub-production sandbox first. Update sets that modify ACLs, workflows, or Business Rules can have unintended side effects on live GRC data.
{% endhint %}

## Available Update Sets (Catalog)

| Update Set Name | Covers | Prerequisite |
|---|---|---|
| `irm-foundations-v1` | Risk Register structure, Risk Statements, Entity hierarchy, basic Control Objectives | None |
| `irm-assessments-v1` | Assessment templates, scoped risk assessments, evidence collection tasks | `irm-foundations-v1` |
| `irm-kri-indicators-v1` | KRI/Indicator configuration, threshold alerts, escalation rules | `irm-foundations-v1` |
| `irm-tprm-v1` | Third-Party Risk profiles, vendor assessment questionnaire, BAA tracking | `irm-foundations-v1` |
| `irm-cri-profile-v1` | CRI Profile control objective library (financial services) | `irm-foundations-v1` |
| `irm-cam-v1` | Continuous Authorization and Monitoring setup, POAM workflow | `irm-assessments-v1` |

## In the video

* Walking through the full import procedure — download, upload, preview, conflict review, commit.
* Demonstrating what each foundation update set installs and how to verify the configuration.
* Showing how to create your own update set to capture customizations made after import.

## Key takeaways

* Update sets install configuration, not data — they are safe to import into an instance with existing GRC content, provided you preview conflicts first.
* Always match the update set release tag to your ServiceNow instance version.
* Import in dependency order — foundation sets before module-specific sets.
* Create a local update set in your instance before making any additional customizations, so your changes are captured and portable.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
