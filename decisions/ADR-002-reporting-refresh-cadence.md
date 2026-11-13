# ADR-002: Use daily scheduled refreshes for reporting while keeping operational inventory live

- **Status:** Proposed
- **Date:** 2026-11-13
- **Decision owner:** Kloud Kart executive sponsor

## Context

Kloud Kart wants improved reporting and visibility across its business. However, the case study brief establishes that stock counts are the only process requiring near-real-time freshness. Other reporting requirements can tolerate daily refreshes.

Introducing real-time processing across every business function would add cost and technical complexity without a demonstrated business requirement.

The company also has limited technical capacity, with one existing PHP/MySQL developer and approval for only two data hires.

## Decision

Kloud Kart should use scheduled daily data refreshes for its reporting environment. Operational inventory decisions must continue to use the live transactional system as their authoritative source rather than relying on potentially delayed reporting data.

## Alternatives considered

### Alternative A: Introduce real-time data processing across all business functions

- **How it would work:** Continuously transfer and process business data so that reports and dashboards update as transactions occur.
- **Why it is attractive:** Provides more immediate visibility into business activity and could support advanced analytical use cases.
- **Why rejected:** The brief does not establish a business need for real-time updates across all reporting areas. The additional infrastructure, monitoring, and maintenance would be difficult to justify with the current budget and team capacity.

### Alternative B: Use daily scheduled refreshes for reporting and retain live inventory operations

- **How it would work:** Refresh reporting data on a daily schedule while the production system continues to manage live orders and inventory.
- **Why it is attractive:** Meets the stated freshness requirements, reduces unnecessary processing complexity, and keeps operational stock information within the live transactional environment.
- **Why selected:** It provides an appropriate balance between business needs, cost, and the company's ability to maintain the solution.

### Alternative C: Refresh all business data daily, including operational inventory

- **How it would work:** Use the reporting environment as the source for inventory information, updating it once per day.
- **Why it is attractive:** Simplifies the refresh process by applying one schedule to all data.
- **Why rejected:** Daily refreshes could leave stock information outdated during the day, creating a risk of inaccurate stock availability and poor fulfilment decisions.

## Consequences

- **What this buys:** Lower processing complexity, predictable reporting schedules, and a refresh approach that matches the business requirements.
- **What this costs:** Reports will not reflect every transaction immediately. The business must understand the reporting cut-off time and the difference between operational data and reporting data.
- **What it costs the client if I am wrong:** If business users require more frequent reporting than anticipated, daily refreshes could delay decisions. If operational inventory is mistakenly taken from the reporting copy, stock information could become stale and affect customer orders.
- **What would make me revisit this:** A demonstrated requirement for more frequent reporting, material business losses caused by reporting delays, or a change in inventory operations that requires a different data architecture.

## What this survives

- The stated requirement for near-real-time inventory information.
- Daily reporting requirements across other business functions.
- The current budget and two-hire constraint.
- Future growth, provided the reporting refresh schedule continues to meet agreed business needs.