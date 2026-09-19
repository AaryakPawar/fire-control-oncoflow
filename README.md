<div align="center">

# OncoFlow

### Integrated Oncology Care Coordination & Workflow Platform

**CSYE 7230 · Team Fire Control**

A workflow-oriented web application for coordinating oncology care activities across patients, clinicians, laboratories, pharmacies, insurance personnel, and administrators.

</div>

---

## Overview

Cancer care requires coordination among multiple participants, including oncologists, nurses, diagnostic laboratories, pharmacies, insurance personnel, administrators, and patients.

Although these participants contribute to the same care journey, their activities may occur through separate workflows. This can make it difficult to determine:

- what has already been completed,
- what remains pending,
- which role currently owns the next action, and
- how the patient's overall care journey is progressing.

**OncoFlow** is a full-stack web application designed to address this coordination problem through secure, role-based workflows.

The application focuses on **workflow visibility, ownership, traceability, and cross-role coordination** rather than functioning as an Electronic Health Record or clinical decision-support system.

---

## Core Concept

OncoFlow is centered around two primary concepts.

### Unified Patient Care Timeline

Important events generated across clinical and administrative workflows are organized chronologically so authorized users can understand how a patient's care journey is progressing.

Examples include:

- treatment-plan updates,
- nursing observations,
- diagnostic requests and results,
- prescriptions and pharmacy updates,
- insurance-authorization decisions.

### Role-Based Work Queues

Actions performed by one role can create downstream work for another role.

For example:

```mermaid
flowchart LR
    A["Doctor creates diagnostic request"]
    --> B["Laboratory work queue"]

    B --> C["Lab technician processes request"]

    C --> D["Diagnostic result published"]

    D --> E["Patient care timeline updated"]

    E --> F["Doctor reviews result"]
```

This workflow model makes task ownership and cross-role handoffs visible throughout the system.

---

## Team

### Fire Control

| Team Member | NUID |
|---|---:|
| **Aaryak Pawar** | `002065641` |
| **Jamal Opeyemi Akinlabi** | `001647538` |

---

## Primary User Roles

| Role | Primary Responsibility |
|---|---|
| Patient | View permitted care progress, milestones, prescriptions, diagnostics, and authorization status |
| Doctor / Oncologist | Manage treatment plans, diagnostic requests, prescriptions, and clinical workflows |
| Nurse | Record care updates, observations, and treatment progress |
| Laboratory Technician | Process diagnostic requests and publish results |
| Pharmacist | Process prescriptions and manage fulfillment status |
| Insurance Officer | Review authorization requests and update authorization status |
| System Administrator | Manage users, permissions, audit activity, and operational information |

---

## Planned Functional Scope

The following capabilities define the **planned Part A project scope**. Application implementation will take place during later project phases.

### Identity & Access

- Secure user authentication
- Role-Based Access Control
- Server-side authorization
- User-account administration

### Patient Care

- Patient profiles
- Unified patient care timeline
- Treatment planning
- Nursing updates
- Care milestone tracking

### Diagnostic & Laboratory Workflow

- Diagnostic request creation
- Laboratory work queues
- Request-status tracking
- Diagnostic-result publication
- Clinical review handoff

### Prescription & Pharmacy Workflow

- Prescription creation
- Pharmacy work queues
- Fulfillment tracking
- Prescription-status visibility

### Insurance Authorization Workflow

- Authorization request submission
- Insurance review
- Approval, denial, or additional-information status
- Clinical and patient status visibility

### Workflow Coordination

- Role-specific work queues
- Cross-role handoffs
- Workflow notifications
- Operational dashboards
- Audit trail
- Administrative analytics

---

## Planned Technology Stack

The following technologies are planned for implementation. Application code, dependency versions, and deployment configuration have not yet been finalized.

