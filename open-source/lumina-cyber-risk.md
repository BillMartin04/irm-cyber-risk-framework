---
description: Lumina Cyber Risk — the open-source portal that reflects this course's design patterns.
---

# Lumina Cyber Risk Portal

**Repo:** [github.com/BillMartin04/lumina-cyber-risk](https://github.com/BillMartin04/lumina-cyber-risk)

Lumina Cyber Risk is an open-source cyber-operational-risk portal built by TechTalk with Bill. It is deliberately small — small enough that a solo advisor can fork it, customise the data model, and demo it to a client inside an hour — and deliberately shaped after the enterprise IRM pattern that this course teaches.

## Why it exists

Enterprise IRM platforms (ServiceNow IRM being the reference) express the mature GRC operating model, but you cannot demo them to a client without a licence. Lumina exists to demonstrate the same pattern in an open, forkable form so advisors, consultants, and course learners can practise the architecture without waiting for a paid environment.

## What is in it

- A minimal, readable data model exposing **risk scenarios**, **controls**, **authority documents**, and **assessments**.
- Explicit **4LOD** fields on the risk scenario (`first_line_owner` → `fourth_line_governance`).
- **Framework citation** linking a single control to many authority documents — the UCF pattern.
- Seed data covering three worked scenarios (data breach, privileged-access abuse, third-party outage) end-to-end.

## How this course uses it

Several lessons — especially in Modules 1, 2, 3, 4, and 12 — cite specific Lumina objects as the reference implementation. When a lesson says "see Lumina", open the repo alongside the reading.

## Contributing

Lumina is an open-source project. Contributions are welcome — see the repo's `CONTRIBUTING.md`.

[← Course Home](../README.md)
