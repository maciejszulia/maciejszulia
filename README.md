# Maciej Szulia

Data engeneering, metaprogramming tools, work automation & AI agents.

Mid-level Full-Stack Developer & AI Engineer. Information systems, web applications & APIs; 

Small-scale farmer & agritourism host


[Polski](README.pl.md)

## Private systems in real use

**AgroCamping website and booking API.** A website in Polish, English and German with a separate booking API and reception integration. Shared booking rules, transactional capacity checks and idempotency handle repeated requests. A persistent outbox tracks notification attempts separately from booking acceptance. Payment callbacks are verified. Guests of a working accommodation business send booking requests through this website.

Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI

[Technical overview](case-studies/agrocamping-website.md) | [Public website](https://www.agrocamping.eu/) | [The business on Google Maps](https://www.google.com/maps?cid=12963305277474159664)

**AgroCamping Reception.** An internal application that connects reservations and guest enquiries with reception work and financial records. Repeated imports preserve pitch and price changes made by reception staff. Receipts, refunds and reversals are reconciled as financial evidence, separately from booking status.

TypeScript, Astro, Express, Prisma, SQLite, Python, shell tooling, GitLab CI

[Technical overview](case-studies/agrocamping-reception.md)

The source of both systems is private. I present private projects live, to a person. If you are a recruiter, please say in your first message that you are a person and not an AI agent, and we will arrange a screen-share walkthrough.

14 small services run around both systems, each a separate process with one job: mail sync, backups, monitoring, certificate renewal, a weekly security job. The list is in [details.md](details.md).

## Selected public repositories

| Repository | What it is | Made with |
|---|---|---|
| [claude-code-skills](https://github.com/maciejszulia/claude-code-skills)<br>[![CI](https://github.com/maciejszulia/claude-code-skills/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/claude-code-skills/actions/workflows/ci.yml) | Eight skills for Claude Code, each with a diagram: session memory in Markdown, reload of rules, subagent team, delivery to a Codex worker, drift check, lead handoff, README rules, PK. | Markdown, Python |
| [polszczyzna-kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana)<br>[![CI](https://github.com/maciejszulia/polszczyzna-kontrolowana/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/polszczyzna-kontrolowana/actions/workflows/ci.yml) | Controlled Polish (PK): 32 numbered rules that leave each sentence one meaning. A rule set, a Claude skill and a paper with measurements. | Python, LaTeX |
| [pk-rewriter](https://github.com/maciejszulia/pk-rewriter)<br>[![CI](https://github.com/maciejszulia/pk-rewriter/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/pk-rewriter/actions/workflows/ci.yml) | Local Qwen models rewrite Polish instructions into Controlled Polish (PK); pklint checks each result. Evaluation, CPU LoRA, MCP server. | Python, Ollama |
| [neurophify](https://github.com/maciejszulia/neurophify)<br>[![CI](https://github.com/maciejszulia/neurophify/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/neurophify/actions/workflows/ci.yml) | Knowledge graph in 3D, shaped like a brain: reads graphify graph.json or a Markdown folder and writes an interactive page, a turning SVG and an STL model for a README. Release v1.3.0, container image, [live demo](https://maciejszulia.github.io/neurophify/). | Python, 3d-force-graph |
| [book-skills](https://github.com/maciejszulia/book-skills) | Six skills that turn five C++ books and four mathematics books into checklists for writing and reviewing code. | Markdown |
| [rogalddl-scraper](https://github.com/maciejszulia/rogalddl-scraper)<br>[![CI](https://github.com/maciejszulia/rogalddl-scraper/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/rogalddl-scraper/actions/workflows/ci.yml) | Node.js CLI that builds a local metadata catalogue. No npm dependencies, 75 offline tests at the audited snapshot, recovery from interrupted writes. | Node.js |
| [agro-kubernetes](https://github.com/maciejszulia/agro-kubernetes)<br>[![CI](https://github.com/maciejszulia/agro-kubernetes/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/agro-kubernetes/actions/workflows/ci.yml) | Kubernetes lab on two unrooted Xperia phones: a QEMU guest in Termux, a measured status, K3s blocked by 3 missing kernel options. 28 tests. | Python, Bash, QEMU, K3s |
| [millennium-models](https://github.com/maciejszulia/millennium-models)<br>[![CI](https://github.com/maciejszulia/millennium-models/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/millennium-models/actions/workflows/ci.yml) | Minimal models of the 7 Millennium Prize problems: 3 models, 14 numerical checks, 18 figures, an interactive page. Proof plans with the missing step named, no proofs. | Python |

The other public repositories, with CI status, are in [details.md](details.md).

## How I work

I write the requirements, AI coding agents write the code, and I accept the result on tests. Models by role: Claude Fable 5.2 leads and orchestrates the agents, Claude Opus 5.5 writes code, DeepSeek V4.1 Flash (release 1017) serves API calls, Sonnet 5.5 / GPT-6 Luna reads.

The agent tools I use are listed in [details.md](details.md).

Since 2026-11-15 two agent sessions work as a pair. One plans, decides and reviews. The other measures, proves and writes code. Each hands its finished task to the other for review, and a measurement, a test or a quoted rule wins over an opinion. The pair decides what is reversible; I decide everything irreversible or external.

How the agents are kept in check:

- **Handoff and drift check**: a session that reaches its usage limit writes a handoff page; the next lead first compares my orders with the state of the repositories ([lead-handoff](https://github.com/maciejszulia/claude-code-skills/tree/main/skills/lead-handoff), [drift-check](https://github.com/maciejszulia/claude-code-skills/tree/main/skills/drift-check)).
- **Guard hooks**: one hook asks me near the usage limit whether the session continues or hands over; one hook asks for a README update after a large commit ([github-readme](https://github.com/maciejszulia/claude-code-skills/tree/main/skills/github-readme)).
- **Order ledger**: each order I give is recorded with its time, its evidence and a completion percentage.

I apply mathematics to the problems I meet. Each solution leads to new problems, so I keep a solution as small as it can be. The reasoning is in [philosophy](https://github.com/maciejszulia/philosophy). Why a request to a machine is dangerous: [notes/why-ai-is-dangerous.md](notes/why-ai-is-dangerous.md).

## Languages

Share of code by language in my 67 repositories on GitHub (24 public, 43 private), measured on 2026-11-16 with GitHub Linguist, in bytes of code.

| Language | Share | What I use it for |
|---|---|---|
| Jupyter Notebook | 30.9 % | University coursework. Notebooks store their outputs, so the byte count overstates the code. |
| HTML | 29.3 % | Generated documents: CVs and reports of the job-search project, pages of the reception panel. |
| TypeScript | 12.7 % | The AgroCamping reception panel (Astro, Express, Prisma) and the booking website (Next.js, React). |
| JavaScript | 10.5 % | The booking API in Node.js, website scripts and the rogalddl-scraper CLI. |
| Python | 8.7 % | Tools and research: the Controlled Polish linter and pk-rewriter, neurophify, hooks and supervision of AI agents, mathematical models, a farm design model, job-offer collectors. |
| Astro | 2.5 % | Front end of the reception panel. |
| Shell | 1.9 % | Operations: deploys, backups, runit services, status-bar scripts. |
| C | 1.2 % | dwm and st: suckless code with my patches. |
| TeX | 0.8 % | Papers: Controlled Polish, function-generated arithmetics, tpfas. |
| CSS, SCSS | 0.8 % | Styles of the website, the reception panel and the CV page. |

The remaining 0.6 % is Java and Prolog (coursework), MATLAB and Lean (the mathematics repositories), PL/pgSQL (the farm design database), Mermaid, Roff, Makefile and Dockerfile.

Not counted: 2 forks and 1 private coursework repository with a committed Python environment (37.6 MB of Python). With that repository Python would reach 61.4 %.

## Evidence and scope

The [verification record](verification.md) includes **75 passing offline CLI tests** at the audited snapshot, selected API checks and a synthetic reception start-up. Each result names its source revision and scope.

[Guest data, recovery and licensing](engineering-practices.md) documents the limits of access, retention, deletion and reuse. Public descriptions exclude guest records and production configuration. Test results do not certify production health, complete coverage or legal compliance.

## Contact

CV: https://maciejszulia.github.io

maciej.szulia@gmail.com

As a human, I have will, attention and responsibility. 

Hobbies: Psychics, philosophy and humanism. 

Favourite book: John Taylor's „Black Holes: The End of the Universe?” 

Favourite math: Probability and Statistics.
