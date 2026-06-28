---
description: How to contribute to this project.
---

# How to Contribute

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
How to Contribute — video placeholder
{% endembed %}

## Overview

This handbook and its companion repository are community resources. Contributions — whether a typo correction, a new cheat sheet, an improved diagram, or a more thorough code example — make the content better for every IRM practitioner who uses it. The contribution process is designed to be lightweight for small fixes and structured for larger additions, with a clear review path in both cases.

## Key concepts

* **GitHub Pull Requests** — All content contributions are submitted as Pull Requests (PRs) to the companion GitHub repository. The PR description should explain what changed and why. PRs go through a maintainer review before merge. Small fixes (typos, broken links, formatting) are typically reviewed and merged within a few days; larger content additions require more thorough review.
* **Issues as proposals** — Before investing significant time writing a new section or building a new update set, open a GitHub Issue first to describe what you intend to contribute. This avoids duplicate effort and confirms the content fits the handbook's scope and structure. Use the "Content Proposal" issue template.
* **Scope boundary** — This handbook covers ServiceNow IRM and cyber risk. Contributions should stay within that scope. Content about other ServiceNow product suites, general IT management, or non-IRM GRC tools will not be accepted. When in doubt, check with a maintainer via the Discussions tab before writing.
* **Formatting standards** — Markdown content should follow the handbook's established structure: frontmatter, H1, hint/embed block, body sections as specified in the Enrichment Contract, footer line. Do not introduce new page types or restructure existing pages without maintainer agreement.

## Contribution Workflow

1. **Check for existing Issues.** Search open Issues and Discussions before starting. Someone may already be working on the same improvement.
2. **Open an Issue (for non-trivial changes).** Use the appropriate template: Bug Report, Content Proposal, or Update Set Issue. Describe the problem or proposed addition clearly.
3. **Fork the repository.** Work in your own fork, not in a branch on the main repo. Keep your fork's `main` branch in sync with upstream.
4. **Create a branch.** Use a descriptive branch name: `fix/typo-banking-page`, `content/fintech-kri-example`, `update-set/irm-tprm-v2`.
5. **Make your changes.** Follow the formatting and scope standards. For update sets, test in a PDI before submitting. For diagrams, include both the `.drawio` source and an exported PNG.
6. **Submit a Pull Request.** Reference the related Issue in the PR description. Fill out the PR template completely — incomplete PRs slow down review.
7. **Respond to review feedback.** Maintainers may request changes. Engage constructively and promptly — PRs that go silent for two weeks may be closed and re-opened later.

## Content Standards

* Write in the handbook's voice: authoritative, specific, practical. No filler. No emojis. No generic best-practice platitudes without concrete examples.
* Use real ServiceNow construct names (Risk Statement, Control Objective, Entity Profile, etc.) consistently.
* If you reference a specific ServiceNow release behavior, note the release version.
* Diagrams must be editable (draw.io source required, not just image exports).
* Update sets must be tested against a PDI on a supported release and include a README with prerequisites and compatibility notes.

{% hint style="info" %}
The fastest path to a merged contribution is a well-scoped, well-described Issue opened before you start writing. Maintainers can confirm scope fit and flag any conflicts with in-progress work in the roadmap.
{% endhint %}

## In the video

* Navigating the GitHub repository structure and finding the right place to submit content.
* Opening a Content Proposal Issue and filling out the template.
* The full fork → branch → PR workflow demonstrated step by step.
* What maintainers look for in a PR review.

## Key takeaways

* Open an Issue before writing substantial new content — it prevents wasted effort and scope conflicts.
* All contributions go through PR review; the standards are high because the audience relies on accuracy.
* Update sets must be tested in a PDI before submission — untested code is not accepted.
* Diagrams require the `.drawio` source file, not just exported images.
* The handbook's voice is expert and concrete — match it when writing new content.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
