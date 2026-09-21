# AgroCamping: from a multilingual website to a booking workflow

**Context:** a family campsite in Olsztyn, Poland.  
**Role:** AI-assisted development coordination for my parents’ business.  
**Technologies:** Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI.  
**Public website:** [agrocamping.eu](https://www.agrocamping.eu/).

## The problem

A booking form has to connect what guests see with what reception can actually confirm. Dates, party size, pitch type, electricity and payment state affect that decision. Repeated submissions, interrupted payments and unavailable email delivery also need understandable outcomes.

The project combines a Polish, English and German website with a separate booking API and an integration boundary to the reception application.

## My contribution

I coordinate the development using AI coding tools and the operational context of my parents’ campsite. The work involves turning business needs into concrete requirements, checking behaviour against those requirements, and coordinating fixes and delivery. I describe this as AI-assisted project work, not as proof that I manually authored every part of the code.

## Engineering decisions worth discussing

| Decision | Why it matters |
| --- | --- |
| Static website, separate transactional API | Public content can be deployed as static files while booking writes stay within the API. |
| Shared pricing and booking rules | The interface and API use common domain modules, reducing opportunities for contradictory rules. |
| Explicit pending-availability state | A request can reach reception for review when the system cannot safely confirm capacity. |
| Idempotency and database transactions | Retried requests are distinguished from conflicting submissions; booking allocation and related records are handled together. |
| Verified payment events | Webhook signatures and stored provider-event identities support handling payment callbacks and duplicate delivery. |
| Persistent notification outbox | Reservation storage and delivery attempts have separate states; failed delivery can be retried and investigated. |
| Synthetic tests against two database engines | The repository provides an isolated MySQL/MariaDB matrix for checking persistence behaviour. |

## Privacy work that is easy to miss in a screenshot

The system separates an optional review-request opt-in from required booking acceptance. The opt-in has a server timestamp and a terms version, rather than relying only on a browser checkbox.

A short-lived browser draft retains selected stay fields, excluding contact details, consent and payment fields. Visit analytics derive country from an IP address, then pass only reduced dimensions to the aggregate store; query strings and full referrer paths are discarded on that path.

Authenticated API operations replace selected reservation identity fields, clear related notification payloads and remove stored idempotency responses. A separate retention sweep removes old replay records and reduces older notification and attribution data. Enquiry erasure retains a tombstone so that a retry cannot recreate the erased enquiry under the same key.

**Scope matters:** these are implemented technical mechanisms, not a claim of blanket GDPR compliance. The retention sweep is not automatic deletion of every guest record. Provider-held payment data, delivered email, backups and the reception application have their own data lifecycles. Their complete erasure and organisational/legal arrangements are outside this case study’s verification.

## What this project demonstrates

The useful part is the connection between a real operational problem and behaviour that can be inspected: validation, retry handling, delivery failures, data minimisation and verification steps. Those are relevant discussion points for application support, implementation and technical customer support work.

The source remains private and proprietary. This case study describes code reviewed on 21 September 2026; it does not certify the configuration, uptime, conversion impact or compliance of the live deployment. No revenue or performance improvement is claimed without measured evidence.
