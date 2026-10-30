# Insforge

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

InsForge is an open-source (Apache-2.0), agent-native cloud infrastructure platform built so that AI coding agents can provision and operate an entire backend end to end through a CLI and packaged agent skills instead of a human clicking through a dashboard. A single project bundles a Postgres database with schema management and row-level security, authentication (users, sessions, OAuth, JWT), S3-compatible object storage, Deno-based edge functions with cron, a unified AI model gateway, realtime subscriptions and webhooks, long-lived custom compute, frontend hosting via Vercel, transactional email, and payments via Stripe and Razorpay. The REST API is documented as fourteen OpenAPI 3.0 service specifications and is driven by an official TypeScript SDK, CLI, and hosted MCP server. InsForge is a Y Combinator company.

**Areas:** Company · Backend-as-a-Service · Agent-Native · Cloud Infrastructure · Database · Authentication · Storage · Serverless · Edge Functions · AI Gateway · Payments · Real-Time

## Insforge on APIs.io

Everything profiled for Insforge is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/insforge/](https://apis.io/providers/insforge/)** — or go straight to one of the APIs or properties below.

### APIs (11)

- [Insforge Admin API](https://apis.io/apis/insforge/insforge-admin-api/) — The Admin API from Insforge — 54 operation(s) for admin.
- [Insforge Channels API](https://apis.io/apis/insforge/insforge-channels-api/) — Configure realtime channel patterns, webhooks, and availability.
- [Insforge Client API](https://apis.io/apis/insforge/insforge-client-api/) — The Client API from Insforge — 35 operation(s) for client.
- [Insforge Configuration API](https://apis.io/apis/insforge/insforge-configuration-api/) — Manage realtime retention settings.
- [Insforge Messages API](https://apis.io/apis/insforge/insforge-messages-api/) — Inspect realtime message history and delivery stats.
- [Insforge Payment Webhooks API](https://apis.io/apis/insforge/insforge-payment-webhooks-api/) — Provider webhook ingestion routes
- [Insforge Permissions API](https://apis.io/apis/insforge/insforge-permissions-api/) — Manage helper endpoints for realtime RLS examples.
- [Insforge Razorpay Payments API](https://apis.io/apis/insforge/insforge-razorpay-payments-api/) — Razorpay Orders, Subscriptions, catalog, manual webhook setup, sync, customer, and transaction routes
- [Insforge S3 Access Keys API](https://apis.io/apis/insforge/insforge-s3-access-keys-api/) — The S3 Access Keys API from Insforge — 3 operation(s) for s3 access keys.
- [Insforge S3 Protocol API](https://apis.io/apis/insforge/insforge-s3-protocol-api/) — The S3 Protocol API from Insforge — 1 operation(s) for s3 protocol.
- [Insforge Stripe Payments API](https://apis.io/apis/insforge/insforge-stripe-payments-api/) — Stripe Checkout, Billing Portal, catalog, sync, customer, subscription, and transaction routes

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [insforge](https://apis.io/servers/insforge/insforge/)

#### Collections (11)

Postman and Open Collection request collections.

- [Insforge AI Admin API](https://apis.io/collections/insforge/open-insforge-admin-api/)
- [Insforge AI Admin Channels API](https://apis.io/collections/insforge/open-insforge-channels-api/)
- [Insforge AI Admin Client API](https://apis.io/collections/insforge/open-insforge-client-api/)
- [Insforge AI Admin Configuration API](https://apis.io/collections/insforge/open-insforge-configuration-api/)
- [Insforge AI Admin Messages API](https://apis.io/collections/insforge/open-insforge-messages-api/)
- [Insforge AI Admin Payment Webhooks API](https://apis.io/collections/insforge/open-insforge-payment-webhooks-api/)
- [Insforge AI Admin Permissions API](https://apis.io/collections/insforge/open-insforge-permissions-api/)
- [Insforge AI Admin Razorpay Payments API](https://apis.io/collections/insforge/open-insforge-razorpay-payments-api/)
- [Insforge AI Admin S3 Access Keys API](https://apis.io/collections/insforge/open-insforge-s3-access-keys-api/)
- [Insforge AI Admin S3 Protocol API](https://apis.io/collections/insforge/open-insforge-s3-protocol-api/)
- [Insforge AI Admin Stripe Payments API](https://apis.io/collections/insforge/open-insforge-stripe-payments-api/)

#### Overlays (3)

OpenAPI overlays, including conversational phrasing for each operation.

- [Insforge Auth Overlay](https://apis.io/overlays/insforge/insforge-auth-overlay/)
- [Insforge Payments Overlay](https://apis.io/overlays/insforge/insforge-payments-overlay/)
- [Insforge Storage Overlay](https://apis.io/overlays/insforge/insforge-storage-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Insforge Authentication](https://apis.io/security/insforge/insforge-authentication/)
- [Insforge Domain Security](https://apis.io/security/insforge/insforge-domain-security/)
- [Insforge Vulnerability Disclosure](https://apis.io/security/insforge/insforge-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Insforge Scopes](https://apis.io/scopes/insforge/insforge-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://insforge.dev)
- [Documentation](https://docs.insforge.dev)
- [Getting started](https://docs.insforge.dev/quickstart)
- [API reference](https://docs.insforge.dev/api-reference/admin/admin-login)
- [Pricing](https://insforge.dev/pricing)
- [Sign up](https://insforge.dev/dashboard)
- [Support](https://discord.gg/DvBtaEc9Jz)
- [Changelog](https://insforge.dev/changelogs)
- [Blog](https://insforge.dev/blog)
- [Terms of service](https://insforge.dev/terms)
- [Privacy policy](https://insforge.dev/privacy)
- [GitHub](https://github.com/InsForge)

## API Evangelist rating

**Kin Score 53.4** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 76.7 |
| Contract quality | 46.5 |
| Contract governance | 4.5 |
| Operational transparency | 28.9 |
| Developer ergonomics | 78.6 |
| Access clarity | 44.7 |

**Agent readiness 56.6** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | yes |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 36.6** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/insforge/](https://apis.io/providers/insforge/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Insforge: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/insforge/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
