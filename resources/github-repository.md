---
description: The companion GitHub repository.
---

# GitHub Repository

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
GitHub Repository — video placeholder
{% endembed %}

## Overview

Every video in this handbook has a companion set of artifacts — update sets, scripts, diagrams, and templates — stored in the public GitHub repository for TechTalk with Bill. The repository is version-tagged to align with specific handbook releases, so you can always retrieve the exact artifacts demonstrated in a given video rather than a later version that may have diverged.

## What's in the Repository

The repository is organized by module area and content type:

| Folder | Contents |
|---|---|
| `/update-sets/` | ServiceNow XML update sets, one per major configuration demo |
| `/diagrams/` | Architecture and data model diagrams (draw.io `.drawio` + exported PNG/SVG) |
| `/templates/` | Risk register templates, assessment questionnaires, RACI matrices, policy templates (XLSX/DOCX) |
| `/scripts/` | Background scripts, scheduled jobs, and Business Rule examples referenced in videos |
| `/cheat-sheets/` | PDF and Markdown cheat sheets for IRM terminology, navigation, and module cross-references |
| `/cert-prep/` | Study guides, practice question sets, and flashcard exports for CSA and CIS-RC |

## Key concepts

* **Release tags** — Each video series has a corresponding Git release tag (e.g., `v1.0-irm-foundations`, `v1.1-advanced-risk`). Always clone or download the tag matching the video you are following — the `main` branch may contain work in progress.
* **Fork vs. clone** — If you intend to customize artifacts for your own implementation, fork the repository first so your changes are isolated from upstream updates. If you only need the artifacts as-is, a standard clone is sufficient.
* **Issues and discussions** — The GitHub Issues tab is where bugs in update sets, errors in diagrams, and content gaps are tracked. The Discussions tab is for broader questions and community conversation. Both feed into the public roadmap.
* **Contributions** — Pull requests are welcome. The contribution workflow is described in the Contributing section of this handbook — content standards, commit message conventions, and the review process.

## In the video

* Navigating the repository structure and finding the right artifacts for a specific video.
* Cloning the repository and checking out a specific release tag.
* Importing an update set from the repository into a ServiceNow PDI.
* Opening a draw.io diagram file in the browser-based editor.

## Key takeaways

* Always use the release tag corresponding to your video — `main` may be ahead of published content.
* Fork the repository before customizing artifacts for production use.
* GitHub Issues is the canonical bug and gap tracker — check it before raising a support question.
* The `/templates/` and `/cheat-sheets/` folders are useful even if you never import an update set.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
