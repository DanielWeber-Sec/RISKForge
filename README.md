<div align="center">

```text
                              ██████╗ ██╗███████╗██╗  ██╗███████╗ ██████╗ ██████╗  ██████╗ ███████╗
                              ██╔══██╗██║██╔════╝██║ ██╔╝██╔════╝██╔═══██╗██╔══██╗██╔════╝ ██╔════╝
                          ██████╔╝██║███████╗█████╔╝ █████╗  ██║   ██║██████╔╝██║  ███╗█████╗
                          ██╔══██╗██║╚════██║██╔═██╗ ██╔══╝  ██║   ██║██╔══██╗██║   ██║██╔══╝
                              ██║  ██║██║███████║██║  ██╗██║     ╚██████╔╝██║  ██║╚██████╔╝███████╗
                              ╚═╝  ╚═╝╚═╝╚══════╝╚═╝  ╚═╝╚═╝      ╚═════╝ ╚═╝  ╚═╝ ╚═════╝ ╚══════╝
```

# RISKForge

### Lightweight GRC & ISMS Management Platform

> Practical governance, risk, compliance, audit, and evidence management in one focused workspace.

<br>

![Project Status](https://img.shields.io/badge/status-early%20development-blue?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-UI-FF4B4B?style=flat-square\&logo=streamlit\&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-database-003B57?style=flat-square\&logo=sqlite\&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-dashboards-3F4F75?style=flat-square\&logo=plotly\&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-testing-0A9EDC?style=flat-square\&logo=pytest\&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Portfolio Project](https://img.shields.io/badge/type-portfolio%20project-6f42c1?style=flat-square)

<br>

> Best viewed in GitHub Dark Mode.

</div>

---

## 01 – Project Overview

**RISKForge** is a lightweight web-based GRC and ISMS management platform for managing:

* information-security risks
* security controls
* treatment actions
* audit findings
* corrective actions
* compliance evidence
* management-level reporting

The project translates governance and information-security requirements into a structured, traceable, and usable software workflow.

RISKForge is being developed as a practical portfolio project to demonstrate the connection between:

```text
Governance
   ↓
Requirements
   ↓
Risks
   ↓
Controls
   ↓
Actions
   ↓
Evidence
   ↓
Management Reporting
```

The objective is not to recreate a large enterprise platform such as ServiceNow GRC, Archer, or OneTrust.

The objective is to build a focused, understandable, and working MVP that demonstrates how GRC and ISMS processes can be operationalized.

---

## 02 – Core Problem

Many organizations still manage information-security governance using disconnected tools and documents:

* spreadsheet-based risk registers
* separate audit finding lists
* Word-based policies
* SharePoint folders
* email-based task tracking
* manually collected evidence
* inconsistent ownership and review dates

This often results in:

* incomplete risk visibility
* overdue treatment actions
* missing or expired evidence
* inconsistent control assessments
* poor audit readiness
* limited management reporting
* unclear accountability

RISKForge aims to provide one focused workspace for these processes.

---

## 03 – Core Workflow

```text
Risk identified
      ↓
Risk assessed
      ↓
Controls assigned
      ↓
Treatment actions created
      ↓
Evidence recorded
      ↓
Risk reviewed
      ↓
Risk accepted, reduced, avoided, or transferred
```

The application is designed around traceability between risks, controls, actions, findings, and evidence.

---

## 04 – Planned MVP Features

### Risk Register

* create and update information-security risks
* assign risk owners
* document assets, threats, and vulnerabilities
* assess likelihood and impact
* calculate inherent and residual risk
* define treatment decisions
* track review dates
* filter and export risk data

### Risk Dashboard

* total number of risks
* critical and high risks
* risks by status
* risks by owner
* risk heatmap
* overdue reviews
* top-risk overview
* management-level key risk indicators

### Control Library

* define security controls
* assign control owners
* track implementation status
* assess control effectiveness
* link controls to risks
* reference relevant frameworks
* track control review dates

### Treatment Actions

* create remediation and treatment actions
* assign responsible owners
* define due dates and priorities
* track implementation progress
* identify overdue actions
* document completion notes

### Audit Findings

* document findings, observations, and nonconformities
* assign severity and ownership
* link findings to controls
* create corrective actions
* track remediation
* verify and close findings

### Evidence Management

* register evidence for security controls
* assign evidence owners
* define evidence types
* track validity and review dates
* identify missing or expired evidence
* support audit-readiness reporting

---

## 05 – Risk Scoring Model

The MVP uses a simple five-by-five risk matrix.

```text
Risk Score = Likelihood × Impact
```

| Score | Rating   |
| ----: | -------- |
|   1–4 | Low      |
|   5–9 | Medium   |
| 10–15 | High     |
| 16–25 | Critical |

This model is intentionally simple for the first version.

Future versions may support:

* configurable risk methodologies
* weighted scoring models
* custom thresholds
* qualitative and quantitative assessments
* business-impact categories

---

## 06 – Example Risk Scenario

```text
Risk:
Unauthorized access to sensitive customer data

Asset:
Customer database

Threat:
Compromised privileged account

Vulnerability:
Privileged accounts are not reviewed regularly

Likelihood:
4

Impact:
5

Inherent Risk:
20 – Critical

Treatment Decision:
Mitigate

Assigned Control:
Quarterly privileged-access review

Treatment Action:
Implement an automated access-review process

Required Evidence:
Completed access-review report
```

RISKForge will connect this risk to its controls, treatment actions, audit findings, responsible owners, review dates, and supporting evidence.

---

## 07 – Technology Stack

The first version of RISKForge is planned as a Python-based browser application.

| Layer             | Technology     |
| ----------------- | -------------- |
| Application Logic | Python         |
| User Interface    | Streamlit      |
| Database          | SQLite         |
| Data Models       | Pydantic       |
| Dashboards        | Plotly         |
| Testing           | Pytest         |
| Version Control   | Git and GitHub |

The business logic will remain separated from the user interface.

This allows the application to evolve later without rewriting the core risk and control logic.

---

## 08 – Planned Architecture

```text
┌──────────────────────────────┐
│       Streamlit UI           │
│ Dashboard, forms, tables     │
└──────────────┬───────────────┘
               │
┌──────────────▼───────────────┐
│       Service Layer          │
│ Risk, control, action logic  │
└──────────────┬───────────────┘
               │
┌──────────────▼───────────────┐
│       Domain Models          │
│ Pydantic models and rules    │
└──────────────┬───────────────┘
               │
┌──────────────▼───────────────┐
│       Repository Layer       │
│ Database access and queries  │
└──────────────┬───────────────┘
               │
┌──────────────▼───────────────┐
│          SQLite              │
│ Risks, controls, evidence    │
└──────────────────────────────┘
```

---

## 09 – Planned Project Structure

```text
RISKForge/
├── app.py
├── pages/
│   ├── 1_Dashboard.py
│   ├── 2_Risk_Register.py
│   ├── 3_Controls.py
│   ├── 4_Actions.py
│   └── 5_Audit_Findings.py
├── riskforge/
│   ├── models/
│   ├── services/
│   ├── database/
│   ├── repositories/
│   └── scoring/
├── tests/
├── data/
├── assets/
├── requirements.txt
└── README.md
```

---

## 10 – Development Roadmap

### Phase 1 – Risk Register

* define the risk data model
* create and edit risks
* calculate risk scores
* assign owners
* track treatment decisions
* filter risks
* export risk data

### Phase 2 – Dashboard

* risk KPI cards
* risk heatmap
* severity distribution
* status distribution
* critical-risk overview
* overdue reviews

### Phase 3 – Controls and Actions

* control library
* risk-to-control mapping
* control effectiveness
* treatment-action tracking
* overdue-action reporting

### Phase 4 – Findings and Evidence

* audit findings
* corrective actions
* evidence metadata
* evidence validity tracking
* audit-readiness indicators

### Phase 5 – Portfolio Release

* realistic demonstration data
* architecture documentation
* security considerations
* screenshots
* hosted demo
* project walkthrough
* final case study

---

## 11 – Planned Case Study

RISKForge will use a fictional organization to demonstrate a realistic ISMS and GRC implementation scenario.

The case study will include:

* organization context
* ISMS scope
* business assets
* risk assessment
* control selection
* treatment planning
* audit findings
* evidence tracking
* management reporting

This approach ensures that the project demonstrates more than basic CRUD functionality.

It will show a connected and realistic governance workflow.

---

## 12 – Future Roadmap

The following features are outside the initial MVP:

* role-based access control
* user authentication
* multi-tenant organizations
* PostgreSQL support
* configurable risk methodologies
* ISO 27001 implementation tracking
* NIS2 and DORA modules
* supplier-risk management
* policy lifecycle management
* file uploads
* document storage
* audit trails
* API integrations
* Microsoft Entra ID integration
* automated cloud-security assessments
* AI-assisted risk and control suggestions

These features are roadmap items and are intentionally excluded from the initial implementation scope.

---

## 13 – Security Considerations

RISKForge will follow basic secure-development principles, including:

* input validation
* separation of application layers
* parameterized database queries
* dependency management
* secure configuration handling
* test coverage for risk calculations
* no hardcoded credentials
* no copyrighted framework texts
* no production data in the demo environment

A dedicated threat model and security review will be added during development.

---

## 14 – Compliance Notice

RISKForge is a portfolio and demonstration project.

It does not provide:

* certification
* legal advice
* regulatory assurance
* automatic compliance
* official ISO 27001 implementation approval
* official NIS2 or DORA assessment

Framework references are used for educational and demonstration purposes.

Full copyrighted standard texts are not included.

---

## 15 – Why This Project Exists

RISKForge combines experience and interests in:

* information-security governance
* ISMS and GRC
* risk management
* requirements engineering
* project management
* audit and compliance workflows
* software design
* automation
* management reporting

The project demonstrates how governance requirements can be translated into:

```text
Structured requirements
        ↓
Clear data models
        ↓
Traceable workflows
        ↓
Working software
        ↓
Management information
```

---

## 16 – Project Status

```text
Current Status: Early Development
Current Phase:  Project Foundation
Next Milestone: Functional Risk Register
```

The repository will be updated continuously as the MVP is implemented.

---

## 17 – Related Portfolio

This project complements the following GRC and ISMS portfolio:

**GRC Security Portfolio**

https://github.com/DanielWeber-Sec/grc-security-portfolio

The portfolio demonstrates the governance, risk, audit, and ISMS concepts behind the application.

RISKForge demonstrates how these concepts can be translated into working software.

---

## 18 – Author

**Daniel Weber**

Information Security Governance | GRC | ISMS | Risk Management

* GitHub: https://github.com/DanielWeber-Sec
* LinkedIn: https://www.linkedin.com/in/daniel-weber-594a81156

---

## 19 – License

This project is licensed under the MIT License.

See the `LICENSE` file for details.
