# Penumbra Protocol - Fully Private Proof-of-Stake Network

## Overview

Penumbra is a fully private proof-of-stake network and decentralized exchange for the Cosmos ecosystem. It integrates privacy with proof-of-stake through a novel private delegation mechanism that provides staking derivatives, tax-efficient staking, and on-chain governance with private voting.

## Key Features

### Private Transactions

Penumbra records all value in a single multi-asset shielded pool based on the Zcash Sapling design, but allows private transactions in any kind of IBC asset. 

- Inbound IBC transfers shield value as it moves into the zone
- Outbound IBC transfers unshield value
- No notion of transparent transactions or transparent value pool
- The entire Cosmos ecosystem functions analogously to Zcash's transparent pool
- No account-based model - only validators have long-term identity

### Private Staking

Penumbra uses a novel mechanism that eliminates traditional staking rewards, treating unbonded and bonded stake as separate assets with an epoch-varying exchange rate.

**Key innovations:**
- Delegation tokens are fungible and represent shares of validator delegation pools
- First-class staking derivatives
- Delegators realize capital gains/losses on unbonding rather than income
- Privacy for delegators while maintaining accountability for validators
- Delegation tokens can be traded and transacted like any other token

**Benefits:**
- Privacy for delegations
- Flexibility for delegators
- Tax-efficient staking (capital gains vs. income)

### Private Governance

Unlike the Cosmos Hub, Penumbra's governance mechanism supports secret ballots:

- Anonymous proposal submission by escrowing bonded stake
- Stakeholders vote by proving ownership of bonded stake
- Votes encrypted to threshold key controlled by validator set
- Validators sum encrypted votes and decrypt only per-epoch totals
- Delegated voting supported

### Private DEX (ZSwap)

ZSwap allows users to privately swap between any pair of assets:

- **Sealed-bid batch auctions** - Prevents frontrunning and provides better execution
- **Concentrated liquidity** - Uniswap-v3-style positions created anonymously
- **Privacy-preserving** - Individual swaps burn input notes and privately mint output notes
- **Batch execution** - All swaps in each block executed in single batch
- **Anonymous liquidity provision** - Positions reveal liquidity amount and bounds but not identity

## Technical Architecture

- **Consensus:** Tendermint-based proof-of-stake
- **Privacy:** Zcash Sapling-based shielded pool
- **Interoperability:** IBC-compatible, connects to entire Cosmos ecosystem
- **DEX:** ZSwap with sealed-bid batch auctions and concentrated liquidity

## Use Cases

1. **Private cross-chain transactions** - Transact in any IBC asset with full privacy
2. **Tax-efficient staking** - Earn through capital appreciation rather than income
3. **Private trading** - Swap assets without revealing trading strategies
4. **Anonymous liquidity provision** - Provide liquidity without revealing positions
5. **Private governance** - Vote on proposals with secret ballots

## Resources

- Protocol Documentation: https://protocol.penumbra.zone/
- GitHub: https://github.com/penumbra-zone/penumbra
- Discord: https://discord.gg/hKvkrqa3zC
- Twitter: https://twitter.com/penumbrazone
