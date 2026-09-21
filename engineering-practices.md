# Guest data, recovery and licensing

These notes cover parts of the projects that a screenshot cannot show: what
happens to guest data, how the applications recover from failures and what can
be reused. They are based on code review, not a legal opinion, certification or
an audit of every deployment.

## How the applications handle guest data

| Mechanism | What it does | Limitation |
| --- | --- | --- |
| Separate, optional consent to receive a review request | Records the choice with server time and a terms version | A stored flag alone does not prove that the notice, lawful basis or withdrawal process is adequate. |
| A short-lived website draft | Leaves contact, consent and payment fields out of the saved draft | Other application and provider records have separate lifecycles. |
| Reduced website analytics | Does not store an IP address in the reviewed aggregate path; removes query strings and full referrer paths | Hosting access logs and other processors may retain different data; those were not verified. |
| An authenticated operation to replace reservation identity fields | Replaces selected fields and clears related notification payloads | This does not demonstrate irreversible anonymisation of every linked record. |
| Passing enquiry deletion between systems while retaining its import identity | Stops an old synchronisation feed from recreating a deleted enquiry | The retained identity needs its own purpose and retention decision. Mailboxes and backups are separate. |
| Backend permissions that deny operations unless granted | Checks access at the API, where the action takes place | Access control does not determine a lawful basis or anonymise stored records. |

Data minimisation, storage limitation and appropriate protection are part of the
[European Commission's GDPR principles](https://commission.europa.eu/law/law-topic/data-protection/information-business-and-organisations/principles-gdpr_en).
The examples above address parts of those principles. They do not establish
compliance with every obligation.

Replacing an identifier does not necessarily make a person unidentifiable.
The [EDPB explains the difference between pseudonymisation
and anonymisation](https://www.edpb.europa.eu/topics/ai-and-technology/anonymisation-pseudonymisation_en).
Hashing, redaction or keeping an import identity is not, on its own, proof of
irreversible anonymity.

## When an operation fails or runs twice

- An outbox tracks delivery so a failed notification can be retried.
- Repeated imports preserve decisions already made by reception staff.
- Financial reconciliation checks recorded movements and uses integer minor units; a payment status label alone is not enough.
- Release recovery procedures account for database changes and other processes writing to it.

These details help when diagnosing a problem: they show which records to check
before retrying an operation or deleting data. See the [website](case-studies/agrocamping-website.md) and
[reception](case-studies/agrocamping-reception.md) case studies.

## Public source, content rights and licensing

The [catalogue CLI](https://gitlab.com/maciejszulia/rogalddl-scraper) validates
entries locally, records where they came from and can recover interrupted
catalogue writes. Its offline tests use synthetic tools and data. Looking up
live metadata contacts external services, and optional fingerprint modes can
download temporary audio.

[YouTube's terms](https://www.youtube.com/static?template=terms) constrain automated
access and content use. A public URL, a metadata-only flag or temporary-file
cleanup does not by itself establish permission. The project README explains the
behaviour and known limits. It does not establish copyright clearance.

The two business applications remain private and proprietary. The public CLI
currently has no declared software license. Publication here does not add a
license to that code, the business applications, photographs or third-party media.
Dependency and tool licenses remain separate. This portfolio makes no blanket
claim that all third-party rights have been audited.

## What was checked

The case studies use identified development-source snapshots reviewed on
21 September 2026. A test result refers to the named snapshot and test selection;
it does not prove production configuration, complete test coverage, traffic,
business impact or legal compliance. The [verification record](verification.md)
states what was actually run.

[Back to profile](README.md)
