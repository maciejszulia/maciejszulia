# Verification record

Recorded on 21 September 2026 using Node.js **22.22.3**. Business-project checks
used separate checkouts with their own dependencies and synthetic data. The
production applications and guest databases were not used for these checks.

| Project and source snapshot | Fresh check | Result |
| --- | --- | --- |
| Website — `0cfda93c87a83fc2e3a5c1a6f1bb0ec053c1e2e9` | Root and API lockfile installation; static export build; API TypeScript build | Passed |
| Same website snapshot | Five focused API suites: reservation privacy, review consent, visit analytics, reservation service and Stripe provider | 33 passed; 0 failed; 0 skipped |
| Same website snapshot | Start static server and request German, Polish and English pages plus build metadata | Four HTTP 200 responses; expected commit and staging marker verified |
| Reception — `d79af82350cefeb763e8b672e12c562793a51280` | Backend build; domain, service and middleware suites | 670 passed; 0 failed; 2 skipped |
| Same reception snapshot | Frontend check and verify (tests, static build and UI contracts) | 169 passed; 0 failed; 0 skipped; type check: 0 errors/warnings, 2 hints |
| Same reception snapshot | Copied-schema migrations, synthetic account and pitches, backend health/login, gateway CSRF login and session identity | Passed with external networking blocked; owned processes and temporary state cleaned |
| Public CLI — `67483084db5adc4a0d234985f1e834601a88ecc7` | `./test-all.sh`: syntax checks plus the existing Node test suite | 74 passed; 0 failed; 0 skipped |
| Same CLI snapshot | Help/version, separate-prefix installation and installed diagnostics | Passed; optional `fpcalc` unavailable on the review host |

Website builds and selected API tests ran with external networking disabled and
only loopback available. The CLI suite substitutes synthetic external tools; no
live discovery, playback or media download was used for its evaluation.

Reception build and test commands also ran with only loopback networking. Two
WhatsApp-related domain tests were skipped because the optional Python
`websocket-client` dependency was absent. Mail, migration, operations and the
entire CI suite were not included in that selected backend test run.
The separate runtime smoke did apply migrations to a fresh synthetic database;
it did not run the full migration regression suite or a manual browser/layout review.

The CLI documentation update also passed its
[GitLab pipeline](https://gitlab.com/maciejszulia/rogalddl-scraper/-/pipelines/2867408036)
at commit `da99e1882fa7776f4bfe8154d4a376705d470867`.

During the initial portfolio review, the public CLI README was the only changed
file in that repository. The private application changes in that review were documentation. Source snapshot hashes above identify the
application code reviewed, rather than a later documentation-only commit.

## Limits of these results

The website check did not run the full browser suite or the MySQL/MariaDB matrix.
It did not send SMTP messages or create a payment. A static preview with an
unavailable local API does not demonstrate a completed reservation.

These results do not establish a coverage percentage, security certification,
production health, uptime, performance gains or legal compliance. They are a
reproducible starting point for technical discussion.

## Follow-up README and code audit: 21 September 2026

A later audit corrected two CLI documentation guarantees and fixed the syntax
checker for checkout paths containing spaces. At commit
[`992a8126`](https://gitlab.com/maciejszulia/rogalddl-scraper/-/commit/992a8126a5ff3ea28cc7dcad51e7827926b89081), the fresh offline suite passed
**75 tests, 0 failed, 0 skipped**, including the new regression. The
[merge-request pipeline](https://gitlab.com/maciejszulia/rogalddl-scraper/-/pipelines/2868596537) also passed.
The README installation paths and bounded scan example were checked with isolated
synthetic tools. Live extraction, playback and audio fingerprinting remain untested.

These results are a separate run; the earlier snapshot and its 74-test result
above remain historical evidence. The audit also checked the website and reception
case-study claims against their development source. It did not certify production
configuration or complete legal compliance.

[Back to profile](README.md)
