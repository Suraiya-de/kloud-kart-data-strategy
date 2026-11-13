# ADR-003: Establish one governed source for business reporting

- **Status:** Proposed
- **Date:** 2026-11-13
- **Decision owner:** Kloud Kart executive sponsor

## Context

Kloud Kart currently lacks a consistent and trusted reporting process. Nana Adjei, Head of Operations, manually rebuilds Monday reporting figures from CSV exports, while Finance maintains a separate spreadsheet that does not produce matching results.

Marketing also exports customer lists without consistently tracking the copies created.

These practices create uncertainty about which figures should be used for business decisions. They increase manual effort and make it difficult for management to produce reliable board reports.

Separating reporting workloads from production will address the performance problem, but it will not automatically resolve inconsistent definitions, transformations, or reporting practices.

## Decision

Kloud Kart should establish a controlled reporting layer containing validated business data and agreed metric definitions. Finance and Operations should use this shared reporting source for management reporting instead of independently rebuilding figures from separate spreadsheets.

## Alternatives considered

### Alternative A: Allow each department to maintain its own reporting spreadsheets

- **How it would work:** Finance, Operations, and other departments would continue exporting data and calculating their own business figures.
- **Why it is attractive:** Requires little initial technical investment and allows departments to retain familiar processes.
- **Why rejected:** It preserves inconsistent calculations, duplicated effort, and disagreement over business figures. It does not establish a reliable basis for board reporting.

### Alternative B: Establish a governed reporting layer with shared metric definitions

- **How it would work:** Extract data into the reporting environment, apply documented cleaning and validation rules, and create business-ready reporting tables. Finance and Operations would agree on definitions for key metrics such as orders, sales, and revenue.
- **Why it is attractive:** Creates consistency, makes reporting processes repeatable, and provides a common basis for management decisions.
- **Why selected:** It directly addresses the reporting trust problem while building on the proposed reporting environment.

## Consequences

- **What this buys:** More consistent business figures, reduced spreadsheet reconciliation, repeatable reporting, and a clearer basis for board decisions.
- **What this costs:** Initial effort to agree on definitions, document transformation rules, validate historical figures, and maintain reporting tables. Departments may need to change familiar spreadsheet practices.
- **What it costs the client if I am wrong:** If the agreed definitions or transformations are incorrect, management could rely on consistently produced but misleading figures. The reporting layer must therefore be reconciled against source records and reviewed by the relevant business owners.
- **What would make me revisit this:** Persistent unexplained differences between source records and reports, changes in business definitions, expansion into new markets requiring additional reporting measures, or evidence that the reporting layer no longer meets business needs.

## What this survives

- Different reporting needs across Finance and Operations.
- The need to produce repeatable board reports.
- Growth in order volumes and business activity.
- The current requirement to reduce manual spreadsheet reconciliation without introducing an unnecessarily complex platform.