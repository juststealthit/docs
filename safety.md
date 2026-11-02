# Safety and trust

A wallet you connect stays yours: you sign its transactions and Just Stealth It never sees its keys. Each coin's venue, pair, tax and launch type are set at launch.

## What Just Stealth It can't do

- **Mint coins.** Supply is fixed at 1,000,000,000.
- **Change a coin's tax or launch type after launch.**
- **Pull the liquidity** of a graduated Raydium LaunchLab or Meteora coin, or of an EVM coin. It's locked forever, though Just Stealth It can collect the fees on its locked positions. A Pump.fun coin's pool is run by Pump's own program.
- **Stop a coin trading on chain.** It can hide a coin from its own lists, and that's all.

## What it can do

- **Control each coin's escrow.** It acts on the escrow by the coin's launch type: paying people, buying and burning, or adding liquidity.
- **Apply launch types with its bot.** Most of a launch type is applied by the bot, not enforced on chain. Pump.fun's split and the EVM contracts' split are locked on chain.
- **Move a coin's creator fees to a new wallet,** only through a [CTO](cto.md), after a public notice during which it can be cancelled.
- **Change launch settings,** such as the tiers on offer, for future launches only.
- **Move the funds in a Social vault,** because it holds the keys. Nothing does that on a timer: fees wait with no deadline.

## Keys it holds

Just Stealth It holds keys for Telegram wallets, hidden wallets, Social vaults, Auto Liquidity wallets and every coin's escrow. What sits there depends on its systems and security.

## EVM roles

| Role | Can | Can't |
| --- | --- | --- |
| Factory admin | Change future-launch settings within compiled caps, list quotes, pause new launches, replace the distributor and creator manager, rotate the two payout wallets, cancel a takeover | Touch a live token, its tier, its liquidity or its launch type. Change the tiers or the sniper fee |
| Distributor (ops bot) | Pay a Holders or Pot coin's pot to any address, and spend a Buyback coin's pot on `buyback` | Touch any other balance, or withdraw a Buyback pot to an address |
| Creator manager | Propose a takeover, with notice | Take effect without the notice and the new creator's acceptance |
| Creator | Claim its balance on a Creator coin, and hand the role over | Change the tier, the type or the split |
| Team wallet | Claim its share | Move its share to another address |
| Anyone | Sweep to the two payout wallets, launch | Choose where a sweep pays |

**The distributor is the main trust point.** A compromised key can pay a Holders or Pot pot to any address, up to all of it, and can spend a Buyback pot at a bad price. The loss is bounded by the pots.

## Audit

**Unaudited.** The EVM contracts haven't been audited, and Just Stealth It claims no independent audit of its servers, bots or fee logic.

## How far this has been tested

Every launch type ran on all three Solana venues on Solana's devnet. Devnet isn't mainnet, so that shows our code and the venues' test deployments work together, and no more. All coins in the final check matched the ledger to the lamport.

The EVM contracts have unit, fork, differential and invariant tests on both builds.

Not proven in that run:

- Anything through Jupiter: Auto Liquidity's buy, buy-backs and Feed a Coin after graduation, and Feed a Coin on third-party coins
- Payouts to other chains
- Non-SOL pairs
- Jito bundles
- The Global tax
- EVM chains
- Real social sign-in for claims
- Raydium tiers above 1.25% in trading
- Auto Liquidity's burn after 30 days

No job claims pool LP fees yet on the Meteora pot position or on Raydium's Fee Key.

## Support and safety

Reach the team through the form on [juststealthit.xyz/status](https://juststealthit.xyz/status). Automated accounts on X and Telegram aren't support. **Nobody from Just Stealth It will ever ask for your recovery phrase.**

Next: [Addresses](addresses.md)
