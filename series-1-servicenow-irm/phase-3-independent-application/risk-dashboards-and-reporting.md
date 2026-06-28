---
description: Build dashboards and reports independently.
---

# Risk Dashboards and Reporting

{% hint style="info" %}
**Video coming soon.** The link below is a placeholder until the video is published.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=PLACEHOLDER" %}
Risk Dashboards and Reporting — video placeholder
{% endembed %}

## Overview

A risk program that cannot communicate posture to leadership is not a risk program — it is a filing cabinet. In financial services, where the board risk committee, the Chief Risk Officer, and regulators all demand timely evidence of control effectiveness, the ability to produce accurate, data-driven dashboards is a compliance requirement, not a nice-to-have. ServiceNow IRM's Performance Analytics engine, combined with the platform's native reporting layer, gives you the infrastructure to move from quarterly PDF snapshots to live, role-differentiated risk visibility.

## Key concepts

* **Performance Analytics (PA)** — ServiceNow's built-in analytics framework that collects historical snapshots of record counts and field values on a schedule, enabling trend analysis over time. IRM ships with pre-built PA indicators for Risk, Control, and Issue data.
* **Indicators and Indicator Sources** — An Indicator defines *what* to measure (e.g., number of high-residual-risk items in the Risk Register); an Indicator Source defines *how* to query the data (table, filter, aggregate function). You can combine multiple indicators into a single score.
* **KRI Thresholds** — Each Key Risk Indicator carries green/yellow/red threshold bands. When a KRI score crosses a band, the platform changes the indicator's color state and can trigger automated responses (covered in the next page).
* **Dashboards** — Configurable canvas pages composed of widgets: scorecards, bar/line charts, heat maps, and data tables. ServiceNow supports role-based dashboard visibility so a branch operations manager sees operational risk; the CISO sees cyber risk; the board sees an aggregated enterprise view.
* **Reports** — Scheduled reports deliver PDF or CSV extracts to stakeholder inboxes. In IRM you can report on any table — Risk Register, Control Objectives, Audit Findings, Vendor Assessments — with the same filtering and grouping logic available in the list view.
* **CRI Profile (Cyber Risk Intelligence)** — For organizations that have licensed the Advanced Risk module, the CRI Profile widget displays the organization's cyber risk score derived from external threat feeds alongside internal control effectiveness, giving the board a single fused signal.

## Building a board-level risk dashboard in ServiceNow IRM

The following steps walk through creating a Risk Posture dashboard appropriate for a regional bank's quarterly board risk committee packet.

### 1. Define your Indicators

Navigate to **Performance Analytics > Indicators** and confirm the following baseline indicators exist (IRM ships with most of these out of the box):

| Indicator | Source table | Aggregate | Purpose |
|---|---|---|---|
| Open High Risks | sn\_risk\_risk | COUNT where residual rating = High | Track unacceptable residual risk |
| Controls Past Due | sn\_compliance\_control | COUNT where review\_date < today | Control staleness |
| KRI Threshold Breaches | sn\_risk\_indicator\_value | COUNT where color\_state = Red | Active KRI alerts |
| Open Audit Findings (Critical) | sn\_audit\_finding | COUNT where severity = Critical, state ≠ Closed | Audit exposure |
| Vendor Risk — Tier 1 Past Due | sn\_vendorrisk\_engagement | COUNT where tier = 1 and due\_date < today | Vendor assessment gaps |

For each indicator, set a **collection frequency** (daily is standard for operational risk; hourly is appropriate for cyber KRIs tied to SIEM feed data).

### 2. Configure KRI thresholds

Open the **Indicator** record and click the **Thresholds** tab. For the *Open High Risks* indicator, a typical regional bank might set:

* **Green:** 0–3 open high risks
* **Yellow:** 4–8
* **Red:** 9 or more

These thresholds should be calibrated against your Risk Appetite Statement. If your board has approved a risk appetite of "no more than five high-residual-risk items outstanding for more than 30 days," the yellow band should begin at five.

### 3. Build the dashboard

Go to **Dashboards > New** and name it *Board Risk Committee — Quarterly View*. Add the following widget types:

* **Scorecard widgets** for each KRI (shows current value + trend arrow vs. prior period)
* **Heat map widget** pointing to the Risk Register, grouped by Risk Category (Credit, Operational, Cyber, Regulatory) on one axis and Residual Rating on the other — this is the classic 5×5 risk heat map regulators recognize immediately
* **Bar chart** showing Open Issues by Assigned Group and Days Open — exposes remediation bottlenecks
* **Data table** listing the top 10 highest-residual risks with owner, target date, and current mitigation plan status

Set the dashboard **audience** to the *Board Risk Committee* role so it does not appear in the default employee view.

### 4. Schedule reports for regulatory submissions

Under **Reports > Scheduled Reports**, create a monthly export that emails a PDF of the dashboard to the CRO, CCO, and board secretary. For OCC or Federal Reserve exam preparation, add a quarterly export of the full Risk Register to CSV — examiners frequently request this in their opening information request.

{% hint style="warning" %}
Avoid attaching raw ServiceNow exports directly to board packets without a cover narrative. The heat map and scorecard widgets are self-explanatory; the raw CSV is for examiner requests only.
{% endhint %}

## In the video

* Navigating to Performance Analytics and reviewing the IRM indicator library.
* Configuring KRI thresholds against a sample Risk Appetite Statement.
* Building a board-level dashboard with heat map, KRI scorecards, and a top-risk data table.
* Scheduling a monthly PDF report for distribution to the board risk committee.
* Interpreting trend data — what a rising KRI count tells the CRO vs. what it tells the CISO.

## Key takeaways

* Performance Analytics turns the Risk Register from a point-in-time record into a live trending data source — essential for demonstrating control effectiveness over time to regulators.
* KRI threshold bands should be directly traceable to approved Risk Appetite Statements; if they are not, they are decorative.
* Role-based dashboards prevent information overload: the board sees aggregated posture; operations sees their own control gaps.
* The CRI Profile widget provides a fused internal/external cyber risk signal that board members and audit committees increasingly expect.
* Scheduled reports close the loop between the platform and the governance rhythm — board packets, RCSA submissions, and examiner information requests all draw from the same data source.

---

*IRM & Cyber Risk Framework — TechTalk with Bill*
