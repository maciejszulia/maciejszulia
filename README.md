# Maciej Szulia

AI and AI automation specialist · information systems builder · AI agents · web applications and APIs

[Website & booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md) · [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md) · [CLI & source](https://gitlab.com/maciejszulia/rogalddl-scraper)

[Polski](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/README.pl.md) · [Verification record](verification.md)

## How I build information systems

I design and deliver information systems (bookings, reception, financial records) with a team of AI agents that I plan for, direct and review:

- **Claude Code** (Anthropic): a coding agent in the terminal. It reads the repository, plans, writes and tests code, and runs subagents.
- **OMX, oh-my-codex**: orchestration on top of OpenAI's Codex CLI. Planning, teams of agents each working in its own git worktree, quality gates at the end.
- **OMC, oh-my-claudecode**: multi-agent orchestration for Claude Code, run as a separate instance.
- **Hermes Agent** (Nous Research): an autonomous agent with memory, scheduled jobs and a Kanban board. It runs my daily press digest.
- **oh-my-pi** (`omp`): a terminal coding agent with separate models for planning, quick edits and deep reasoning, across many providers.
- **OMH, oh-my-hermes**: skills and roles for Hermes, under evaluation for my move to Hermes.

I decide what gets built, accept every change on tests and own the release.

## Private projects

Many of my projects are private. I am happy to present them live, to a human. If you are a recruiter, please confirm in your first message that you are a person and not an AI agent, and we will arrange a screen-share walkthrough.

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

Business-application source is private; public descriptions exclude guest records and production configuration. The CLI source is public. The AI agents listed above assist implementation and verification of the AgroCamping projects.

[Guest data, recovery and licensing](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/engineering-practices.md) documents the limits of access, retention, deletion and reuse. Test results do not certify production health, complete coverage or legal compliance.

## About me

My favourite books: Wittgenstein's *Tractatus Logico-Philosophicus*, *Podstawy logiki i teorii mnogości* (foundations of logic and set theory) by Murawski and Świrydowicz, graph theory.
