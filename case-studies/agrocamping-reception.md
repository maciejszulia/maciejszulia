# AgroCamping Reception

AgroCamping Reception is an internal application for a family campsite. It connects incoming reservations and enquiries with reception work and financial records.

I coordinate development for my parents' campsite. My role is to turn day-to-day needs into requirements, set priorities and define acceptance criteria. I use AI coding tools for implementation and verification.

The stack is TypeScript, Astro, Express, Prisma, SQLite, Python, shell tooling, and GitLab CI.

## Repeated imports

A reservation may arrive again after reception staff have assigned its pitch or changed its price. Import identities and replay rules preserve those staff changes. They also prevent cancellation and checkout states from regressing, and leave timestamps unchanged when there is no meaningful update. Rejection records persist field and error codes without copying guest descriptions.

## Payment evidence

The integration treats booking status and financial evidence separately. It identifies payment movements by account, live/test mode, movement kind, and provider identity, then checks the relationships between receipts, refunds, and reversals. Supported ledger amounts are recorded in integer minor currency units. Conflicting evidence, incomplete chains, and closed accounting shifts require reconciliation.

## Deletion across systems

Deleting an imported website enquiry queues an erasure request for the website in the same database transaction. The integration retries until it receives acknowledgement. It keeps the enquiry's import identity so that an old feed cannot recreate the deleted enquiry.

## Access and release recovery

The backend checks user identity against the current database state. Endpoint authorization defaults to deny, with separate access for staff, finance, and owner resources. Delivery scripts use immutable releases, writer locks, database backups, and health checks for the selected release. They include recovery procedures for failed activation or migration.

## Privacy mechanisms and their limits

| Mechanism | Scope | Limit |
|---|---|---|
| Backend access control | Restricts operational actions. | Does not anonymise stored data. |
| Enquiry deletion propagation | Requests erasure in the website and prevents an old feed from recreating the enquiry. | Does not purge every mailbox, backup, log, or processor copy. |
| Review follow-up consent | Requires a stored consent flag and explicit feature enablement. | The mechanism alone does not establish notice quality or a complete withdrawal process. |
| Backup rotation | Removes older local backup files according to a configured age. | Covers backup age, not a comprehensive guest-data retention policy. |
| Reduced logging and rejection records | Avoids copying some sensitive content. | Identifiers and free-text business records can remain personal data. |

Retaining an import identity does not establish irreversible anonymisation. This case study makes no claim of legal certification or GDPR compliance. Rights to the source code and third-party components are separate from privacy controls.

## Interview topics

In an interview, I can discuss how a reception problem becomes a checkable acceptance criterion and how to investigate a record changed by a repeated import. Other topics include distinguishing integration failures from incomplete payment evidence, and reviewing changes through tests, migration checks, and release recovery scenarios. The privacy controls also provide examples of where operational policy is still required.

## Review scope

This case study covers the private development-source snapshot reviewed on 21 September 2026. Guest records and production credentials are excluded. The description explains what the tests cover; it makes no claims about measured scale, unverified pass counts, or production uptime. Source access and a demonstration using synthetic data can be arranged separately.
