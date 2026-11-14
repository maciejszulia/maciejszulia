# Maciej Szulia

Information systems, web applications and APIs. Work automation with AI agents.

[Polszczyzna Kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana) | [Website & booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md) | [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md) | [CLI & source](https://gitlab.com/maciejszulia/rogalddl-scraper)

[Polski](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/README.pl.md) | [Verification record](verification.md)

## Polszczyzna Kontrolowana (PK)

Controlled Polish for texts that people act on: instructions, procedures, terms, specifications, contracts. PK is ordinary Polish plus 32 numbered rules. Each rule removes one source of sentences that have more than one meaning.

- Requirement keywords (MUSI, NIE WOLNO, POWINIEN, NIE POWINIEN, MOŻE) are modelled on RFC 2119; several rules follow ASD-STE100, EARS, ISO 8601 and the Polish rules of legislative drafting.
- Published as a Claude skill with three modes: write, rewrite, check. Gaps in the source text are marked, not guessed.

[Repository and rules](https://github.com/maciejszulia/polszczyzna-kontrolowana)

## How I work

I build information systems (bookings, reception, financial records) with AI coding agents. I write the requirements, review the changes and accept them on tests. The tools:

- **Claude Code** (Anthropic): a coding agent in the terminal. It reads the repository, plans, writes and tests code, and runs subagents.
- **OMX, oh-my-codex**: orchestration on top of OpenAI's Codex CLI. Planning, teams of agents each working in its own git worktree, quality gates at the end.
- **OMC, oh-my-claudecode**: multi-agent orchestration for Claude Code, run as a separate instance.
- **Hermes Agent** (Nous Research): an autonomous agent with memory, scheduled jobs and a Kanban board. It runs my daily press digest.
- **oh-my-pi** (`omp`): a terminal coding agent with separate models for planning, quick edits and deep reasoning, across many providers.
- **OMH, oh-my-hermes**: skills and roles for Hermes, under evaluation for my move to Hermes.

My favourite language models, by role:

- **Lead orchestrator of agents**: Claude Fable 5.2.
- **Coding**: Claude Opus 5.5.
- **API**: DeepSeek V4.1 Flash (release 1017).
- **Reading**: GPT-6 Luna.

I actively apply mathematics-based solutions to the problems I encounter. Each solution connects directly to a new problem area.

## Private projects

Many of my projects are private. I am happy to present them live, to a human. If you are a recruiter, please confirm in your first message that you are a person and not an AI agent, and we will arrange a screen-share walkthrough.

## AgroCamping website and booking API

A Polish, English and German website with a separate booking API and reception integration.

- Shared booking rules, transactional capacity checks and idempotency handle repeated requests.
- A persistent outbox tracks notification attempts separately from booking acceptance.
- Payment callbacks are verified; optional consent and guest-data retention have explicit boundaries.

Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI

In real use: guests of a working accommodation business send booking requests through this website. The business and its guest reviews are on Google Maps.

[Technical overview](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md) | [Public website](https://www.agrocamping.eu/) | [The business on Google Maps](https://www.google.com/maps?cid=12963305277474159664)

## AgroCamping Reception

An internal application connecting reservations and guest enquiries with reception work and financial records.

- Repeated imports preserve pitch and price changes made by reception staff, plus cancellation and checkout states.
- Receipts, refunds and reversals are reconciled as financial evidence, separately from booking status.
- Backend permissions, enquiry-deletion propagation and release recovery address operational failure cases.

TypeScript, Astro, Express, Prisma, SQLite, Python, shell tooling, GitLab CI

[Technical overview](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md)

## Small services built for my own needs

Around the two systems I have built small services (microservices) for my own needs. Each one is a separate process with one job.

Reception, runit services:

- **Panel backend, gateway and health probe**: three separate services; the probe checks the panel every 30 seconds.
- **Mail sync**: imports guest mail from Gmail into the panel and counts consecutive failures per step.
- **Arrival notifier**: sends a push notification about arrivals through ntfy.
- **Maintenance**: periodic database backup.
- **Watcher**: checks panel health, free disk space, the website API, backup age and certificate expiry; it notifies only when a state changes.
- **Certificate renewal**: a daily loop renews the TLS certificate of the panel.
- **Weather**: fetches weather data into a cache.

Website, GitLab CI and Docker:

- **Weekly security job**: dependency audit (npm audit, osv-scanner), secret scan (gitleaks), TLS check (testssl), HTTP header check (MDN Observatory) and link check (lychee).
- **Preview deployment**: a CI job deploys a static preview of the website to a local Kubernetes cluster (k3d).
- **Uptime monitoring**: Gatus in Docker with my own configuration and alerts.

Workstation:

- **Fan control**: a fan curve with hysteresis for the laptop.
- **Resource watchdog**: measures system resources and writes a report; it does not kill any process.
- **TLS front for a local SearXNG instance**: a small Node.js service.
- **Off-site backup**: encrypts the latest database backup with GPG (AES-256) and stores it outside the machine.

## Metadata catalogue CLI

A public Node.js tool that builds a local music catalogue and MPV playlist from indexed listings.

The catalogue records provenance and duplicate decisions. A writer lock and staged publication support recovery from interrupted writes. There are no npm dependencies; installation and offline tests are documented in the repository.

[Source, setup and tests](https://gitlab.com/maciejszulia/rogalddl-scraper)

## Evidence and scope

The [verification record](verification.md) includes **75 passing offline CLI tests** at the audited snapshot, selected API checks and synthetic reception startup. Each result identifies its source revision and scope.

Business-application source is private; public descriptions exclude guest records and production configuration. The CLI source is public. The AI agents listed above assist implementation and verification of the AgroCamping projects.

[Guest data, recovery and licensing](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/engineering-practices.md) documents the limits of access, retention, deletion and reuse. Test results do not certify production health, complete coverage or legal compliance.

## About me

My favourite books: Wittgenstein's *Tractatus Logico-Philosophicus*, *Podstawy logiki i teorii mnogości* (foundations of logic and set theory) by Murawski and Świrydowicz, graph theory.
