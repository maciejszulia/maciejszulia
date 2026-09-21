# AgroCamping: multilingual website and booking workflow

AgroCamping is a family campsite in Olsztyn, Poland. This project combines its Polish, English and German website with a separate booking API and an integration with the reception application.

The stack is Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe and GitLab CI. The public website is [agrocamping.eu](https://www.agrocamping.eu/).

## The booking problem

The form has to connect what guests see with what reception can confirm. Dates, party size, pitch type, electricity and payment state all affect that decision. Guests also need clear outcomes when they submit a request again, a payment is interrupted or an email cannot be delivered.

## Development responsibilities

Development coordination for the family campsite covers requirements, review of results, fixes and delivery. AI coding tools are used for implementation and verification.

## How the system handles bookings

| Part of the system | What it does |
| --- | --- |
| Static website and separate transactional API | Public content can be deployed as static files, with booking writes handled by the API. |
| Shared pricing and booking rules | The interface and API use common domain modules to reduce the risk of contradictory rules. |
| Pending-availability state | A request can reach reception for review when the system cannot safely confirm capacity. |
| Idempotency and database transactions | The API distinguishes retries from conflicting submissions. Transactions handle booking allocation and related records together. |
| Payment-event verification | Webhook signatures and stored provider-event identities support payment callbacks and duplicate delivery handling. |
| Persistent notification outbox | Reservation storage and delivery attempts have separate states, so failed delivery can be retried and investigated. |
| Synthetic database tests | An isolated MySQL/MariaDB test matrix is available for checking persistence behaviour against both engines. |

## Privacy controls

The system keeps the optional opt-in for review requests separate from required booking acceptance. It records the opt-in with a server timestamp and a terms version.

A short-lived browser draft saves selected stay fields. It excludes contact details, consent and payment fields. Visit analytics derive country from an IP address and pass only reduced fields to the aggregate store. That path discards query strings and full referrer paths.

Authenticated API operations replace selected reservation identity fields, clear related notification payloads and remove stored idempotency responses. A separate retention sweep removes old replay records and reduces older notification and attribution data. Erased enquiries leave a tombstone so that a retry cannot recreate the enquiry under the same key.

These controls cover specific data paths and do not establish blanket GDPR compliance. The retention sweep does not automatically delete every guest record. Payment data held by providers, delivered email, backups and the reception application have separate data lifecycles. This review does not verify their complete erasure or the organisational and legal arrangements around them.

## Review scope

The source is private and proprietary. This case study covers code reviewed on 21 September 2026. It does not certify the live deployment's configuration, uptime, conversion impact or compliance. No revenue or performance improvement is claimed without measured evidence.
