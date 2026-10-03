# Digital Loan Origination System — Business Analyst Portfolio Project

**NovaTrust Bank | End-to-End Business Analysis Case Study**
Prepared by **Harshada Kardile** — Business Analyst

---

## Overview

NovaTrust Bank, a mid-size retail bank, runs its personal-loan origination process largely manually: paper/PDF intake, duplicate data entry across two systems, sequential KYC/AML and credit checks, and physical sign-offs. This results in a **9.2-day average turnaround time** against an industry-competitive target of **3 days**, and a **22% applicant drop-off rate**.

This repository documents the full business analysis lifecycle for redesigning that process — from stakeholder elicitation through to a working SQL + Power BI performance dashboard — covering requirement elicitation, process mapping, requirements authoring, Agile delivery, quality assurance, and data analysis.

Start with [`00_Project_Case_Study_Summary.docx`](./00_Project_Case_Study_Summary.docx) for a two-page overview of the whole project before diving into individual artifacts.

---

## Repository Structure

| # | File | Phase | Description |
|---|---|---|---|
| 00 | `Project_Case_Study_Summary.docx` | Summary | One-stop overview: problem, approach, results, skills demonstrated |
| 01 | `Business_Case_Stakeholders_Elicitation.docx` | 1. Discovery | Business case, stakeholder register (Power/Interest grid), elicitation summary |
| 02 | `AS-IS_Process.docx` | 2. AS-IS Analysis | Current-state process narrative |
| 03 | `SIPOC_Gap_RootCause_Analysis.docx` | 2. AS-IS Analysis | SIPOC analysis, 6-item gap analysis, root cause analysis |
| 04 | `AS-IS_BPMN_Diagram.drawio` | 2. AS-IS Analysis | AS-IS BPMN swimlane diagram (open in [draw.io](https://app.diagrams.net)) |
| 05 | `TO-BE_Process.docx` | 3. TO-BE Design | Future-state process redesign, mapped to each AS-IS gap |
| 06 | `BRD.docx` | 3. TO-BE Design | Business Requirements Document — BR-01 to BR-14, BRL-01 to BRL-15 |
| 07 | `FRD.docx` | 3. TO-BE Design | Functional Requirements Document — FR-001 to FR-099 |
| 08 | `RTM_TestCases_UAT.xlsx` | 5. Quality & UAT | Requirements Traceability Matrix, 33 test cases, defect log, UAT sign-off |
| 09 | `loan_applications_dataset.csv` | 6. Data & Reporting | 420-record loan application dataset |
| 10–14 | `SQL_*.sql` | 6. Data & Reporting | Data import, KPI, SLA, operational, and final BA SQL queries |
| 15 | `PowerBI_Dashboard.pbix` | 6. Data & Reporting | Power BI dashboard — 6 KPI cards, 5 visuals, 3 slicers |

> Phase 4 (Agile delivery) lives in Jira, not this repo — see [Jira Board](#) *(replace with your board link if you make it public, or remove this line)*.

---

## Key Findings

- **Requirements traceability gap identified:** while building the RTM, found that BR-11 (loan disbursement) had no corresponding functional requirement anywhere in the 99-item FRD — logged as a defect and tracked through to UAT sign-off rather than ignored.
- **Data reconciliation check:** validated `tat_days` against `DATEDIFF(decision_date, submission_date)` in SQL, identifying and correctly explaining an expected ~0.44-day rounding variance as a source-data artifact, not a defect.
- **Cross-tool consistency:** every KPI on the Power BI dashboard was independently verified against SQL output before being treated as final.

## Results Snapshot

| Metric | AS-IS Baseline | Dataset / Dashboard Result |
|---|---|---|
| Average Turnaround Time (TAT) | 9.2 days | 8.86 days |
| Applicant Drop-off Rate | 22% | 24.5% |
| Approval Rate (of decided applications) | Not previously measured | 65.3% |
| SLA Breach Rate (3-day target) | Target not met (by definition) | 97.2% — confirms the case for the TO-BE redesign |

## Skills Demonstrated

Requirement Elicitation · Stakeholder Management · Gap Analysis · Root Cause Analysis · BRD/FRD Authoring · User Stories & Acceptance Criteria · BPMN · AS-IS/TO-BE Mapping · SIPOC · Process Improvement · Agile/Scrum · Backlog & Sprint Planning (Jira) · UAT · Test Scenarios & Test Cases · Defect Management · Requirements Traceability Matrix (RTM) · SQL (joins, CTEs, window functions, aggregation) · Power BI · Advanced Excel

---

## Contact

**Harshada Kardile**
*(add your email / LinkedIn link here)*
