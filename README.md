# Exactly Protocol

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

Exactly Protocol is a decentralized, non-custodial, open-source protocol providing autonomous fixed and variable interest rate credit markets on Ethereum, Optimism, and Base. It enables users to deposit and borrow crypto assets at both variable rates and fixed rates through maturity pools, using a continuous non-linear interest rate model, dynamic close factor liquidations, and a rewards distribution system with the EXA governance token.

**Areas:** DeFi · Lending · Borrowing · Fixed Rate · Variable Rate · Ethereum · Optimism · Base · ERC-4626 · Credit Markets

## Exactly Protocol on APIs.io

Everything profiled for Exactly Protocol is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/exactly/](https://apis.io/providers/exactly/)** — or go straight to one of the APIs or properties below.

### APIs (17)

- [Exactly Protocol Previewer API](https://apis.io/apis/exactly/exactly-protocol-previewer-api/) — Read-only smart contract interface for previewing deposits, borrows, withdrawals, and repayments across all market maturity pools. Returns projected yields,…
- [Exactly Protocol Market API](https://apis.io/apis/exactly/exactly-protocol-market-api/) — ERC-4626-compliant smart contract interface for the core Market contract exposing view and write methods for depositing, borrowing, withdrawing, repaying,…
- [Exactly Protocol Auditor API](https://apis.io/apis/exactly/exactly-protocol-auditor-api/) — Smart contract interface for the Auditor, the central risk management component that manages market listings, collateral factors, account liquidity checks,…
- [Exactly Protocol RewardsController API](https://apis.io/apis/exactly/exactly-protocol-rewardscontroller-api/) — Smart contract interface for querying and claiming EXA and esEXA token rewards distributed to depositors and borrowers. Supports querying claimable rewards,…
- [Exactly Protocol Subgraph API (The Graph)](https://apis.io/apis/exactly/exactly-protocol-subgraph-api-the-graph/) — GraphQL subgraph API powered by The Graph for querying indexed on-chain data from Exactly Protocol on Ethereum mainnet and Optimism. Supports advanced…
- [Exactly Protocol ERC-4626 API](https://apis.io/apis/exactly/exactly-erc-4626-api/) — ERC-4626 vault standard methods
- [Exactly Protocol Fixed Rate API](https://apis.io/apis/exactly/exactly-fixed-rate-api/) — Fixed rate maturity pool operations
- [Exactly Protocol Liquidations API](https://apis.io/apis/exactly/exactly-liquidations-api/) — Liquidation eligibility and seizure calculations
- [Exactly Protocol Liquidity API](https://apis.io/apis/exactly/exactly-liquidity-api/) — Account liquidity and collateral checks
- [Exactly Protocol Market Management API](https://apis.io/apis/exactly/exactly-market-management-api/) — Write methods for market configuration (admin only)
- [Exactly Protocol Market State API](https://apis.io/apis/exactly/exactly-market-state-api/) — View methods for querying market state
- [Exactly Protocol Markets API](https://apis.io/apis/exactly/exactly-markets-api/) — Market listing and configuration queries
- [Exactly Protocol Previewer API](https://apis.io/apis/exactly/exactly-previewer-api/) — Read-only preview methods for Exactly Protocol markets
- [Exactly Protocol Reward Configuration API](https://apis.io/apis/exactly/exactly-reward-configuration-api/) — Reward program configuration and indexes
- [Exactly Protocol Rewards Claims API](https://apis.io/apis/exactly/exactly-rewards-claims-api/) — Write methods for claiming earned rewards
- [Exactly Protocol Rewards Query API](https://apis.io/apis/exactly/exactly-rewards-query-api/) — View methods for querying reward state and amounts
- [Exactly Protocol Variable Rate API](https://apis.io/apis/exactly/exactly-variable-rate-api/) — Floating/variable rate deposit and borrow operations

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Exactly Protocol GraphQL API (The Graph Subgraph)](https://apis.io/graphqls/exactly/exactly-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Exactly Agentic Access](https://apis.io/agentic-access/exactly/exactly-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [FixedPreview](https://apis.io/schemas/exactly/fixed-preview/)
- [MarketAccount](https://apis.io/schemas/exactly/market-account/)
- [RewardConfig](https://apis.io/schemas/exactly/reward-config/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Exactly Context](https://apis.io/jsonld/exactly/exactly-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Exactly Protocol Vocabulary](https://apis.io/vocabularies/exactly/exactly-vocabulary/)

#### Examples (3)

Example requests and responses.

- [Claim All Rewards](https://apis.io/examples/exactly/claim-all-rewards/)
- [Get Market Accounts](https://apis.io/examples/exactly/get-market-accounts/)
- [Preview Deposit At Maturity](https://apis.io/examples/exactly/preview-deposit-at-maturity/)

#### Collections (11)

Postman and Open Collection request collections.

- [Exactly Protocol Auditor ERC-4626 API](https://apis.io/collections/exactly/open-exactly-erc-4626-api/)
- [Exactly Protocol Auditor ERC-4626 Fixed Rate API](https://apis.io/collections/exactly/open-exactly-fixed-rate-api/)
- [Exactly Protocol Auditor ERC-4626 Liquidations API](https://apis.io/collections/exactly/open-exactly-liquidations-api/)
- [Exactly Protocol Auditor ERC-4626 Liquidity API](https://apis.io/collections/exactly/open-exactly-liquidity-api/)
- [Exactly Protocol Auditor ERC-4626 Market Management API](https://apis.io/collections/exactly/open-exactly-market-management-api/)
- [Exactly Protocol Auditor ERC-4626 Market State API](https://apis.io/collections/exactly/open-exactly-market-state-api/)
- [Exactly Protocol Auditor ERC-4626 Markets API](https://apis.io/collections/exactly/open-exactly-markets-api/)
- [Exactly Protocol Auditor ERC-4626 Reward Configuration API](https://apis.io/collections/exactly/open-exactly-reward-configuration-api/)
- [Exactly Protocol Auditor ERC-4626 Rewards Claims API](https://apis.io/collections/exactly/open-exactly-rewards-claims-api/)
- [Exactly Protocol Auditor ERC-4626 Rewards Query API](https://apis.io/collections/exactly/open-exactly-rewards-query-api/)
- [Exactly Protocol Auditor ERC-4626 Variable Rate API](https://apis.io/collections/exactly/open-exactly-variable-rate-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Exactly Protocol — jsonschema rules](https://apis.io/rules/exactly/exactly-jsonschema-spectral-rules/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Exactly Domain Security](https://apis.io/security/exactly/exactly-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Plans](https://apis.io/plans/exactly/plans/)

#### Rate limits (1)

Published request limits.

- [Rate Limits](https://apis.io/rate-limits/exactly/rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Finops](https://apis.io/finops/exactly/finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://exact.ly)
- [Documentation](https://docs.exact.ly)
- [Blog](https://medium.com/feed/@exactly_protocol)
- [Terms of service](https://exact.ly/terms)
- [Privacy policy](https://exact.ly/privacy)
- [Status](https://exact.ly)

## API Evangelist rating

**Kin Score 27.9** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 55.3 |
| Contract governance | 9.8 |
| Operational transparency | 21.1 |
| Developer ergonomics | 16.7 |
| Access clarity | 5.3 |

**Agent readiness 19.8** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 10.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/exactly/](https://apis.io/providers/exactly/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Exactly Protocol: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/exactly/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
