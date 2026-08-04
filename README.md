# Exactly Protocol (exactly)

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

Exactly Protocol is a decentralized, non-custodial, open-source protocol providing autonomous fixed and variable interest rate credit markets on Ethereum, Optimism, and Base. It enables users to deposit and borrow crypto assets at both variable rates and fixed rates through maturity pools, using a continuous non-linear interest rate model, dynamic close factor liquidations, and a rewards distribution system with the EXA governance token.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/apis.yml)

## Tags

- DeFi
- Lending
- Borrowing
- Fixed Rate
- Variable Rate
- Ethereum
- Optimism
- Base
- ERC-4626
- Credit Markets

## Timestamps

- **Created:** 2026-06-14
- **Modified:** 2026-06-14

## APIs

### Exactly Protocol Previewer API

Read-only smart contract interface for previewing deposits, borrows, withdrawals, and repayments across all market maturity pools. Returns projected yields, repayment amounts, and comprehensive account positions across all markets on Ethereum and Optimism without executing any transactions.

- **Human URL:** [https://docs.exact.ly/guides/periphery-contracts/previewer-read-only.md](https://docs.exact.ly/guides/periphery-contracts/previewer-read-only.md)
- **Base URL:** `https://app.exact.ly`

#### Tags

- Previewer
- Markets
- Maturity Pools
- User Positions
- Read-only

#### Properties

- [Documentation](https://docs.exact.ly/guides/periphery-contracts/previewer-read-only.md)
- [Plans](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/plans/plans.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/rate-limits/rate-limits.yml)
- [Graph Q L](graphql/exactly-graphql.md)

### Exactly Protocol Market API

ERC-4626-compliant smart contract interface for the core Market contract exposing view and write methods for depositing, borrowing, withdrawing, repaying, minting, redeeming, and liquidating positions at both variable and fixed rates. Includes account snapshots, debt previews, and floating asset calculations.

- **Human URL:** [https://docs.exact.ly/guides/protocol/market.md](https://docs.exact.ly/guides/protocol/market.md)
- **Base URL:** `https://app.exact.ly`

#### Tags

- Market
- ERC-4626
- Deposits
- Borrows
- Liquidations
- Variable Rate
- Fixed Rate

#### Properties

- [Documentation](https://docs.exact.ly/guides/protocol/market.md)
- [Plans](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/plans/plans.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/rate-limits/rate-limits.yml)

### Exactly Protocol Auditor API

Smart contract interface for the Auditor, the central risk management component that manages market listings, collateral factors, account liquidity checks, and liquidation eligibility. Provides methods to query all markets, compute account liquidity, calculate seizure amounts, and check liquidation conditions.

- **Human URL:** [https://docs.exact.ly/guides/protocol/auditor.md](https://docs.exact.ly/guides/protocol/auditor.md)
- **Base URL:** `https://app.exact.ly`

#### Tags

- Auditor
- Risk
- Collateral
- Liquidity
- Liquidations
- Markets

#### Properties

- [Documentation](https://docs.exact.ly/guides/protocol/auditor.md)
- [Plans](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/plans/plans.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/rate-limits/rate-limits.yml)

### Exactly Protocol RewardsController API

Smart contract interface for querying and claiming EXA and esEXA token rewards distributed to depositors and borrowers. Supports querying claimable rewards, reward configurations, distribution timelines, reward indexes, and claiming rewards across all market operations.

- **Human URL:** [https://docs.exact.ly/guides/protocol/rewardscontroller.md](https://docs.exact.ly/guides/protocol/rewardscontroller.md)
- **Base URL:** `https://app.exact.ly`

#### Tags

- Rewards
- EXA
- esEXA
- Distribution
- Governance

#### Properties

- [Documentation](https://docs.exact.ly/guides/protocol/rewardscontroller.md)
- [Plans](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/plans/plans.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/rate-limits/rate-limits.yml)

### Exactly Protocol Subgraph API (The Graph)

GraphQL subgraph API powered by The Graph for querying indexed on-chain data from Exactly Protocol on Ethereum mainnet and Optimism. Supports advanced queries including aggregation, filtering, relationships, and historical data for markets, user positions, maturity pools, borrowing rates, and protocol-wide statistics.

- **Human URL:** [https://docs.exact.ly/guides/the-graph.md](https://docs.exact.ly/guides/the-graph.md)
- **Base URL:** `https://api.thegraph.com`

#### Tags

- GraphQL
- Subgraph
- The Graph
- Historical Data
- Analytics
- Ethereum
- Optimism

#### Properties

- [Documentation](https://docs.exact.ly/guides/the-graph.md)
- [Graph Q L](https://thegraph.com/explorer/subgraphs/As6Xz6GCvbW8B9Xb7Rx2LqQeJcL3FcUyD8Tk95L8rG5d)
- [Graph Q L](https://thegraph.com/explorer/subgraphs/9jpa2F3ZuirB11m3GL36wcNoNGETd3Z2zf7Cre5iwyeC)
- [Plans](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/plans/plans.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/rate-limits/rate-limits.yml)

## Common Properties

- [Website](https://exact.ly)
- [Documentation](https://docs.exact.ly)
- [Git Hub](https://github.com/exactly)
- [Discord](https://discord.gg/exactly)
- [Twitter](https://twitter.com/exactlyprotocol)
- [Telegram](https://t.me/exactlyprotocol)
- [Medium](https://medium.com/exactly-protocol)
- [Terms of Service](https://exact.ly/terms)
- [Privacy Policy](https://exact.ly/privacy)
- [Bug Bounty](https://immunefi.com/bounty/exactly)
- [Status Page](https://exact.ly)
- [Governance](https://docs.exact.ly/governance/protocol-governance)
- [White Paper](https://docs.exact.ly/resources/white-paper)
- [Audits](https://docs.exact.ly/security/audits)
- [Smart Contracts](https://docs.exact.ly/guides/smart-contract-addresses.md)
- [Finops](https://raw.githubusercontent.com/api-evangelist/exactly/refs/heads/main/finops/finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
