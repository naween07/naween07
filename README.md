### Full-stack developer — Kathmandu, Nepal

I build and run production systems end to end: product, API, data pipeline, and
the server they run on. Most of my work is client-owned or private, so what
follows describes the systems rather than linking to the code.

---

#### Last Football — [lastfootball.com](https://lastfootball.com)

A football news, livescore and statistics platform, with an Android app on the
Play Store and an internal editorial panel. One GraphQL backend and one
PostgreSQL database serve all three, so the web and mobile experiences stay in
step.

- **Automated match reports.** A generator writes reports from fixture, lineup
  and standings data — scorers and minutes, the turning point, what the result
  means for the table. It is built to *decline* fixtures that aren't worth
  writing up: volume without substance is how a site gets demoted rather than
  ranked. Around 2,000 articles are live.
- **An entity graph, not just pages.** Teams, players and competitions are
  first-class entities with their own hub pages, linked both ways with the
  articles that concern them, and described in `NewsArticle` / `SportsEvent`
  JSON-LD derived on write from the stored row — so the markup cannot drift
  from the page it describes.
- **Rendering for crawlers.** The server prerenders every article and hub to
  static HTML alongside the SPA, generates the sitemap at runtime, and pushes
  new URLs through IndexNow on publish.
- **Operations.** VPS with nginx and PM2, CI deploys, nightly database backups
  verified row by row, scheduled generation jobs.

`React` · `TypeScript` · `Vite` · `Node` · `Apollo GraphQL` · `Prisma` ·
`PostgreSQL` · `Flutter`

#### Compliance and fintech tooling

Internal systems for a SEBON-licensed NEPSE brokerage: digital KYC collection
and review, AML flagging, regulatory PDF annexes, audit trails, role-based
access for staff, and payroll. Built around the regulator's forms and retention
rules rather than bolted on afterwards.

`Node` · `Express` · `JWT` · `SQLite` / `PostgreSQL` · `Electron`

#### Elsewhere

- **AstroNepal Pro** — a Vedic astrology application.
- **Farm accounting** — double-entry accounting for a rainbow trout farm,
  designed to be usable by people who don't know accounting, and intended to
  generalise to agricultural SMEs.

---

Interested in search and AI-answer retrieval, structured data, keeping
generated content on the right side of the quality line, and small teams
shipping things that stay up.

MBA candidate, Asia Pacific University.
