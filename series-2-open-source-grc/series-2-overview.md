---
description: What Series 2 (Open Source GRC) will cover.
---

# Series 2 Overview

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Series 2 Overview — video placeholder
{% endembed %}

## Overview

Series 1 of this handbook covered Integrated Risk Management on ServiceNow — a mature, enterprise-grade commercial platform with deep financial services adoption and strong regulatory credibility. Series 2 takes a different path. It explores whether you can build a credible, production-quality GRC capability using open-source and low-cost tooling — without a ServiceNow license, without a Archer deployment, without a six-figure implementation budget. The honest answer is: yes, to a meaningful degree, for the right organization. Series 2 will show you how, what the trade-offs are, and where open-source tools hit real limits.

This series is currently in development. The pages that follow will be published as content is ready. This overview frames the scope, the tools, and the questions the series intends to answer.

## Key concepts

* **Open-source GRC** — Governance, Risk, and Compliance capability built primarily on tools whose source code is publicly available and freely licensed. This does not mean free to operate — it means free to modify, self-host, and extend. Organizations that choose this path trade license cost for engineering and hosting overhead.
* **OpenComply** — An open-source cloud compliance and controls automation platform (formerly known in the CNAPP space) that maps cloud infrastructure configurations to compliance frameworks (SOC 2, ISO 27001, NIST CSF, CIS Benchmarks) and generates evidence automatically. Strong for technology risk and cloud control monitoring; not a full GRC suite.
* **Eramba** — A community-edition GRC platform built on PHP/MySQL that covers risk management, control management, policy management, and audit management in a single application. Eramba has a genuine risk register, control library, and assessment module — it is the closest open-source analog to a commercial IRM tool. The community edition is free and self-hosted; an enterprise edition with vendor support exists.
* **OpenRMF** — An open-source Risk Management Framework tool focused on NIST RMF compliance, primarily for U.S. federal and defense contexts. Covers System Security Plans, POA&Ms, and control assessments. Less relevant for commercial banking but useful for understanding what structured controls automation looks like at no license cost.
* **GRC Stack** — Series 2 will also look at assembling a "GRC stack" from composable components: a risk register in a structured database or Notion/Airtable, policy management via a wiki, control testing via scripts and cloud scanning tools, and evidence collection via an S3 or SharePoint artifact store. This modular approach trades integration depth for flexibility.
* **Trade-off analysis** — The honest throughline of Series 2. Every open-source choice involves a trade-off: lower cost vs. higher operational burden; flexibility vs. lack of vendor support; community-built features vs. enterprise-hardened capabilities. Series 2 will make these trade-offs explicit rather than evangelical.

## What Series 2 will cover

The planned scope for Series 2 is as follows. This list reflects current thinking and may evolve as content is developed.

| Phase | Topic | Focus |
|---|---|---|
| Phase 1 | Introduction to Open-Source GRC | Why open source, when it makes sense, and when it does not; audience and use cases |
| Phase 1 | Eramba — Setup and Risk Register | Installing Eramba, configuring a risk register, and running a basic risk assessment |
| Phase 1 | Eramba — Controls and Policies | Building a control library, linking controls to risks, and managing policy attestations |
| Phase 2 | OpenComply — Cloud Compliance Automation | Connecting OpenComply to a cloud environment, mapping findings to frameworks, auto-generating evidence |
| Phase 2 | Building a Lightweight GRC Stack | Risk register in Airtable or Notion, evidence store in S3/SharePoint, control testing via scripts |
| Phase 3 | Audit-Readiness on Open Source | Producing an audit trail from open-source tools that an examiner or external auditor will accept |
| Phase 3 | Open-Source vs. Commercial GRC | Head-to-head comparison: what you get with Eramba vs. ServiceNow IRM, and where the gaps are |
| Phase 4 | When to Migrate | Signals that you have outgrown open-source tooling and a migration framework for moving to a commercial platform |

## How Series 2 complements Series 1

Series 1 and Series 2 are designed to be complementary, not competing. They answer different questions for different audiences:

* **Series 1 (ServiceNow IRM)** is for practitioners at organizations that have already invested in ServiceNow, or are evaluating it, and need to build IRM capability on that platform. It is also for anyone who wants to understand what enterprise-grade IRM looks like before evaluating alternatives.
* **Series 2 (Open-Source GRC)** is for smaller financial institutions, fintech startups, and risk professionals at organizations that cannot or will not invest in a commercial GRC platform — and need to know what is realistically achievable without one. It is also useful for practitioners at large organizations who want to understand the tooling landscape before making a platform recommendation.

The maturity model from Phase 4 of Series 1 applies equally to open-source implementations. An organization running Eramba well, with documented risk assessments, tested controls, and evidence attached, can operate at Level 3 maturity. The platform does not determine maturity — the discipline does. What commercial platforms like ServiceNow provide is the infrastructure that makes Level 4 and Level 5 achievable without heroic manual effort.

{% hint style="info" %}
If you are exploring open-source GRC as a starting point with the intention to migrate to a commercial platform later, Series 2's Phase 4 (When to Migrate) will be particularly relevant. It covers how to structure your open-source data so that migration is a lift-and-shift rather than a rebuild.
{% endhint %}

## What to expect as content is published

Series 2 content will be published in phases, following the same structure as Series 1: each page will include a written deep-dive and a video walkthrough. Videos will be linked when available. The GitBook structure is in place; pages will be populated as recordings are completed.

If you are following along in real time, the best way to stay current is to subscribe to the TechTalk with Bill channel where video announcements are made. Each new video corresponds to a page in this handbook.

## In the video

* An honest overview of the open-source GRC landscape as of the series launch date — which tools are actively maintained, which are stagnating, and which are genuinely production-ready.
* A demonstration of Eramba's community edition: what the interface looks like, what data model it uses, and how it compares to ServiceNow IRM at a functional level.
* A walkthrough of OpenComply's cloud compliance scanning — connecting to an AWS account and generating a SOC 2 evidence report automatically.
* A frank discussion of where open-source GRC is not good enough: vendor risk management at scale, board-level reporting, regulatory examination support.

## Key takeaways

* Open-source GRC is a credible option for organizations that lack commercial platform budgets, provided they have the engineering capacity to operate and maintain the tooling.
* Eramba is the most complete open-source IRM analog currently available; its risk register, control library, and audit modules cover the core IRM use cases at no license cost.
* OpenComply fills a specific gap that Eramba does not: automated cloud compliance evidence generation, which is increasingly important as financial services workloads move to AWS, Azure, and GCP.
* The maturity ceiling for open-source GRC is real — continuous monitoring, advanced analytics, and regulatory-grade reporting are significantly harder without a commercial platform's data model and integration ecosystem.
* Series 2 is coming. Follow TechTalk with Bill for publication updates.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
