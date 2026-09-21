# Maciej Szulia

Technical support · implementation · web applications · Linux  
Olsztyn, Poland · Looking for full-time remote or hybrid work

[Website & booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md)
· [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md)
· [CLI](https://gitlab.com/maciejszulia/rogalddl-scraper)

I help with reservations and guest correspondence at AgroCamping Olsztyn, my
parents' campsite. I also coordinate the development of its website and reception
software. The two AgroCamping projects come from that work: getting bookings to
reception, keeping records consistent and dealing with integration problems.

I have commercial experience in junior frontend development and e-commerce,
including work with PrestaShop and InsERT Sello.

[Wersja polska](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/README.pl.md)
· [LinkedIn](https://www.linkedin.com/in/maciej-szulia)
· [AgroCamping website](https://www.agrocamping.eu/)

## Projects

- [AgroCamping website and booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md).
  A Polish, English and German website with a separate TypeScript API. The notes
  explain the booking flow, what happens when a notification fails, and how the
  forms and analytics limit the data they keep.
- [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md).
  Tools for daily reception work. The details include handling the same booking
  more than once without overwriting staff decisions, user permissions and
  recovery after a failed release.
- [Local metadata catalogue CLI](https://gitlab.com/maciejszulia/rogalddl-scraper).
  A smaller Node.js project with no npm dependencies. You can read the code,
  see why entries were kept, merged or rejected, and run the offline tests locally.
  Its README includes installation steps and input-validation details.

The business applications have private source repositories. Their public notes
cover the design and its limits without exposing guest records or operational
configuration. The CLI is available to download and run.

## How I work

For the camping projects, I describe what reception needs, set priorities and
check the results against agreed requirements. I use Claude Code and Codex for
implementation and verification. My part in these AI-assisted projects is
coordinating the work and reviewing what gets delivered.

Troubleshooting can mean following a problem from the screen through the API and
database to an import script or deployment setting. I use targeted tests and
reproducible builds to check changes, and keep setup instructions and known failure
cases in the documentation. The project notes distinguish what was tested from
what still needs checking.

I also document the parts that affect guest data: optional consent, retention,
access permissions and deletion. The [privacy and reliability notes](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/engineering-practices.md)
explain the mechanisms in the code and their limits. They don't claim a complete
legal audit.
