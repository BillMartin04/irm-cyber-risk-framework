---
description: What you need before starting.
---

# Prerequisites and Tools

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Prerequisites and Tools — video placeholder
{% endembed %}

## Overview

This page covers the access, tools, and baseline knowledge that make following along with the handbook as productive as possible. Having the right environment before you start the hands-on sections removes friction and lets you focus on the IRM concepts and platform configuration rather than troubleshooting access issues. Most practitioners can be set up in under an hour.

## Key concepts

* **Personal Developer Instance (PDI)** — ServiceNow's free developer program provides a full-featured instance you can request at developer.servicenow.com. A PDI is the fastest way to follow along without touching a production or customer environment. Instances are provisioned with a recent release and can have plugins activated on demand.
* **IRM / GRC Plugin** — The IRM capability on ServiceNow is delivered through the GRC plugin (formally `com.snc.grc`). In a PDI, activate it via the Plugin Manager. In an enterprise instance, your ServiceNow admin or platform team controls activation. Confirm the plugin is active before starting Series 1.
* **Scope and application** — Most IRM configuration lives in the `sn_risk` and `sn_compliance` scopes. Understanding which scope a table or module belongs to matters when you are troubleshooting or customizing. This handbook works in the global scope for clarity unless a scoped app is specifically called out.
* **Browser and browser tools** — A modern Chromium-based browser (Chrome or Edge) is recommended. The ServiceNow UI behaves consistently across these. Browser developer tools are occasionally useful for troubleshooting form layouts or inspecting field names.
* **Baseline navigation skills** — You should be comfortable with: navigating via the Application Navigator, opening and editing records in list and form views, using filters and queries in list views, and understanding basic relationships (parent/child records, related lists). If any of these are unfamiliar, work through ServiceNow's free Welcome to ServiceNow learning path before continuing.

## Platform requirements by section

| Section | Minimum requirement |
|---------|---------------------|
| Foundations | No instance needed — conceptual content only |
| Series 1, Phase 1 (Setup & Authority Documents) | PDI or sandbox with GRC plugin active |
| Series 1, Phase 2 (Risk Register & Assessments) | GRC plugin + Risk Management module enabled |
| Series 1, Phase 3 (Control Testing & Evidence) | GRC plugin + Policy & Compliance module |
| Series 1, Phase 4 (Reporting & Dashboards) | GRC plugin + Performance Analytics (PA) |
| Advanced Risk (CRI Profile, Continuous Auth) | Advanced Risk license or equivalent entitlement |

{% hint style="warning" %}
**PDI reset policy.** ServiceNow reclaims inactive PDIs after a period of inactivity. If your instance is reset, you will need to re-activate plugins and re-import any configuration you created. Save exports of key records — Risk Statements, Control Objectives — as update sets or Excel exports as you build.
{% endhint %}

## Supporting assets

The handbook references a set of supporting assets used across multiple sections:

* **Authority Document library** — A pre-built set of UCF (Unified Compliance Framework) citations or manually authored authority documents aligned to NIST CSF, ISO 27001, and PCI DSS. These are loaded in Phase 1 and referenced throughout.
* **Risk Statement templates** — A starter library of Risk Statements formatted as `[Threat/Event] + [Asset/Process] + [Impact]` tuples, organized by risk category (cyber, operational, third-party, regulatory).
* **Control Objective library** — A tiered set of Control Objectives mapped to authority document citations, suitable for immediate use or adaptation to your organization's control framework.
* **KRI / Indicator library** — A set of pre-built Indicators (KRIs and KPIs) with threshold definitions, ready to attach to Entities and Risk Statements.
* **Excel import templates** — For organizations importing existing risk registers or control lists, formatted import templates aligned to ServiceNow IRM table structures are provided.

Links to download each asset are in the Resources section of the handbook.

## Background knowledge recommendations

The following are helpful but not mandatory. Each is noted where it becomes relevant:

* **GRC concepts** — Familiarity with terms like risk appetite, residual risk, control objective, and attestation speeds up the Foundations section. The [GRC Terminology Glossary](../foundations/grc-terminology-glossary.md) covers all of these.
* **Regulatory frameworks** — A working awareness of NIST CSF, ISO 27001, or SOC 2 helps the authority document and framework mapping chapters land faster. The [Regulatory Frameworks Overview](../foundations/regulatory-frameworks-overview.md) provides a primer.
* **Operational risk in financial services** — For practitioners in banking or insurance, familiarity with Basel operational risk categories, the Three Lines of Defense, and regulatory exam processes adds depth to the financial-services use cases.

## In the video

* How to request a free PDI and activate the GRC plugin step by step.
* A tour of the IRM modules and how they are structured in the Application Navigator.
* Where to download the supporting assets and how they are used in later sections.
* A quick orientation to the tables and scopes that matter most for IRM configuration.

## Key takeaways

* A free PDI from developer.servicenow.com is sufficient for all Series 1 hands-on work.
* Activate the GRC plugin before starting Phase 1; Advanced Risk features require an additional entitlement.
* Save your work as update sets or exports — PDIs can be reset and configuration lost.
* Download the supporting asset library before starting Series 1; it accelerates every phase.
* Basic ServiceNow navigation skills are the only hard prerequisite; everything else is taught as you go.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
