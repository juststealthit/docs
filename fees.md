# Fees and tax tiers

Every buy and sell pays the coin's fee, taken in the pair token. On Pump.fun that's Pump's own fee. On Raydium LaunchLab, Meteora and EVM chains it's the coin's **tax**, set at launch. The venue's program or contract charges it, so it's the same on juststealthit.xyz and anywhere else the coin trades.

## The two parts

Every coin's fee has two parts: **30** goes to Just Stealth It and **70** goes to the coin's launch type.

Launch flows and token pages only show the launch type's part, called **creator fees**. 100% of creator fees go where the launch type says. That never means 100% of the tax.

The venue's own cut comes first where it has one. Raydium is the exception to 70 / 30, explained below.

## All rates at a glance

What a coin gets of each trade, on the curve:

| Tier | EVM chains | Meteora | Raydium LaunchLab |
| --- | --- | --- | --- |
| 1.25% | 0.875% | 0.70% | 0.50% |
| 2.25% | 1.575% | 1.26% | 0.50% |
| 3.25% | 2.275% | 1.82% | 0.50% |
| 4.25% | 2.975% | 2.38% | 0.50% |
| 5.75% | 4.025% | 3.22% | 0.50% |

Pump.fun has no tiers. Fees depend entirely on trading. A coin nobody trades earns nothing.

## Pump.fun

Pump sets the fee itself and can change it, by market cap, from its own live config. Part of it is Pump's **creator fee**. Every launch locks how that part is shared, on chain and for good:

| Share of Pump's creator fee | Goes to |
| --- | --- |
| 70% | The coin's escrow |
| 30% | Just Stealth It |

Pump won't distribute a coin's creator fee until the coin has earned a minimum, which Pump sets and changes. It was about 0.0039 SOL on the coin we tested. A low-volume coin can wait a long time for its first payout.

## Raydium LaunchLab

Raydium's curve caps the creator fee at **0.5%**, so 70 / 30 can't be exact here. The coin gets 0.5% of each trade on every tier. Just Stealth It keeps the rest of the tax, after Raydium's own 0.25%.

| Tier | Raydium | Just Stealth It | Coin | Coin's share of the split |
| --- | --- | --- | --- | --- |
| 1.25% | 0.25% | 0.50% | 0.50% | 50% |
| 2.25% | 0.25% | 1.50% | 0.50% | 25% |
| 3.25% | 0.25% | 2.50% | 0.50% | 16.7% |
| 4.25% | 0.25% | 3.50% | 0.50% | 12.5% |
| 5.75% | 0.25% | 5.00% | 0.50% | 9.1% |

Higher tiers add only to Just Stealth It's share.

After graduation the Raydium CPMM pool charges its own fee:

| Launch tier | Pool fee | To the LP | To the coin |
| --- | --- | --- | --- |
| 1.25% | 1.25% | 0.75% | 0.50% |
| All others | 1.50% | 0.70% | 0.80% |

## Meteora

Meteora keeps 20% of the pool fee. The rest splits 70 / 30 on every rate.

| Tier | Meteora | Just Stealth It | Coin | Own config? |
| --- | --- | --- | --- | --- |
| 1.25% | 0.25% | 0.30% | 0.70% | Shared |
| 2.25% | 0.45% | 0.54% | 1.26% | About 0.006 SOL |
| 3.25% | 0.65% | 0.78% | 1.82% | About 0.006 SOL |
| 4.25% | 0.85% | 1.02% | 2.38% | About 0.006 SOL |
| 5.75% | 1.15% | 1.38% | 3.22% | About 0.006 SOL |

After graduation the coin trades in a Meteora DAMM v2 pool that keeps the coin's rate, capped at 10% by Meteora. That fee goes to the LP, not to creator fees. See [Graduation](curve-and-graduation.md#graduation).

The [anti-sniper fee](anti-sniper.md) splits the same way, because the pool's shares are fixed.

## EVM chains

A coin pays one tier on every trade, before and after graduation. The pool's own LP fee is 0, because the hook takes the tax. The DEX's owner can switch on a protocol fee: up to 0.1% per direction on Uniswap v4, and up to 0.4% on PancakeSwap Infinity. It's a cut of the pool, separate from these books.

| Tier | Coin (70%) | Just Stealth It (30%) |
| --- | --- | --- |
| 1.25% | 0.875% | 0.375% |
| 2.25% | 1.575% | 0.675% |
| 3.25% | 2.275% | 0.975% |
| 4.25% | 2.975% | 1.275% |
| 5.75% | 4.025% | 1.725% |

This split is written in the contract and is locked. Everything a trade pays above the tier, which is the anti-sniper fee, goes to Just Stealth It, so a launcher gains nothing by sniping their own coin.

## The coin's escrow

Creator fees land in the coin's own **escrow**, which Just Stealth It controls. On EVM chains they land in the contract's fee vault. Just Stealth It's bot claims them and acts on them by the coin's launch type. Claims under about 0.001 SOL are left for a later run.

## Payouts

| Launch type | How it pays |
| --- | --- |
| Creator, Wallet, Team | To the addresses set at launch, in the pair token. Nothing to claim on Solana |
| Social | Waits in the person's vault until they claim it |
| Holders, Diamond Hands | Every 10 minutes to qualifying holders, in the pair token. Nothing to claim |
| Buy back and burn, Feed a Coin | Spent on buying a coin each time fees are claimed. What it buys is burned |
| Auto Liquidity | Builds up in the coin's own wallet, then goes into its pool |
| Marketing | Sent to the marketing wallet, which pays for the coin's [ladder](marketing.md) |

## Global tax

Built and off for now. A Meteora launch on a SOL pair could add a Token-2022 transfer fee of 0.5%, 1%, 2%, 3% or 5%, locked at launch. It applies to every transfer of the coin, wallet to wallet included. It doesn't work with Auto Liquidity. Pump.fun, Raydium LaunchLab and EVM coins can't have one.

## Other costs

- **Launch costs:** see [Launching](launching.md#what-a-launch-costs).
- **Relay's fee:** moving money between chains costs Relay's fee. You see it before you pay.
- **Network fees:** you always need a little of the chain's coin.

Just Stealth It adds no separate fee to a trade on top of the coin's tax.

## Trading fees

There is **no trading fee from Just Stealth It** today: not on coins launched here, beyond their own tax above, and not on [external coins](external-tokens.md), where you pay only the route's and the network's costs.

A trading fee will be introduced later, to fund referral rewards and callouts, which are being built now. This page will show it.

Next: [Launch types](launch-types.md)
