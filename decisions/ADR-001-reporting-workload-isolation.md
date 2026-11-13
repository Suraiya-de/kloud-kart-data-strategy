# ADR-001: Separate reporting workloads from the production database

- **Status:** Proposed
- **Date:** 2026-11-13
- **Decision owner:** Kloud Kart executive sponsor

## Context

Kloud Kart currently operates its website and business database using the same MySQL environment. The database contains approximately 40GB of data and supports around 4,000 orders per day.

Reporting exports are also executed against this environment. The case study brief confirms that Monday exports slowed the live website twice during the previous month.

This creates an operational risk because reporting activity competes with the database resources required to process customer transactions. Further growth of 15–20% annually and the Nigeria pilot could increase this pressure.

Kloud Kart has approved a second server or a read replica. However, the company has only one PHP/MySQL developer and can recruit only two data specialists during the financial year. The proposed solution must therefore reduce production risk without introducing unnecessary operational complexity.

## Decision

Kloud Kart should use the approved second server to host a MySQL read replica dedicated to reporting workloads, subject to technical validation of the existing database configuration and replication capacity.

Reporting queries and scheduled exports should run against the replica rather than the live production database. The production database must remain the authoritative system for customer transactions.

## Alternatives considered

### Alternative A: Continue running reporting queries against production

- **How it would work:** Continue generating Monday exports and other reports directly from the existing production database.
- **Why it is attractive:** Requires no additional infrastructure or initial migration effort.
- **Why rejected:** This preserves the existing resource contention that has already caused website slowdowns. It exposes customer transactions to unnecessary reporting workloads.

### Alternative B: Use the approved second server as a reporting replica

- **How it would work:** Replicate production data to the second server and direct reporting queries to that environment.
- **Why it is attractive:** Separates analytical workloads from customer transactions, uses infrastructure already approved by the board, and provides a manageable first step for a small team.
- **Why selected:** It addresses the immediate operational problem without requiring a complex new data platform.

### Alternative C: Introduce a separate cloud data warehouse immediately

- **How it would work:** Transfer business data into a separately managed analytical platform for reporting and future analytics.
- **Why it is attractive:** Could provide greater analytical flexibility as the business expands.
- **Why rejected:** It introduces additional cost, migration work, and operational responsibilities before Kloud Kart has established reliable reporting processes or a sufficiently experienced data team.

## Consequences

- **What this buys:** Reduced competition between reporting queries and customer transactions, improved production stability, and a controlled environment for reporting development.
- **What this costs:** Additional server resources, replication setup, monitoring, maintenance, and staff time to manage the reporting environment. Replication lag must be monitored because the replica may not contain the latest production changes.
- **What it costs the client if I am wrong:** If the replica cannot handle reporting workloads or becomes unreliable, reports may become delayed or inconsistent. If reporting workloads are allowed to fall back to production without control, the original website performance risk remains.
- **What would make me revisit this:** Sustained replication lag, insufficient replica capacity, continued production performance issues, significant growth beyond current assumptions, or evidence that a different reporting architecture is required.

## What this survives

- The expected 15–20% annual business growth described in the brief, subject to capacity testing.
- The current two-hire limit.
- The requirement to keep the live website and production database available.
- The need to introduce reporting improvements without immediately adopting a more complex analytical platform.