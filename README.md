# Kloud Kart Data Strategy Engagement

## Overview

This repository contains the deliverables for the DE01 Architecture Case Study involving Kloud Kart, a Ghana-based e-commerce company seeking a practical and defensible data strategy following a recent funding round.

The objective is to identify the company's significant operational, reporting, governance, and compliance risks, recommend a realistic data architecture and operating model, and present a phased implementation roadmap that fits Kloud Kart's size, team capability, and budget constraints.

## Deliverables and Progress

| Deliverable | Status |
|---|---|
| Situation Diagnosis | Completed |
| Architecture Recommendation | Completed |
| 12-Month Implementation Roadmap | Completed |
| Architecture Decision Records (ADRs) | Prepared — pending review |
| Board Presentation | Pending |
| Improvement Beyond the Brief | Pending |

## Repository Structure

```text
Kloud-Kart-Data-Strategy/
│
├── diagnosis/
│   └── situation-diagnosis.md
│
├── recommendation/
│   ├── recommendation.md
│   └── roadmap.md
│
├── decisions/
│   ├── ADR-001-reporting-workload-isolation.md
│   ├── ADR-002-reporting-refresh-cadence.md
│   ├── ADR-003-governed-reporting-source.md
│   └── ADR-004-customer-data-governance.md
│
├── presentation/
│
├── appendix/
│
└── README.md
```

## Current Status

**Work in Progress**

The situation diagnosis, architecture recommendation, and 12-month implementation roadmap have been prepared.

Four Architecture Decision Records have also been drafted to document the key decisions supporting the proposed strategy, the alternatives considered, and the expected consequences.

These decisions remain proposed pending review and approval by the appropriate Kloud Kart decision-makers.

## Strategic Direction

The proposed strategy prioritises:

- Separating reporting workloads from the live production environment.
- Establishing a trusted and consistent source for business reporting.
- Reducing manual reporting and spreadsheet reconciliation.
- Improving customer-data visibility, access control, retention, and deletion processes.
- Using daily scheduled refreshes for ordinary reporting while keeping operational inventory live.
- Building a foundation for future business growth without introducing unnecessary technology or operational complexity.

## Current Focus

Reviewing and refining the Architecture Decision Records to ensure that each decision is supported by the situation diagnosis, executive recommendation, and implementation roadmap.

The next stages are the board presentation and the development of an improvement beyond the original brief.