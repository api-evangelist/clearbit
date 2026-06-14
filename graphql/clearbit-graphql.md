# Clearbit GraphQL Schema

## Overview

This directory contains a conceptual GraphQL schema for the Clearbit (now HubSpot Breeze Intelligence) B2B data enrichment and intelligence platform. Clearbit provided REST APIs for person and company enrichment, website visitor de-anonymization, prospecting, risk scoring, and logo resolution. HubSpot acquired Clearbit in late 2023 and has integrated most capabilities into HubSpot Breeze Intelligence; standalone Clearbit API access is being sunset for new customers.

The schema in `clearbit-schema.graphql` is a conceptual translation of the REST API surface into GraphQL types, queries, and mutations. It is not an officially published Clearbit endpoint.

## Schema File

- `clearbit-schema.graphql` — Full GraphQL schema with 55+ named types.

## Type Summary

### Person Types
| Type | Description |
|------|-------------|
| `Person` | Core person record from Person Enrichment |
| `PersonName` | Given name, family name, full name |
| `PersonEmail` | Email address with verification status |
| `PersonGeo` | Geographic location for a person |
| `PersonEmployment` | Current employer, title, role, seniority |
| `EmploymentTitle` | Title string, role, sub-role, seniority |
| `EmploymentSeniority` | Enum: EXECUTIVE through INTERN |
| `EmploymentSubRole` | Enum: ENGINEERING, SALES, MARKETING, etc. |
| `SocialProfile` | Aggregated social handles (LinkedIn, Twitter, GitHub) |
| `LinkedInProfile` | LinkedIn handle and profile URL |
| `TwitterProfile` | Twitter handle, bio, follower counts |
| `GitHubProfile` | GitHub handle, repos, follower counts |
| `PersonBio` | Biography text and source URL |
| `PersonAvatar` | Profile image URL |

### Company Types
| Type | Description |
|------|-------------|
| `Company` | Core company record from Company Enrichment |
| `CompanyDomain` | Primary domain and TLD |
| `CompanyName` | Name and known aliases |
| `CompanyLegalName` | Registered legal name and jurisdiction |
| `CompanyDescription` | Description text and tagline |
| `CompanyMetrics` | Revenue, Alexa rank, market cap, raised |
| `CompanyGeo` | Full headquarters address with lat/lng |
| `CompanyCategory` | Sector, industry group, industry, SIC/NAICS codes |
| `CompanyTags` | Keyword tags for the company |
| `CompanyPhone` | Phone number and type |
| `CompanyEmailProvider` | Whether the domain provides email hosting |
| `CompanySite` | Website metadata (title, meta description, emails) |
| `CompanyTech` | Individual technology used by the company |
| `TechStack` | Full tech stack with categories |
| `TechCategory_` | Grouping of technologies by category |
| `TechName` | Technology name, tag, and category |
| `CompanySocial` | Social handles (Twitter, LinkedIn, Crunchbase, etc.) |
| `CompanyFundingTotal` | Total funding raised |
| `CompanyFundingRound` | Individual funding round details |
| `CompanyIPO` | IPO status, valuation, ticker |
| `FoundedYear` | Year and decade company was founded |
| `CompanyPeople` | Notable people associated with the company |
| `CompanyEmployeeCount` | Employee count and range |
| `EmployeeGrowth` | Growth rates at 3m, 6m, 1yr, 2yr |

### Product / Enrichment Result Types
| Type | Description |
|------|-------------|
| `Enrichment` | Generic enrichment wrapper (streaming/webhook) |
| `PersonEnrichment` | Person-only enrichment result with status |
| `CompanyEnrichment` | Company-only enrichment result with status |
| `CombinedEnrichment` | Combined person + company enrichment |
| `ProspectorResult` | Person record from Prospector search |
| `RevealResult` | Company record de-anonymized from an IP |
| `RiskResult` | Risk score and flags for an email address |
| `DiscoverResult` | Company returned by the Discovery API |
| `EmailVerification` | Email deliverability and verification result |

### Auth / Config Types
| Type | Description |
|------|-------------|
| `APIKey` | API key credential for Clearbit requests |
| `Webhook` | Webhook subscription with events and secret |

### Enums
| Enum | Values |
|------|--------|
| `EmploymentSeniority` | EXECUTIVE, VP, DIRECTOR, MANAGER, SENIOR, MID, JUNIOR, INTERN, UNKNOWN |
| `EmploymentSubRole` | ENGINEERING, PRODUCT, DESIGN, MARKETING, SALES, SUPPORT, FINANCE, LEGAL, HR, OPERATIONS, EXECUTIVE, EDUCATION, OTHER |
| `TechCategory` | CRM, ANALYTICS, ADVERTISING, EMAIL, CLOUD, ECOMMERCE, CONTENT, SECURITY, DEVOPS, FINANCE, HR, SUPPORT, COLLABORATION, OTHER |
| `RiskLevel` | LOW, MEDIUM, HIGH, VERY_HIGH, UNKNOWN |
| `WebhookEvent` | PERSON_ENRICHED, COMPANY_ENRICHED, COMBINED_ENRICHED, REVEAL_MATCHED, RISK_SCORED |
| `FoundedDecade` | BEFORE_1990, DECADE_1990S, DECADE_2000S, DECADE_2010S, DECADE_2020S |

### Scalars
| Scalar | Purpose |
|--------|---------|
| `Date` | Calendar date (YYYY-MM-DD) |
| `DateTime` | ISO 8601 timestamp |
| `URL` | Absolute URL string |
| `Email` | RFC 5321 email address |
| `IP` | IPv4 or IPv6 address string |

## Queries

| Query | Description |
|-------|-------------|
| `enrichPerson(email)` | Enrich a person by email address |
| `enrichCompany(domain)` | Enrich a company by domain |
| `enrichCombined(email)` | Person + company enrichment in one call |
| `reveal(ip)` | De-anonymize a website visitor by IP |
| `prospectPeople(...)` | Search for people by role, domain, location |
| `riskScore(email)` | Score fraud/spam risk for an email |
| `discoverCompanies(...)` | Discover companies by firmographic filters |
| `verifyEmail(email)` | Check email deliverability |
| `logo(domain)` | Resolve a company logo URL by domain |
| `autocomplete(name)` | Autocomplete company name to domain |
| `webhooks` | List configured webhook subscriptions |
| `webhook(id)` | Fetch a single webhook by ID |
| `apiKeys` | List API keys for the account |

## Mutations

| Mutation | Description |
|----------|-------------|
| `createWebhook(url, events, secret)` | Register a new webhook |
| `updateWebhook(id, ...)` | Update an existing webhook |
| `deleteWebhook(id)` | Remove a webhook subscription |
| `triggerEnrichment(email, webhook)` | Trigger async enrichment delivery |

## References

- Clearbit Docs: https://dashboard.clearbit.com/docs
- HubSpot Breeze Intelligence: https://www.hubspot.com/products/breeze-intelligence
- GitHub: https://github.com/clearbit
