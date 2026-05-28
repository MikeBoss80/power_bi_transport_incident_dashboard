<div align="center">

<img src="https://img.shields.io/badge/-%F0%9F%9A%A6%20LONDON%20TRANSPORT%20INCIDENT%20DASHBOARD-0A0A0A?style=for-the-badge&labelColor=0A0A0A" height="42"/>

<br/>
<br/>

*Turning four years of transport incident records into prevention intelligence*

<br/>

[![Power BI](https://img.shields.io/badge/Power%20BI-Interactive%20Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=000000)](dashboard/Accidents_Project.pbix)
[![Domain](https://img.shields.io/badge/Domain-Transport%20Safety-C0392B?style=flat-square)](documentation/data_dictionary.md)
[![City](https://img.shields.io/badge/City-London%2C%20UK-003087?style=flat-square)](https://tfl.gov.uk)
[![Period](https://img.shields.io/badge/Period-2015–2018-2ECC71?style=flat-square)](#)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)](#)

<br/>

<img src="Assets/report.jpg" alt="Dashboard preview" width="900" style="border-radius:6px; box-shadow: 0 8px 32px rgba(0,0,0,0.3);"/>

</div>

---

## The Problem

Every incident in London's public transport network is more than a statistic — it affects commuters, disrupts operations, and strains emergency services. Yet without clear visibility into *where, when, and how* incidents cluster, prevention resources remain scattered.

> **Core question: Can we turn raw incident logs into a prioritized, evidence-based prevention map?**

This project does exactly that — cleaning four years of TfL-adjacent incident records and transforming them into an interactive Power BI dashboard that surfaces patterns invisible in spreadsheets.

---

## Dashboard Pages

| Page | What It Answers |
|------|----------------|
| **Overview** | Total volume, trend direction, headline KPIs |
| **Time Trends** | Seasonality, week-over-week shifts, peak risk windows |
| **Borough Risk Map** | Which boroughs concentrate the most incidents |
| **Incident Types** | Frequency breakdown by event category |
| **Victim Profile** | Demographics by sex, age group, and vulnerability |
| **Injury Outcomes** | Severity distribution by operator and context |

---

## Visual Preview

<table>
  <tr>
    <td align="center" width="50%">
      <img src="Assets/overview.jpg" alt="Overview page" width="100%"/>
      <br/><sub><b>Overview — headline metrics and trend direction</b></sub>
    </td>
    <td align="center" width="50%">
      <img src="Assets/report.jpg" alt="Main report page" width="100%"/>
      <br/><sub><b>Main Report — cross-filtered incident analysis</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="Assets/victims_profile.jpg" alt="Victim profile page" width="100%"/>
      <br/><sub><b>Victim Profile — demographics and at-risk groups</b></sub>
    </td>
    <td align="center" width="50%">
      <i>Add next screenshot to <code>Assets/</code> and update this cell</i>
    </td>
  </tr>
</table>

---

## Key Findings (Analytical Scope)

- **Borough concentration** — identifies the top boroughs by raw volume and rate, enabling targeted enforcement
- **Temporal patterns** — surfaces peak hours, days, and months where incidents spike
- **Event-type breakdown** — ranks incident categories to guide operator training priorities
- **Demographic exposure** — maps which age/sex groups are disproportionately affected
- **Outcome severity** — connects injury seriousness to operator, mode, and location context

---

## Data Pipeline

```
Raw incident records (Excel)
        │
        ▼
  Cleaning & standardisation
  (nulls, type casting, deduplication)
        │
        ▼
  Power BI data model
  (relationships, calculated columns, measures)
        │
        ▼
  Interactive dashboard (6 pages)
```

Dataset fields, transformations, and measure logic are documented in [`documentation/data_dictionary.md`](documentation/data_dictionary.md).

---

## Repository Structure

```
power_bi_transport_incident_dashboard/
│
├── README.md                        ← You are here
│
├── Assets/
│   ├── overview.jpg
│   ├── report.jpg
│   └── victims_profile.jpg
│
├── dashboard/
│   └── Accidents_Project.pbix       ← Main Power BI file
│
├── dataset/
│   └── london_transport_data.xlsx   ← Source data
│
└── documentation/
    └── data_dictionary.md           ← Field definitions & logic
```

---

## How to Open

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
2. Clone or download this repository.
3. Open `dashboard/Accidents_Project.pbix`.
4. All data is embedded — no external connections required.

---

## Tech Stack

| Tool | Role |
|------|------|
| **Power BI Desktop** | Data modelling, DAX measures, dashboard authoring |
| **Power Query (M)** | Data cleaning and transformation |
| **Excel** | Source dataset |

---

<div align="center">

*Built to demonstrate that good analysis asks the right question first — then lets the data answer it.*

</div>