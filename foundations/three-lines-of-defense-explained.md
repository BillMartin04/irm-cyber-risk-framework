---
description: The Three Lines model and its roles.
---

# Three Lines of Defense Explained

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Three Lines of Defense Explained — video placeholder
{% endembed %}

## Overview

The Three Lines of Defense is the dominant governance model used by financial institutions — and increasingly by all large regulated organizations — to assign accountability for risk management and assurance. Understanding it is not optional background knowledge: it shapes who owns a risk, who tests a control, who issues an audit finding, and how all three groups interact with each other and with the IRM platform. Configuring ServiceNow IRM without understanding the Three Lines model produces a system where no one is sure who is responsible for what, and regulators will notice.

## Key concepts

* **First Line (Business / Operational Management)** — The business units, technology teams, and operational functions that own and execute business processes. The first line is where risk is created and where controls are operated. Risk ownership sits here. In ServiceNow IRM terms, first-line staff are typically the Risk and Control Owners on Entity records and the responders in Risk Assessment campaigns.
* **Second Line (Risk Management and Compliance)** — The independent risk management function (CRO's organization) and the compliance function. The second line sets the risk framework, defines risk appetite, challenges first-line risk assessments, monitors risk posture, and reports to the board and regulators. In ServiceNow IRM, the second line typically owns the platform configuration — the Risk Taxonomy, Control Objective library, Indicator thresholds, and risk reporting dashboards.
* **Third Line (Internal Audit)** — The independent assurance function that tests whether the first and second lines are operating as designed. Internal audit issues Findings against controls and processes, and tracks remediation. In ServiceNow IRM, audit findings are captured as Findings records linked to Controls and Issues, providing a connected audit trail.
* **Board and Executive Management** — Technically outside the three lines but the ultimate accountability layer. The board approves risk appetite, receives risk posture reporting, and holds the CRO/CISO accountable. IRM executive dashboards are designed for this audience.
* **Assurance** — Evidence that controls are working as intended. The Three Lines model produces layered assurance: first-line self-assessment, second-line monitoring and challenge, third-line independent testing. Regulators want to see all three layers functioning and documented.

## How the three lines interact

The model works when each line does its job distinctly and the handoffs are clearly defined. Where organizations fail is when lines blur — business units avoid accountability by pointing to second-line oversight, or internal audit drifts into advisory roles that compromise their independence.

| Activity | First Line | Second Line | Third Line |
|----------|-----------|-------------|------------|
| Owns the risk | Yes | No | No |
| Operates the control | Yes | No | No |
| Sets the risk framework | No | Yes | No |
| Monitors risk posture | Partially | Yes | No |
| Tests control effectiveness | Self-assessment | Challenge / oversight | Independent testing |
| Issues audit findings | No | No | Yes |
| Reports to board | Escalates issues | Risk posture reporting | Audit opinions |
| Approves risk acceptance | Business sponsor | Risk officer sign-off | N/A |

## ServiceNow IRM and the Three Lines

ServiceNow IRM is designed to support all three lines from a single platform. Understanding how the platform is used by each line prevents the common mistake of treating IRM as purely a second-line tool:

**First line in the platform:**
- Risk and Control Owners receive assessment questionnaires and attest to control effectiveness.
- First-line managers review and respond to risk assessments assigned to their Entities.
- Self-identified Issues and control failures are entered directly by operational staff.
- Indicators (KRIs) are fed from first-line operational systems via data integrations.

**Second line in the platform:**
- The IRM team configures and maintains the Risk Taxonomy, Risk Statements, Control Objectives, and Authority Document mappings.
- Second-line risk officers run the assessment campaign calendar and challenge first-line responses.
- The residual risk posture dashboard is owned and maintained by the second line for reporting to the CRO and board.
- Policy attestation and compliance workflows are managed from the Policy & Compliance module.

**Third line in the platform:**
- Internal audit accesses Findings records tied to specific Controls, providing an evidence trail.
- Audit issues are tracked as Findings linked to Issues, with remediation ownership assigned to first-line owners.
- Audit-over-audit visibility — seeing how second-line monitoring identifies the same control gaps — supports the assurance opinion.

{% hint style="warning" %}
**Common pitfall: second line doing first-line work.** A frequent mistake in IRM implementations is having the second-line risk team fill in risk assessment responses on behalf of the business because the business does not engage. This destroys the accountability model: assessments become circular, regulators question the independence of risk oversight, and first-line risk ownership is never truly established. Enforce the model from the start — the platform can enforce workflow routing so that first-line owners must respond before second-line review occurs.
{% endhint %}

## The IIA Three Lines Model (2020 update)

The Institute of Internal Auditors updated the model in 2020, shifting from "Three Lines of Defense" (which implies the primary purpose is defense) to the "Three Lines Model" (which emphasizes contribution to governance). The key changes:

- Stronger emphasis on the governing body (board) as the accountability anchor, not just the recipient of reports.
- Explicit recognition that all three lines serve the organization's objectives, not just risk mitigation.
- Clearer delineation of the second line's advisory and challenge role versus independent assurance (which remains the third line's exclusive domain).

For practical purposes in IRM platform configuration, the structural model is unchanged: first line owns, second line oversees, third line assures. The vocabulary shift matters most in executive communications and governance design documents.

## In the video

* What each of the three lines does — with a concrete banking example showing the same control event viewed from all three perspectives.
* How accountability and assurance flow between lines, and what a regulator expects to see in an exam.
* Common pitfalls when lines blur: second line taking on first-line work, audit drifting into advisory, board receiving compliance reports instead of risk posture.
* How ServiceNow IRM workflow routing enforces the model rather than relying on informal norms.

## Key takeaways

* The Three Lines of Defense is the foundational accountability model for regulated organizations — IRM platform configuration must reflect it, not work around it.
* First line owns and operates controls; second line sets the framework and monitors; third line provides independent assurance.
* ServiceNow IRM serves all three lines from a single platform — the key is configuring role-based access and workflow routing to enforce accountability.
* Blurring the lines — particularly the second line doing first-line work — is one of the most common and damaging IRM implementation failures.
* The 2020 IIA update shifts emphasis to governance contribution, but the structural model is unchanged for platform configuration purposes.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
