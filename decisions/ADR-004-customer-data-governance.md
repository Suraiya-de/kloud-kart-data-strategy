# ADR-004: Establish controlled customer-data access, retention and deletion processes

- **Status:** Proposed
- **Date:** 2026-11-13
- **Decision owner:** Kloud Kart executive sponsor

## Context

Kloud Kart has limited visibility into how customer information is copied, shared, and retained across the organisation. Marketing exports customer lists without tracking how many copies exist or where they are stored.

The company is also responding to a Data Protection Commission complaint involving a customer whose data was requested to be deleted. The case study brief identifies a 90-day period for responding to the complaint.

Without an inventory of customer-data copies and clear ownership of them, Kloud Kart may struggle to demonstrate how customer information is managed and whether deletion or other data requests have been handled consistently.

Adding more reporting systems without first addressing these weaknesses could increase the number of locations where customer information is stored.

## Decision

Kloud Kart should establish a documented customer-data governance process that identifies where customer data is stored or exported, assigns responsibility for access and retention, and provides a repeatable, auditable process for handling deletion requests and other customer-data obligations.

The process should cover relevant operational databases, reporting copies, and departmental exports, with retention exceptions and backup handling assessed appropriately.

## Alternatives considered

### Alternative A: Continue allowing departments to manage customer-data exports independently

- **How it would work:** Marketing and other departments would continue exporting and retaining customer lists according to their own practices.
- **Why it is attractive:** Requires little immediate organisational or technical change.
- **Why rejected:** Kloud Kart would continue to lack visibility and accountability over customer-data copies, making it difficult to manage access, retention, and deletion consistently.

### Alternative B: Establish a controlled customer-data inventory and lifecycle process

- **How it would work:** Identify customer-data locations and copies, assign owners, document access and retention rules, and introduce a process for recording and verifying customer-data requests and actions.
- **Why it is attractive:** Improves visibility, accountability, and the ability to demonstrate how customer data is managed.
- **Why selected:** It addresses the existing governance weakness before additional analytical systems and data copies are introduced.

### Alternative C: Defer governance improvements until a larger data platform is introduced

- **How it would work:** Continue current data practices and address governance during a future platform migration.
- **Why it is attractive:** Could allow governance controls to be designed alongside a broader technology change.
- **Why rejected:** The current complaint and uncontrolled customer-data exports are existing risks. Waiting for a future platform does not resolve them.

## Consequences

- **What this buys:** Better visibility of customer-data copies, clearer accountability, more consistent handling of customer requests, and stronger evidence of data-management practices.
- **What this costs:** Time to identify existing copies, assign data owners, document retention rules, review departmental practices, and maintain records of actions taken. Some existing processes may need to change.
- **What it costs the client if I am wrong:** If the inventory is incomplete or the process does not cover relevant exports and retained copies, Kloud Kart may believe a request has been fully addressed when some data remains unmanaged. This could create continuing compliance and reputational exposure.
- **What would make me revisit this:** Changes in applicable data-protection requirements, new customer-data uses, expansion into additional markets, new systems that create data copies, or evidence that the existing process cannot reliably manage customer requests.

## What this survives

- The current Data Protection Commission complaint.
- The need to manage customer information across operational and reporting environments.
- The existing practice of departmental customer-data exports.
- Future business growth, provided new systems and data copies are included in the governance process.