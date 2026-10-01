# Maciej Szulia

Web applications · API integrations · command-line tools

[Website & booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md) · [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md) · [CLI & source](https://gitlab.com/maciejszulia/rogalddl-scraper)

[Polski](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/README.pl.md) · [Verification record](verification.md)

## AgroCamping website and booking API

A Polish, English and German website with a separate booking API and reception integration.

- Shared booking rules, transactional capacity checks and idempotency handle repeated requests.
- A persistent outbox tracks notification attempts separately from booking acceptance.
- Payment callbacks are verified; optional consent and guest-data retention have explicit boundaries.

Next.js · React · TypeScript · Node.js · MySQL/MariaDB · Stripe · GitLab CI

[Technical overview](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md) · [Public website](https://www.agrocamping.eu/)

## AgroCamping Reception

An internal application connecting reservations and guest enquiries with reception work and financial records.

- Repeated imports preserve pitch and price changes made by reception staff, plus cancellation and checkout states.
- Receipts, refunds and reversals are reconciled as financial evidence, separately from booking status.
- Backend permissions, enquiry-deletion propagation and release recovery address operational failure cases.

TypeScript · Astro · Express · Prisma · SQLite · Python · shell tooling · GitLab CI

[Technical overview](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md)

## Metadata catalogue CLI

A public Node.js tool that builds a local music catalogue and MPV playlist from indexed listings.

The catalogue records provenance and duplicate decisions. A writer lock and staged publication support recovery from interrupted writes. There are no npm dependencies; installation and offline tests are documented in the repository.

[Source, setup and tests](https://gitlab.com/maciejszulia/rogalddl-scraper)

## Evidence and scope

The [verification record](verification.md) includes **75 passing offline CLI tests** at the audited snapshot, selected API checks and synthetic reception startup. Each result identifies its source revision and scope.

Business-application source is private; public descriptions exclude guest records and production configuration. The CLI source is public. AI tools, including Claude Code and Codex, assist implementation and verification of the AgroCamping projects.

[Guest data, recovery and licensing](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/engineering-practices.md) documents the limits of access, retention, deletion and reuse. Test results do not certify production health, complete coverage or legal compliance.
