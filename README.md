[README.md](https://github.com/user-attachments/files/30624418/README.md)
# Predictive Maintenance Dashboard — Aviation

Interactive analytics project that turns historical aircraft maintenance records into a predictive, decision-ready dashboard. Built to help maintenance control, reliability engineering, and operations teams move from reactive repairs to proactive, data-driven maintenance planning.

**Data Lead:** Steven E. Yandle Sr.

**Live demo:**(https://steven-yandle.github.io/Predictive-Maintenance-Dashboard/)*

---

## Overview

Aircraft maintenance teams often rely on static spreadsheets and manually compiled reports to track component and airframe performance — making it hard to spot early reliability trends or get a current, fleet-wide view of equipment health.

This project replaces that manual process with:

- A **Python / Pandas** pipeline that cleans, structures, and analyzes maintenance data
- A **statistical risk-scoring model** that flags aircraft and components showing early signs of degraded reliability
- An **interactive Power BI-style dashboard** that visualizes fleet KPIs, reliability trends, and predictive risk indicators

## Repository Contents

| File | Description |
|---|---|
| `Predictive_Maintenance_Dashboard.html` | Interactive dashboard prototype — open directly in any browser, no install required |
| `Aviation_Maintenance_Data.xlsx` | Data model (fact + dimension tables), ready to import into Power BI Desktop |
| `Aviation_Dashboard_PowerBI_Guide.md` | Step-by-step guide to rebuild the dashboard as a native `.pbix` Power BI report, including DAX measures |
| `Predictive_Maintenance_Dashboard_Case_Study.docx` | Case study write-up: business problem, approach, and results |

## Dashboard Features

- **KPI summary** — total events, downtime hours, repair cost, unscheduled-maintenance rate, and average predictive risk score
- **Monthly reliability trend** — event volume and unscheduled-maintenance rate over time
- **Events by component** — where discrepancies concentrate across engine, avionics, hydraulics, landing gear, and more
- **Fleet comparison** — events and downtime by fleet type
- **Predictive risk table** — tail-number-level risk scoring (High / Medium / Low tiers) over a trailing 90-day window, with click-to-drill-through into that aircraft's maintenance log
- **Interactive filters** — fleet type, tail number, component, and reporting period

## Tech Stack

- **Python & Pandas** — data cleaning, transformation, and workflow automation
- **Statistical analysis** — trend detection and predictive risk scoring
- **Power BI** — interactive dashboard design and data visualization
- **HTML / JavaScript / Chart.js** — standalone interactive prototype of the dashboard

## Getting Started

### View the prototype
Download `Predictive_Maintenance_Dashboard.html` and open it in any modern browser — it runs entirely client-side with the maintenance dataset embedded, so no server or install is required.

### Build the live Power BI report
1. Open Power BI Desktop.
2. Import `Aviation_Maintenance_Data.xlsx` (`Get Data → Excel Workbook`).
3. Follow `Aviation_Dashboard_PowerBI_Guide.md` for the data model relationships, DAX measures, and report page layout.

## Data Model

| Table | Type | Description |
|---|---|---|
| `Maintenance_Log` | Fact | One row per maintenance discrepancy/event (date, tail number, component, downtime, cost, risk score) |
| `Aircraft` | Dimension | One row per tail number (fleet type, base, entry into service) |
| `Components` | Dimension | One row per component code (name, system) |
| `Calendar` | Dimension | Date table for time-intelligence calculations |

> Note: the maintenance data included here is synthetic, generated to reflect realistic aviation reliability patterns for demonstration purposes.

## Results & Impact

- Replaced manual, spreadsheet-based reporting with an automated Python workflow
- Gave maintenance and operations stakeholders a single, always-current view of fleet health and KPIs
- Surfaced reliability trends supporting a shift toward proactive, predictive maintenance planning
- Made statistical, data-backed insight accessible to non-technical decision-makers through an intuitive dashboard
