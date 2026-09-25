# Project documentation

Technical overviews, privacy mechanisms and verification records for the
AgroCamping applications and a local metadata catalogue CLI.

[Wersja polska](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/README.pl.md)

## Projects

| Project | Scope | Stack |
| --- | --- | --- |
| [AgroCamping website and booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md) | Polish, English and German website; booking rules, payment callbacks, notification retries and guest-data controls. | Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI |
| [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md) | Reservation imports, financial records, access control and release recovery. Repeated imports preserve pitch and price changes made by reception staff. | TypeScript, Astro, Express, Prisma, SQLite, Python, shell tooling, GitLab CI |
| [Local metadata catalogue CLI](https://gitlab.com/maciejszulia/rogalddl-scraper) | Records why entries were kept, merged or rejected. The repository documents installation and input validation, with synthetic offline tests. | Node.js, no npm dependencies |

Public website: [agrocamping.eu](https://www.agrocamping.eu/).

## Supporting documentation

- [Guest data, recovery and licensing](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/engineering-practices.md): consent, retention, access permissions, deletion and rights restrictions, with their limits.
- [Verification record](verification.md): source snapshots, commands, test results and checks that were not run.

## Footer

The website and reception source repositories are private. Their public overviews
describe the implementation without publishing guest records or production
configuration. The CLI source is public and can be run locally.

Verification results refer to the recorded snapshots and selected checks. They do
not establish production health, complete test coverage or legal compliance.
AI coding tools, including Claude Code and Codex, are used for implementation and
verification of the AgroCamping projects.
