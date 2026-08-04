# Clearbit (HubSpot Breeze Intelligence) (clearbit)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Clearbit was a B2B marketing and sales intelligence platform; HubSpot acquired it in late 2023 and has rebranded most capabilities as HubSpot Breeze Intelligence. Legacy Clearbit REST APIs (Enrichment, Reveal, Prospector, Discovery, Risk, Logo, NameToDomain) were widely used; new sign-ups are now redirected into HubSpot's product surface, and standalone Clearbit APIs are being sunset for new customers.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/clearbit/refs/heads/main/apis.yml)

## Type
- **x-type:** company

## Tags
- Sales Intelligence, B2B, Enrichment, Reveal, HubSpot, Marketing

## Timestamps
- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

### Clearbit Enrichment API
Person and Company enrichment given an email or domain. Returns firmographic, technographic, and persona data. Endpoints: /person, /company, /combined.
- **Base URL:** `https://person.clearbit.com`
- **Docs:** https://dashboard.clearbit.com/docs

### Clearbit Reveal API
De-anonymizes website visitors by IP address, returning company firmographics for B2B traffic.
- **Base URL:** `https://reveal.clearbit.com`
- **Docs:** https://dashboard.clearbit.com/docs#reveal-api

### Clearbit Prospector API
Search for people and companies matching firmographic and persona filters.
- **Base URL:** `https://prospector.clearbit.com`
- **Docs:** https://dashboard.clearbit.com/docs#prospector-api

### Clearbit Logo API
Free Logo API: returns a company logo image given a domain. No auth required.
- **Base URL:** `https://logo.clearbit.com`
- **Docs:** https://clearbit.com/logo

### Clearbit Autocomplete (Name-to-Domain) API
Free Autocomplete API: returns company candidates (name, domain, logo) for a name fragment.
- **Base URL:** `https://autocomplete.clearbit.com`
- **Docs:** https://clearbit.com/blog/logo

## Common Properties
- [Website](https://clearbit.com/)
- [Developer Portal](https://dashboard.clearbit.com/docs)
- [Plans](plans/clearbit-plans-pricing.yml) — reconciled (HubSpot acquisition; Breeze Intelligence successor)
- [RateLimits](rate-limits/clearbit-rate-limits.yml) — partial (legacy 600 RPM on Enrichment; Breeze migration in progress)
- [FinOps](finops/clearbit-finops.yml) — reconciled (FOCUS-aligned)

## Maintainers
**FN:** Kin Lane

**Email:** kin@apievangelist.com
