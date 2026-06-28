---
description: How the watch-read-apply format and navigation work.
---

# How to Use This Handbook

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
How to Use This Handbook — video placeholder
{% endembed %}

## Overview

This handbook is not a passive reading experience. Each page is designed around a three-part loop — Watch, Read, Apply — that builds both conceptual understanding and hands-on skill in parallel. The structure is deliberate: Foundations pages establish shared vocabulary; Series 1 phases build a working IRM implementation step by step; and Industry Use Cases show how the same constructs solve real problems in regulated environments. Understanding the format before you start makes every subsequent page faster and more actionable.

## Key concepts

* **Watch-Read-Apply loop** — The core learning unit of this handbook. Every page pairs a focused video with a written explanation and a concrete next action. The video demonstrates; the page explains the reasoning; the Apply step gives you something to do in your own instance or design document before moving on.
* **Section hierarchy** — Content is organized in three tiers: top-level sections (Foundations, Series 1, Industry Use Cases, Resources), subsections within each (e.g., Foundations has five pages), and individual pages. Navigation in the left panel reflects this hierarchy. You do not need to read every section — the [Learning Path Recommendations](learning-path-recommendations.md) page helps you find the right entry point for your role.
* **Platform-grounded writing** — Every page that touches ServiceNow IRM uses the real names of platform constructs: Risk Register, Risk Statement, Control Objective, Control, Indicator, Entity, Profile, Authority Document, Policy, Attestation, Issue, Finding, Risk Assessment, Advanced Risk, CRI Profile. This is intentional. Vague generic language does not help you configure anything.
* **Checkpoint pattern** — At the end of each Series 1 phase, there is a checkpoint that describes what a correctly configured instance should look like at that point. Use these checkpoints to verify your work before moving to the next phase.
* **GitBook hint blocks** — Throughout the handbook, colored hint blocks call out important notes (`{% hint style="info" %}`), warnings about common mistakes (`{% hint style="warning" %}`), and tips that accelerate configuration (`{% hint style="success" %}`). Pay attention to warning blocks in particular — they flag the configuration choices that are hardest to undo.

## How each page is structured

A standard handbook page follows this layout:

1. **Frontmatter** — A one-line description used by GitBook for search and navigation. Not visible in the rendered page.
2. **H1 title** — The page name.
3. **Video block** — The hint block noting the video is coming, followed by the embedded YouTube player. Watch the video first when it is available; it is shorter and gives you a mental model before the written detail.
4. **Overview** — Two to four sentences on why this topic matters and what the page covers. Read this to decide whether to go deep or skim.
5. **Key concepts** — Bolded terms with plain-language definitions. These build the vocabulary used in the rest of the page and across the handbook.
6. **Topic-specific sections** — The substantive content: step-by-step instructions, comparison tables, platform configuration details, financial-services examples. This is where most of the learning happens.
7. **In the video** — Bullets previewing what the video demonstrates. Useful if you are revisiting a page and want to know whether the video adds new information.
8. **Key takeaways** — Three to five crisp bullets summarizing what to remember and act on.

## Navigation patterns

**Linear reading:** If you are new to IRM or new to ServiceNow GRC, read Foundations in order, then follow Series 1 phase by phase. Each phase builds on the previous one — skipping ahead creates gaps that surface as confusing configuration errors later.

**Reference lookup:** If you are an experienced practitioner looking for a specific topic, use the left panel search or jump directly to the relevant page. The [GRC Terminology Glossary](../foundations/grc-terminology-glossary.md) and [Regulatory Frameworks Overview](../foundations/regulatory-frameworks-overview.md) are designed as standalone references.

**Role-based paths:** The [Learning Path Recommendations](learning-path-recommendations.md) page maps specific roles (GRC analyst, ServiceNow admin, CISO, internal auditor) to the subset of pages most relevant to each. If your time is limited, start there.

{% hint style="info" %}
**Tip:** Open your ServiceNow instance in a second browser window while reading the hands-on sections. Configuration decisions are much easier to evaluate when you can see the actual platform UI at the same time as the written instructions.
{% endhint %}

## In the video

* A tour of the handbook structure and left-panel navigation in GitBook.
* How to follow along in your own instance while reading.
* Where supporting assets (templates, import files, glossary) live and how they connect to specific pages.
* How to use the checkpoint pattern to verify your Series 1 build at each phase boundary.

## Key takeaways

* The Watch-Read-Apply loop is the core learning unit — use all three parts for maximum retention.
* Foundations first, then Series 1 in phase order; skipping ahead creates configuration gaps.
* Platform constructs are always named precisely — treat the exact names as part of the learning.
* Hint blocks signal what matters most: info for context, warning for risks, success for shortcuts.
* Use the Learning Path Recommendations page to find your optimal entry point if you are not starting from scratch.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
