# Launching a coin

## Step by step

1. **Connect** a wallet with enough to pay for the launch.
2. **Coin details:** name, ticker, logo, description and links.
3. **Where it launches:** Pump.fun, Raydium LaunchLab, Meteora, Robinhood Chain, HyperEVM, Base, Arc or BNB Chain. See [Venues](venues.md).
4. **Pair:** what your coin trades against. See [Pairs](curve-and-graduation.md#pairs).
5. **Tax:** 1.25%, 2.25%, 3.25%, 4.25% or 5.75% on Raydium LaunchLab, Meteora and EVM chains. Pump.fun sets its own fee. See [Fees](fees.md).
6. **Launch type:** where creator fees go. Some types ask for more: a social account, an address, team wallets, a coin to feed, or a set of slices. See [Launch types](launch-types.md).
7. **Singular or Multi-chain:** this sits under the launch types. Singular makes one coin where you picked. Multi-chain makes a separate coin on each chain. See [Multi-chain launches](multi-chain.md).
8. **First buy (optional):** made together with the launch, up to 5% of the supply.
9. **Review and sign.** The token page opens when the launch confirms.

## The logo

Upload a PNG, JPG, WebP or GIF of up to 2 MB, or paste an image link. A square image looks best.

## What a launch costs

| Cost | When |
| --- | --- |
| Network fees and account rent | Always. A small amount of the chain's coin |
| Your first buy | If you make one |
| Gas and Relay's fee | On EVM chains from a Solana wallet. The quote shows them, and the review shows the real total |
| About 0.01 SOL added to the coin's escrow | A coin that keeps a pot on a pair other than SOL. It pays for the coin's own transactions |
| About 0.006 SOL for a Meteora config | When the token has no shared config, or the rate isn't the default 1.25% |

The EVM contracts can charge a launch fee in the native coin, capped at 0.1. It's 0 on all five chains today.

## What's locked at launch

- Venue and pair
- Tax tier
- Launch type
- Team wallets, on a Team coin
- On EVM: max wallet, max buy, and any first-buy lock

Nobody can change these afterwards, the launcher and Just Stealth It included. The one exception is who receives creator fees after a [CTO](cto.md), which runs through a public notice.

On Solana, the launch type is stored with the coin and applied by Just Stealth It's bot. On chain, only Pump.fun's split and the EVM contracts' split are locked. See [Safety and trust](safety.md).

## EVM launch options

The EVM contracts also support these terms, fixed at launch:

| Option | Range |
| --- | --- |
| Max wallet | 0.5% to 5% of supply, for up to 60 minutes |
| Max buy per transaction | 0.1% to 5% of supply, for up to 60 minutes |
| First-buy lock | Up to 90 days |

Next: [Venues](venues.md)
