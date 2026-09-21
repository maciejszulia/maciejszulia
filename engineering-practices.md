# Engineering that is easy to miss in a screenshot

These examples explain how the projects handle failure, personal data and reuse
boundaries. They describe inspected code and documented limitations. They are not
a legal opinion, certification or claim that every deployment has been audited.

## Privacy as application behaviour

| Concrete mechanism | Engineering value | Boundary |
| --- | --- | --- |
| A separate, optional review-request opt-in, recorded with server time and a terms version | Makes a consent-related decision inspectable beyond a checkbox | A stored flag alone does not prove that a notice, lawful basis or withdrawal process is adequate. |
| A short-lived website draft that excludes contact, consent and payment fields | Reduces what remains in browser storage | Other application and provider records have separate lifecycles. |
| Reduced website analytics dimensions | Avoids persisting an IP address in the inspected aggregate path; removes query strings and full referrer paths | This does not establish what the hosting access logs or other processors retain. |
| Authenticated reservation identity replacement and notification-payload cleanup | Makes a privacy operation explicit and testable | It is scoped field replacement, not demonstrated irreversible anonymisation of every linked record. |
| Enquiry erasure propagation with a retained import identity | Prevents an old synchronisation feed from recreating a deleted enquiry | The retained identity needs its own purpose and retention decision; mailboxes and backups are separate. |
| Backend permissions that deny ungranted operations | Places operational access control at the API boundary | Access control does not determine a lawful basis or anonymise stored records. |

Data minimisation, storage limitation and appropriate protection are part of the
[European Commission's GDPR principles](https://commission.europa.eu/law/law-topic/data-protection/information-business-and-organisations/principles-gdpr_en).
These principles inform questions to ask about a system; the code examples above
do not establish compliance with every obligation.

The distinction between replacing an identifier and making a person
unidentifiable matters. The [EDPB explains the difference between pseudonymisation
and anonymisation](https://www.edpb.europa.eu/topics/ai-and-technology/anonymisation-pseudonymisation_en).
I do not treat hashing, redaction or a retained import identity as proof of
irreversible anonymity.

## Reliability protects business records too

- An outbox preserves delivery state when a notification transport fails.
- Replay rules stop repeated imports from overwriting decisions already made by reception.
- Financial reconciliation uses movement evidence and integer minor units rather than trusting a status label alone.
- Release recovery procedures account for database changes and competing writers.

These are useful support and implementation topics because they connect a visible
symptom with the underlying state that must be checked before retrying or deleting
anything. See the [website](case-studies/agrocamping-website.md) and
[reception](case-studies/agrocamping-reception.md) case studies.

## Public source, content rights and licensing

The [catalogue CLI](https://gitlab.com/maciejszulia/rogalddl-scraper) demonstrates
local validation, provenance and recoverable publication. Its offline test route
uses synthetic tools and data. Live metadata discovery contacts external services;
optional fingerprint modes can download temporary audio.

[YouTube's terms](https://www.youtube.com/static?template=terms) constrain automated
access and content use. A public URL, a metadata-only flag or temporary-file
cleanup does not by itself establish permission. The project README explains the
mechanisms and known limits without claiming copyright clearance.

The two business applications remain private and proprietary. The public CLI
currently has no declared software license. Publication here does not add a
license to that code, the business applications, photographs or third-party media.
Dependency and tool licenses remain separate. This portfolio makes no blanket
claim that all third-party rights have been audited.

## Evidence and honest scope

The case studies are based on identified development-source snapshots reviewed on
21 September 2026. A test result refers to the named snapshot and test selection;
it does not prove production configuration, complete test coverage, traffic,
business impact or legal compliance. The [verification record](verification.md)
states what was actually run.

[Back to profile](README.md)
