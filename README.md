# Maciej Szulia

Technical support · implementation · web applications · Linux  
Olsztyn, Poland · Looking for full-time remote or hybrid work

[Website & booking API](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-website.md)
· [Reception system](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/case-studies/agrocamping-reception.md)
· [CLI](https://gitlab.com/maciejszulia/rogalddl-scraper)

I help with reservations and guest correspondence at AgroCamping Olsztyn, my
parents' campsite. I also coordinate the development of its website and reception
software. Both AgroCamping projects grew out of that work. They handle bookings
as they reach reception and help keep records consistent when systems exchange data.

I have commercial experience in junior frontend development and e-commerce,
including work with PrestaShop and InsERT Sello.

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
  A small Node.js project with no npm dependencies. You can read the code,
  see why entries were kept, merged or rejected, and run the offline tests locally.
  Its README includes installation steps and input-validation details.

The business applications have private source repositories. Their case studies
explain the design and its limits without sharing guest records or the company's
configuration. You can download and run the CLI.

## How I work

For the camping projects, my role is to describe what reception needs, set
priorities and review the results against agreed requirements. I coordinate
development using AI tools, including Claude Code and Codex, for implementation
and verification.

A problem visible on screen can start in the API, database, an import script or
a deployment setting. I use targeted tests and reproducible builds to check
changes, and document how to run the applications, known failure cases and
anything that still needs checking.

I also document the parts that affect guest data: optional consent, retention,
access permissions and deletion. The [privacy and reliability notes](https://gitlab.com/maciejszulia/maciejszulia/-/blob/main/engineering-practices.md)
explain what the code does and where its limits are. They are not a complete
legal audit.
