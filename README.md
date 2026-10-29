# Clearbit (HubSpot Breeze Intelligence)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Clearbit is a B2B marketing and sales intelligence platform whose REST APIs resolve an email address to a person, a domain to a company, and an IP address to the business behind it, returning firmographic, technographic and persona data across a documented 100+ company and 60+ person attributes classified against GICS, SIC and NAICS. HubSpot acquired Clearbit in December 2023 and sells the capability as HubSpot Breeze Intelligence. The legacy Clearbit APIs (Enrichment, Streaming, Reveal, Prospector, Discovery, Risk, Name-to-Domain, Autocomplete) remain live and answer on their production hosts, but the provider is in publicly dated wind-down — new API keys have not been issued since 2023, free accounts were sunset 2025-04-30, and the free Logo API was sunset 2025-12-08 and its host no longer resolves. Only the free Autocomplete API is callable without a credential.

**Areas:** Sales Intelligence · B2B · Data Enrichment · Reveal · HubSpot · Marketing · Data · Firmographics · Lead Enrichment · Company Data

## Clearbit (HubSpot Breeze Intelligence) on APIs.io

Everything profiled for Clearbit (HubSpot Breeze Intelligence) is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/clearbit/](https://apis.io/providers/clearbit/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [Clearbit Person Enrichment API](https://apis.io/apis/clearbit/enrichment/) — Person enrichment from an email address, plus the Combined lookup that returns the person and their company in one response. Endpoints: /v2/people/find,…
- [Clearbit Company Enrichment API](https://apis.io/apis/clearbit/company-enrichment/) — Company enrichment from a domain, and the Name to Domain lookup that resolves a company name to its primary domain. Endpoints: /v2/companies/find,…
- [Clearbit Streaming Enrichment API](https://apis.io/apis/clearbit/enrichment-streaming/) — The same enrichment contract served from a streaming host that holds the connection open for up to 60 seconds so a queued (202) lookup resolves in-band. The…
- [Clearbit Reveal API](https://apis.io/apis/clearbit/reveal/) — De-anonymizes website visitors by IP address, returning company firmographics for B2B traffic. Endpoint /v1/companies/find?ip=. Verified live 2026-08-13…
- [Clearbit Prospector API](https://apis.io/apis/clearbit/prospector/) — Search for people matching firmographic and persona filters. Endpoint /v1/people/search. Verified live 2026-08-13 (HTTP 401 auth_required, x-api-version…
- [Clearbit Discovery API](https://apis.io/apis/clearbit/discovery/) — Search Clearbit's company database with a structured query to build target-market lists. Endpoint /v1/companies/search. Verified live 2026-08-13 (HTTP 401…
- [Clearbit Risk API](https://apis.io/apis/clearbit/risk/) — Scores an email address for fraud and abuse risk. Endpoint /v1/calculate?email=. Verified live 2026-08-13 (HTTP 401 auth_required, x-api-version 2016-05-03…
- [Clearbit Autocomplete API](https://apis.io/apis/clearbit/name-to-domain/) — Free, unauthenticated company autocomplete: returns candidate companies (name, domain, logo) for a name fragment. Endpoint /v1/companies/suggest?query=. The…
- [Clearbit Logo API (retired)](https://apis.io/apis/clearbit/logo/) — RETIRED 2025-12-08. The free Logo API returned a company logo image for a domain with no authentication. Announced 2025-02-13, moved to 2025-12-01, then…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Clearbit Webhooks](https://apis.io/asyncapis/clearbit/clearbit-webhooks/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/clearbit/](https://apis.io/graphqls/clearbit/clearbit-graphql/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Clearbit Authentication](https://apis.io/security/clearbit/clearbit-authentication/)
- [Clearbit Domain Security](https://apis.io/security/clearbit/clearbit-domain-security/)
- [Clearbit Trust Center](https://apis.io/security/clearbit/clearbit-trust-center/)
- [Clearbit Vulnerability Disclosure](https://apis.io/security/clearbit/clearbit-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Clearbit Plans Pricing](https://apis.io/plans/clearbit/clearbit-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Clearbit Rate Limits](https://apis.io/rate-limits/clearbit/clearbit-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Clearbit Finops](https://apis.io/finops/clearbit/clearbit-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://clearbit.com/)
- [Documentation](https://help.clearbit.com/)
- [API reference](https://clearbit.com/attributes)
- [Pricing](https://clearbit.com/pricing)
- [Support](https://help.clearbit.com/)
- [Blog](https://clearbit-blog.ghost.io/rss/)
- [Compliance](https://clearbit.com/trust#compliance)
- [Terms of service](https://clearbit.com/legal)
- [Privacy policy](https://clearbit.com/privacy-policy)
- [GitHub](https://github.com/clearbit)
- [Status](https://status.clearbit.com/)

## API Evangelist rating

**Kin Score 57.9** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 39.0 |
| Contract governance | 4.5 |
| Operational transparency | 92.1 |
| Developer ergonomics | 52.4 |
| Access clarity | 75.0 |

**Agent readiness 25.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 35.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/clearbit/](https://apis.io/providers/clearbit/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Clearbit (HubSpot Breeze Intelligence): the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/clearbit/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
