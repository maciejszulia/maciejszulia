# AgroCamping Reception: keeping daily operations consistent

**Context:** an internal application for a family campsite, connecting incoming reservations and enquiries with reception work and financial records.

**My role:** I coordinate development for my parents' family business, turning day-to-day needs into requirements, priorities, and acceptance criteria. I use AI coding tools for implementation and verification. My contribution is described as coordinated, AI-assisted delivery, without claiming sole manual authorship of the codebase.

**Stack:** TypeScript, Astro, Express, Prisma, SQLite, Python, shell tooling, GitLab CI.

## Engineering decisions behind the interface

### Incoming data must not undo staff decisions

A reservation can be imported more than once, while reception staff may already have assigned its pitch or changed its price. Import identity and replay rules preserve reception-owned data, keep cancellation and checkout states from regressing, and avoid timestamp changes when nothing meaningful changed. Invalid items have durable rejection records containing field/error codes rather than copied guest descriptions.

### A payment label is not enough evidence to settle a stay

The integration distinguishes booking status from financial evidence. It identifies payment movements across account, live/test mode, movement kind, and provider identity; checks receipt/refund/reversal relationships; and records supported ledger amounts in integer minor units. Conflicting evidence, incomplete chains, and closed accounting shifts require reconciliation rather than silently appearing settled.

### Deletion must survive the next synchronisation

Deleting an imported website enquiry queues an upstream erasure request in the same database transaction. The integration retries until acknowledgement and retains the enquiry's import identity so that an old feed cannot recreate it. This is a concrete privacy mechanism across system boundaries, not just a delete button.

### Access and recovery belong in the backend

User identity is checked against current database state. Endpoint authorization defaults to deny and distinguishes staff, finance, and owner resources. The delivery scripts use immutable releases, writer locks, database backups, and release-specific health checks, with explicit recovery after failed activation or migration.

## Privacy mechanisms and their limits

| Mechanism | What it does — and what it does not establish |
|---|---|
| Backend access control | Restricts operational actions; it does not anonymise stored data. |
| Enquiry deletion propagation | Requests erasure in the connected website and prevents stale-feed recreation; it does not purge every mailbox, backup, log, or processor copy. |
| Review follow-up consent | Requires the stored consent flag and explicit feature enablement; it does not prove the quality of the original consent notice or a complete withdrawal process. |
| Backup rotation | Removes older local backup files according to a configured age; this is not a comprehensive guest-data retention policy. |
| Reduced logging and rejection records | Avoids copying some sensitive content; identifiers and free-text business records can remain personal data. |

The retained identities are not presented as irreversible anonymisation. No legal certification or blanket GDPR-compliance claim is made. Rights to source code and third-party components are separate from privacy controls.

## What this project lets me discuss in an interview

- Turning a reception problem into an acceptance criterion that can be checked.
- Investigating why a repeated import changed an operational record.
- Distinguishing a failed integration from incomplete financial evidence.
- Reviewing a change through tests, migration checks, and release recovery scenarios.
- Explaining which privacy controls exist and where operational policy is still required.

**Review boundary:** this case study summarises the private development-source snapshot reviewed on 21 September 2026. It includes no guest records, production credentials, or claim of measured scale. Source access and a synthetic-data demonstration can be arranged separately. Test coverage is described by purpose; no unverified pass count or production uptime is claimed.
