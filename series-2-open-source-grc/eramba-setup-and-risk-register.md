---
description: Installing Eramba, configuring a risk register, and running a basic risk assessment.
---

# Eramba — Setup and Risk Register

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Eramba — Setup and Risk Register — video placeholder
{% endembed %}

{% hint style="info" %}
**Companion code and artifacts.** The Docker compose files, seed data, and risk register templates referenced on this page live in the public GitHub repository. The URL below is a placeholder until the repository is published.
{% endhint %}

**GitHub repository:** https://github.com/PLACEHOLDER/open-source-grc

## Overview

Eramba is the closest open-source analog to a commercial IRM tool. Its community edition covers risk management, control management, policy management, and audit management in a single self-hosted PHP/MySQL application. This page walks through standing it up and building your first risk register — the foundational artifact every GRC program depends on.

## Installation

* **Docker deployment** — The fastest path is the official Docker image. A `docker-compose.yml` brings up the application, MySQL database, and cron container for scheduled jobs.
* **System requirements** — Eramba is modest: 2 vCPU and 4 GB RAM handle a small program comfortably. Plan for regular MySQL backups from day one.
* **Initial configuration** — On first login, set the organization profile, create user accounts, and configure the SMTP settings so review and attestation notifications work.

## Building the risk register

* **Define the risk taxonomy** — Align your risk categories to a recognized framework (for example the nine domains used in Series 1) so the register maps cleanly to reporting later.
* **Capture inherent risk** — For each risk, record likelihood and impact before controls. Eramba computes a score from your chosen scale.
* **Assign accountable owners** — Every risk gets a named owner. This is the single most important discipline; an unowned risk is not managed.
* **Set review cadence** — Configure periodic review dates so risks are re-assessed rather than left to go stale.

## Running a basic assessment

* Walk a small set of representative risks end to end: identification, scoring, owner assignment, and review scheduling.
* Use Eramba's built-in reports to produce a first risk heat map — the artifact you will show leadership.

## In the video

* A live Docker deployment of Eramba community edition from a clean host.
* Configuring the risk taxonomy and entering the first risks with inherent scoring.
* Assigning owners and review cadences, then generating the risk heat map report.

## Key takeaways

* Eramba's community edition delivers a genuine risk register at no license cost — the core of an IRM capability.
* Docker makes deployment repeatable; backups and patching are your ongoing responsibility.
* Owner assignment and review cadence are what turn a static list into a managed register.
* A clean taxonomy up front makes later control mapping and reporting far easier.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
