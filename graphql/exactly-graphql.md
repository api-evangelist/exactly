# Exactly Protocol GraphQL API (The Graph Subgraph)

## Overview

Exactly Protocol provides a GraphQL subgraph API powered by The Graph, enabling developers to query indexed on-chain event data from the Exactly Protocol lending protocol deployed on Ethereum mainnet and Optimism. The subgraph is also mirrored via Goldsky.

**Schema source: Real schema retrieved from the official [exactly-finance/subgraph](https://github.com/exactly-finance/subgraph) GitHub repository.**

## Endpoints

### The Graph Decentralized Network

- **Ethereum Mainnet Subgraph:** https://thegraph.com/explorer/subgraphs/As6Xz6GCvbW8B9Xb7Rx2LqQeJcL3FcUyD8Tk95L8rG5d
- **Optimism Subgraph:** https://thegraph.com/explorer/subgraphs/9jpa2F3ZuirB11m3GL36wcNoNGETd3Z2zf7Cre5iwyeC

### Goldsky Mirror

- **Goldsky Endpoint (v1.3.12):** https://api.goldsky.com/api/public/project_clu2walwem1qm01w40v3yhw7y/subgraphs/exactly/1.3.12/gn

## Documentation

- **Subgraph Documentation:** https://docs.exact.ly/guides/the-graph.md
- **GitHub Repository:** https://github.com/exactly-finance/subgraph

## Schema Summary

The subgraph indexes on-chain events from the Exactly Protocol smart contracts and exposes the following entity types:

### Core Market Entities

| Entity | Description |
|---|---|
| `Market` | Core market entity with interest rate model parameters, pool state, and configuration |
| `FixedPool` | A fixed-rate maturity pool within a market (market + maturity timestamp) |
| `Account` | A user account's position within a specific market (address + market pair) |
| `FixedPosition` | A user's fixed-rate deposit or borrow position at a specific maturity |
| `MarketState` | Historical snapshots of market state for time-series analytics |
| `FixedPoolState` | Historical snapshots of fixed pool state |

### Variable-Rate (Floating) Event Entities

| Entity | Description |
|---|---|
| `Deposit` | Variable-rate deposit event (ERC-4626 style, assets and shares) |
| `Withdraw` | Variable-rate withdrawal event |
| `Borrow` | Variable-rate borrow event |
| `Repay` | Variable-rate repayment event |
| `Transfer` | Share transfer between addresses |

### Fixed-Rate (Maturity Pool) Event Entities

| Entity | Description |
|---|---|
| `DepositAtMaturity` | Fixed-rate deposit at a specific maturity with fee |
| `WithdrawAtMaturity` | Fixed-rate withdrawal from a maturity pool |
| `BorrowAtMaturity` | Fixed-rate borrow at a specific maturity with fee |
| `RepayAtMaturity` | Fixed-rate repayment covering debt at a maturity |

### Liquidation Entities

| Entity | Description |
|---|---|
| `Liquidate` | Liquidation event with collateral market and seized asset amounts |
| `Seize` | Asset seizure during a liquidation |

### Configuration and Parameter Change Entities

| Entity | Description |
|---|---|
| `InterestRateModelSet` | Interest rate model parameter updates (curve A/B, max utilization, natural rate, etc.) |
| `AdjustFactorSet` | Collateral adjust factor changes per market |
| `LiquidationIncentiveSet` | Liquidation incentive fee configuration changes |
| `PriceFeedSet` | Price feed oracle address changes per market |
| `MaxFuturePoolsSet` | Maximum number of future fixed-rate pools setting |
| `PenaltyRateSet` | Penalty rate for overdue fixed-rate positions |
| `ReserveFactorSet` | Reserve factor configuration |
| `BackupFeeRateSet` | Backup fee rate setting |
| `EarningsAccumulatorSmoothFactorSet` | Earnings accumulator smooth factor setting |
| `TreasurySet` | Treasury address and fee rate configuration |
| `RewardsControllerSet` | Rewards controller contract address per market |

### Market Listing and Access Entities

| Entity | Description |
|---|---|
| `MarketListed` | Event when a market is listed in the Auditor |
| `MarketEntered` | Event when an account enables a market as collateral |
| `MarketExited` | Event when an account disables a market as collateral |

### State Update Entities

| Entity | Description |
|---|---|
| `MarketUpdate` | Market-level state updates (floating assets, borrow shares, earnings accumulator) |
| `FixedEarningsUpdate` | Unassigned earnings update for a fixed-rate maturity pool |
| `FloatingDebtUpdate` | Floating debt utilization update |
| `AccumulatorAccrual` | Earnings accumulator accrual event |

### Rewards Distribution Entities

| Entity | Description |
|---|---|
| `Config` | Rewards distribution configuration (target debt, distribution period, allocation weights) |
| `DistributionSet` | Event when a reward distribution is configured |
| `IndexUpdate` | Reward index update for borrow and deposit tracking |
| `RewardsClaim` | Individual reward claim event |
| `AccountClaim` | Aggregate claim amount per account and reward token |
| `RewardAmountNotified` | EXA staking reward amount notification |
| `StakingSharedFee` | Shared fee accrued in the EXA staking contract |

### Governance / Timelock Entities

| Entity | Description |
|---|---|
| `TimelockControllerOperation` | Individual call within a timelock operation |
| `TimelockControllerCall` | A batched timelock governance call with scheduling, cancellation, and execution state |
| `TimelockControllerMinDelaySet` | Timelock minimum delay change event |

## Example Queries

### Query all markets

```graphql
{
  markets {
    id
    address
    assetSymbol
    symbol
    floatingAssets
    floatingDebt
    adjustFactor
    interestRateModel
    maxFuturePools
    penaltyRate
    reserveFactor
  }
}
```

### Query a user's account positions

```graphql
{
  accounts(where: { address: "0xYOUR_ADDRESS" }) {
    id
    address
    market
    borrowShares
    depositShares
    isCollateral
    fixedPositions {
      maturity
      principal
      fee
      borrow
      rate
    }
  }
}
```

### Query recent liquidations

```graphql
{
  liquidates(orderBy: timestamp, orderDirection: desc, first: 10) {
    id
    market
    borrower
    receiver
    assets
    collateralMarket
    seizedAssets
    timestamp
  }
}
```

### Query fixed-rate borrows at a specific maturity

```graphql
{
  borrowAtMaturities(
    where: { maturity: 1704067200 }
    orderBy: timestamp
    orderDirection: desc
    first: 20
  ) {
    id
    market
    borrower
    assets
    fee
    maturity
    timestamp
  }
}
```

### Query reward distributions

```graphql
{
  configs {
    id
    market
    reward
    start
    distributionPeriod
    targetDebt
    totalDistribution
    borrowAllocationWeightFactor
    depositAllocationWeightFactor
  }
}
```

## Key Protocol Design Reflected in the Schema

1. **Dual rate system:** The schema cleanly separates variable-rate operations (`Deposit`, `Borrow`, `Repay`, `Withdraw`) from fixed-rate maturity pool operations (`DepositAtMaturity`, `BorrowAtMaturity`, `RepayAtMaturity`, `WithdrawAtMaturity`).

2. **Interest rate model:** The `InterestRateModelSet` entity captures the full non-linear interest rate curve parameters for both floating and fixed markets, including sigmoid speed, growth speed, natural utilization, and spread factor.

3. **ERC-4626 vault design:** Variable-rate positions use shares-based accounting (assets and shares fields), reflecting the ERC-4626 vault standard.

4. **Rewards system:** A comprehensive rewards tracking schema covers distribution configuration, per-block index updates, and cumulative claim tracking for the EXA governance token rewards.

5. **Governance timelock:** The subgraph indexes the TimelockController used for protocol governance, tracking scheduled, cancelled, and executed governance operations.