| Layer | Planned Technology | Purpose |
|---|---|---|
| Frontend | React, TypeScript, Material UI | Role-specific user interfaces and dashboards |
| Backend | Node.js, Express, TypeScript | REST API and workflow business logic |
| Database | PostgreSQL | Relational application data storage |
| ORM | Prisma | Database access, schema management, and migrations |
| Authentication | JWT, bcrypt | Authentication and password security |
| Authorization | Role-Based Access Control | Server-side permission enforcement |
| Validation | Zod | API request and application-data validation |
| Visualization | Recharts | Operational and administrative dashboards |
| Unit / Integration Testing | Vitest or Jest, React Testing Library, Supertest | Automated application testing |
| End-to-End Testing | Playwright | Testing complete user workflows |
| Test Data | Faker | Synthetic users, patients, and workflow data |
| Containerization | Docker | Reproducible development environment |
| CI/CD | GitHub Actions | Automated testing and build validation |
| Frontend Deployment | Vercel | Planned frontend hosting |
| Backend Deployment | Render | Planned backend API hosting |
| Database Deployment | Managed PostgreSQL | Planned hosted database |

No critical application functionality will depend on real hospital, pharmacy, or insurance APIs.

---

## Planned Epics

The initial backlog is organized into eight Epics covering the complete planned OncoFlow prototype.

| # | Epic | GitHub Issue |
|---:|---|---|
| 1 | Authentication & Role-Based Access Control | [Issue #2](https://github.com/AaryakPawar/fire-control-oncoflow/issues/2) |
| 2 | Patient Profiles & Unified Care Timeline | [Issue #3](https://github.com/AaryakPawar/fire-control-oncoflow/issues/3) |
| 3 | Treatment Planning & Clinical Care | [Issue #4](https://github.com/AaryakPawar/fire-control-oncoflow/issues/4) |
| 4 | Diagnostic & Laboratory Workflow | [Issue #5](https://github.com/AaryakPawar/fire-control-oncoflow/issues/5) |
| 5 | Prescription & Pharmacy Workflow | [Issue #6](https://github.com/AaryakPawar/fire-control-oncoflow/issues/6) |
| 6 | Insurance Authorization Workflow | [Issue #7](https://github.com/AaryakPawar/fire-control-oncoflow/issues/7) |
| 7 | Work Queues, Cross-Role Handoffs & Notifications | [Issue #8](https://github.com/AaryakPawar/fire-control-oncoflow/issues/8) |
| 8 | Analytics, Audit Trail & Administration | [Issue #9](https://github.com/AaryakPawar/fire-control-oncoflow/issues/9) |

Each Epic contains its planned feature scope, user benefit, and high-level user stories.

---

## Data & Privacy Scope

OncoFlow will use **synthetic patient information only**.

The academic prototype will not:

- store real patient data,
- provide medical diagnoses,
- generate treatment recommendations,
- integrate with production hospital systems,
- process real insurance transactions,
- connect to real pharmacy systems, or
- claim production healthcare-regulatory compliance.

Security and privacy mechanisms are included to demonstrate responsible software-design practices within the scope of an academic prototype.

---

## Course Repository Setup

This repository was initialized using the Scrum repository template recommended for CSYE 7230.

The original template documentation is preserved at:

[`docs/SCRUM_WORKFLOW.md`](docs/SCRUM_WORKFLOW.md)

The repository also retains the course template's:

- Epic issue template,
- Story issue template,
- Bug issue template,
- Question issue template,
- Pull Request template,
- Epic workflow automation.

---

## Part A Status

**Current Phase: Part A — Project Proposal & Initial Backlog**

| Part A Deliverable | Status |
|---|---|
| Project concept finalized | Complete |
| Team repository created | Complete |
| Team access configured | Complete |
| Scrum repository template retained | Complete |
| Planned functional scope defined | Complete |
| Planned technology stack identified | Complete |
| Eight project Epics created | Complete |
| Part A proposal report | Complete |

Implementation of the application will begin in subsequent project phases.

---

## Repository

**GitHub:**
https://github.com/AaryakPawar/fire-control-oncoflow

---

<div align="center">

**OncoFlow**

Team Fire Control · CSYE 7230

</div>
