# Maciej Szulia

Technical support · implementation · web applications · Linux  
Olsztyn, Poland · Availability: full-time remote or hybrid work

[Website & booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md)
· [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md)
· [CLI](https://gitlab.com/maciejszulia/rogalddl-scraper)

Work at AgroCamping Olsztyn, a campsite run by Maciej Szulia's parents, includes
reservation support, guest correspondence and coordination of website and reception
software development. Both AgroCamping projects grew out of that work. They handle bookings
as they reach reception and help keep records consistent when systems exchange data.

Previous commercial experience includes junior frontend development and e-commerce,
with PrestaShop and InsERT Sello.

[Wersja polska](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/README.pl.md)
· [LinkedIn](https://www.linkedin.com/in/maciej-szulia)
· [AgroCamping website](https://www.agrocamping.eu/)

## Projects

- [AgroCamping website and booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md).
  A website in Polish, English and German, with a separate TypeScript API.
  The case study follows a booking through the system, including what happens
  when a notification fails and which data the forms and analytics keep.
- [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md).
  An application for daily reception work. Repeated imports preserve pitch
  and price changes made by reception staff. The case study also covers user
  permissions and recovery after a failed release.
- [Local metadata catalogue CLI](https://gitlab.com/maciejszulia/rogalddl-scraper).
  A small Node.js project with no npm dependencies. The public code shows
  why entries were kept, merged or rejected, with offline tests available to run locally.
  Its README includes installation steps and input-validation details.

The business applications have private source repositories. Their case studies
explain the design and its limits without sharing guest records or the company's
configuration. The CLI is available to download and run locally.

## Development approach

Maciej Szulia's contribution to the camping projects covers reception requirements,
priorities, development coordination and review against agreed criteria. AI tools,
including Claude Code and Codex, are used for implementation and verification.

A problem visible on screen can start in the API, database, an import script or
a deployment setting. Changes are checked with targeted tests and reproducible
builds. Project documentation covers how to run the applications, known failure
cases and anything that still needs checking.

Documentation also covers optional consent, retention, access permissions and
deletion of guest data. The [privacy and reliability notes](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/engineering-practices.md)
explain what the code does and where its limits are. They are not a complete
legal audit.
