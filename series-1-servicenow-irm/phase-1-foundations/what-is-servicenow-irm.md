---
description: Introduce the ServiceNow IRM application.
---

# What Is ServiceNow IRM

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
What Is ServiceNow IRM — video placeholder
{% endembed %}

## Overview

ServiceNow Integrated Risk Management (IRM) is a suite of applications built on the Now Platform that brings governance, risk, and compliance work onto a single shared data model. For a bank or financial institution, that matters because risk decisions are only as good as the data feeding them — and when risk lives in spreadsheets, controls live in a separate GRC tool, and audit findings live in email chains, you end up with three versions of the truth and a lot of manual reconciliation. IRM eliminates that fragmentation by making every risk, control, policy, assessment, and finding a connected record that any authorized stakeholder can act on in real time.

## Key concepts

- **Risk Register** — The central repository for all identified risks in the organization. Each risk record holds a risk statement, category, owner, inherent and residual scores, and links to the controls that mitigate it. In a retail bank this might contain several hundred operational risk entries spanning fraud, IT outages, third-party failures, and regulatory breaches.
- **Risk Statements** — Structured descriptions of a risk event and its consequence, written in the format "there is a risk that [event] resulting in [impact]." ServiceNow stores these as reusable records that can be associated with multiple entities — a single "unauthorized data access" statement might apply to dozens of business processes across the bank.
- **Entities and Profiles** — The organizational objects (business units, processes, vendors, applications) against which risks and controls are scoped. A retail bank might define entities for Mortgage Origination, Payments Processing, and Core Banking Platform; each entity carries its own risk and control profile.
- **Control Objectives and Controls** — Control Objectives express the desired state (e.g., "all privileged access changes are authorized and logged"); Controls are the specific activities, policies, or technical measures that achieve the objective. ServiceNow links both to the risks they mitigate and the regulatory requirements they satisfy.
- **Indicators and KRIs** — Key Risk Indicators are quantitative signals that a risk is moving toward its threshold. ServiceNow IRM ingests automated data feeds or manual inputs to update indicator values, trigger alerts, and escalate to risk owners when thresholds are breached. A common banking KRI is "percentage of overdue access reviews."
- **Policy & Compliance** — The application that manages the policy lifecycle (draft, review, publish, attest) and maps policy requirements to authority documents such as OCC guidelines, FFIEC handbooks, or the NIST Cybersecurity Framework. Controls can be automatically linked to policy statements.
- **Risk Assessments** — Structured workflows that scope a set of risks or controls for evaluation, assign scorers, collect responses, and aggregate results against a risk appetite or scoring methodology. Assessments can be scoped to an entity, a process, a third party, or a specific framework.
- **Advanced Risk** — An extended capability for quantitative risk analysis, Monte Carlo simulation, and scenario-based modeling. Used by second-line risk teams to calculate Value-at-Risk estimates and present probabilistic loss distributions to executive committees.

## How the modules connect

The power of ServiceNow IRM is relational: modules share data rather than duplicate it. The diagram below shows the primary linkages.

```
Policy & Compliance
  └─ Authority Documents → Policy Statements → Control Objectives
                                                      │
Risk Register                                         ▼
  └─ Risk Statements → Risks → Controls (shared) → Assessments
         │                         │
         ▼                         ▼
     Entities/Profiles          Issues & Findings
         │
         ▼
     Indicators / KRIs → Automated alerts → Risk owners
```

In practice, a compliance team's control attestation result feeds directly into the risk score for the associated risk record. When an auditor raises a finding against a control, that finding is linked to the same control record the second-line team is monitoring — not a separate spreadsheet. That closed loop is the structural advantage that ServiceNow IRM delivers over any collection of point tools.

## IRM in a banking context

A regional bank with $50B in assets might use ServiceNow IRM to manage:

- **Operational risk**: Several hundred risk statements across business lines, each scoped to entities and reviewed quarterly.
- **Third-party risk**: Vendor profiles with inherent risk scores, control assessments, and issue tracking for critical suppliers.
- **Regulatory exam management**: OCC and Fed examination requests linked directly to controls and evidence, with response workflows tracked in the platform.
- **Cyber risk**: CRI Profile and NIST CSF control mappings feeding a continuous monitoring dashboard for the CISO and board risk committee.

None of these programs require separate tooling; they share the same risk and control records, the same scoring methodology, and the same reporting layer.

## In the video

- A live walkthrough of the IRM application navigator and the key modules.
- How a risk record connects to controls, assessments, and indicators.
- A real example showing how an operational risk entry in the Risk Register links to a compliance control and a KRI alert.
- Why the shared data model changes the economics of risk program management.

## Key takeaways

- ServiceNow IRM unifies Risk Management, Policy & Compliance, Audit Management, and Advanced Risk on one platform with a shared data model.
- Core record types — Risk Register, Risk Statements, Entities, Controls, Indicators, Assessments, Issues — are all connected, not siloed.
- For banks and financial institutions, this integration directly addresses the fragmentation that makes regulatory exams, third-party risk programs, and operational risk reporting expensive and error-prone.
- Indicators and KRIs provide automated, real-time signals that shift risk management from periodic point-in-time reviews to continuous monitoring.
- Advanced Risk extends the platform into quantitative analysis, bridging operational risk management and enterprise risk appetite.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
