---
description: Connecting OpenComply to a cloud environment, mapping findings to frameworks, and auto-generating evidence.
---

# OpenComply — Cloud Compliance Automation

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
OpenComply — Cloud Compliance Automation — video placeholder
{% endembed %}

{% hint style="info" %}
**Companion code and artifacts.** The deployment manifests, cloud connection configs, and sample evidence reports referenced on this page live in the public GitHub repository. The URL below is a placeholder until the repository is published.
{% endhint %}

**GitHub repository:** https://github.com/PLACEHOLDER/open-source-grc

## Overview

Eramba manages risk and controls, but it does not test your cloud infrastructure. That is where OpenComply fits: an open-source cloud compliance and controls automation platform that reads your cloud configuration, maps it to compliance frameworks, and generates evidence automatically. It fills the gap Eramba leaves — continuous, technical control monitoring for cloud workloads.

## Connecting to a cloud environment

* **Read-only access** — Connect OpenComply using a least-privilege, read-only role. It needs to inspect configuration, not change it.
* **Multi-account support** — Onboard AWS, Azure, or GCP accounts. For financial services, plan for multiple accounts across environments.
* **Scheduled scans** — Configure recurring scans so compliance posture is continuously refreshed rather than a point-in-time snapshot.

## Mapping findings to frameworks

* **Framework coverage** — OpenComply maps infrastructure findings to SOC 2, ISO 27001, NIST CSF, and CIS Benchmarks out of the box.
* **Control-to-finding traceability** — Each finding ties to a specific control requirement, so you can see exactly which controls are passing and failing.
* **Prioritization** — Findings carry severity, letting teams focus remediation where regulatory and security exposure is highest.

## Auto-generating evidence

* **Evidence reports** — OpenComply produces framework-aligned evidence reports automatically — for example a SOC 2 readiness report from a live AWS account.
* **Feeding the GRC record** — These reports become the technical evidence you attach to the corresponding controls in Eramba, closing the loop between risk, control, and proof.
* **Reducing manual effort** — Automated evidence is the single biggest labor saving open source offers over spreadsheet-based control testing.

## In the video

* Connecting OpenComply to an AWS account with a read-only role.
* Running a scan and reviewing findings mapped to SOC 2 and CIS Benchmarks.
* Generating a SOC 2 evidence report and attaching it to an Eramba control.

## Key takeaways

* OpenComply covers the cloud control-testing gap that Eramba does not address.
* Read-only, least-privilege access keeps the tool safe to run in production.
* Automated evidence generation is the strongest labor-saving argument for this stack.
* Feeding OpenComply output into Eramba connects technical proof to your risk register.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
