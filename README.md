# Clearbit (HubSpot Breeze Intelligence) (clearbit)

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
