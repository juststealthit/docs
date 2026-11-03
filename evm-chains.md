# EVM chains

Just Stealth It launches and trades on five EVM chains. Avalanche, Arbitrum and X Layer show as coming soon in Connect, on Coins and in the launch list. Nothing launches or trades on them yet.

| Chain | Id | Gas and pair | DEX |
| --- | --- | --- | --- |
| Robinhood Chain | 4663 | ETH | Uniswap v4 |
| HyperEVM | 999 | HYPE | Uniswap v4 |
| Base | 8453 | ETH | Uniswap v4 |
| Arc | 5042 | USDC | Uniswap v4 |
| BNB Chain | 56 | BNB | PancakeSwap Infinity |

> **The contracts are unaudited.** On Holders and Pot coins, our bot's key can pay a pot to any address: nothing on chain checks who a pot is for. Our ledger keeps the bot honest, and it wouldn't stop a stolen key.

The contracts are on all five chains. Every address is in [Addresses](addresses.md), and the source is in [smart-contracts](https://github.com/juststealthit/smart-contracts).

## Who can do what

An EVM wallet can sign in, post and pay for a [multi-chain launch](multi-chain.md). Launching, buying and selling on these chains otherwise run from a Solana wallet, through a hidden wallet.

## Hidden wallets

You get one per Solana wallet, with the same address on every EVM chain. It's created the first time you use one, after you prove your wallet. **Just Stealth It holds its key.**

- It signs only set actions: launch, buy, approve, sell, claim and a Relay deposit. None of them can pay a free address.
- For a launch or a buy you pay SOL, and Relay moves it across. Nothing goes on chain until Relay reports the funds arrived, so a failed launch or buy leaves the money in the sub wallet.
- Sale proceeds stay in the sub wallet until you withdraw. A withdrawal pays only the Solana wallet that signed it, through Relay.
- Creator claims land in your sub wallet too.

| Default limit | Amount |
| --- | --- |
| One request | $50 |
| Rolling 24 hours | $200 |

## How a launch works

Every launch deploys a token and opens its pool in one transaction. The whole supply is locked in two positions shaped like a bonding curve.

| Part | What it does |
| --- | --- |
| Factory | Launches tokens |
| Token | A small clone with its name and terms in its own bytecode |
| Locker | Opens the pool, runs the first buy, and owns the liquidity forever |
| Hook | Takes the tax, the sniper fee and the max buy, and allows no other liquidity |
| Fee vault | Books every fee per coin, and pays claims, pots and burns |
| Router | The site's thin swap router |

There's no migration. Nothing can remove the liquidity, and the pool trades on any route of its DEX from the first block.

## Claiming

A creator's balance sits in the fee vault until it's claimed. A claim pays only the claimant. Team wallets claim their own share, and a rejecting wallet hurts only itself.

## Things to know

- **Arc's gas coin is USDC.** Targets there are in dollars. Circle can block an address, which stops native USDC too.
- **Scanners read clones as proxies.** Token-risk tools may flag `is_proxy`. The token isn't upgradeable.
- **Tax-free side pools exist.** Anyone can open a plain pool for a coin without the hook.
- **Rollup data costs.** On Robinhood Chain, a transaction pays for L1 data on top of L2 gas.
- **The DEX's owner** has its own powers. PancakeSwap's can pause swaps and liquidity on BNB Chain.

Next: [Trading](trading.md)
