# Stealth BC and Stealth AMM

> **Coming soon.** Neither program is deployed or audited, and neither has a program id yet. Ids are published at launch.
>
> Today, Solana coins launch on Pump.fun, Raydium LaunchLab and Meteora. Nothing on this page changes that.

Just Stealth It has no program of its own on Solana today. Two are on the way.

| Program | What it is | Repository |
| --- | --- | --- |
| **Stealth BC** | Just Stealth It's own bonding curve. A coin trades on it until the curve sells out, then graduates | [Solana-BC](https://github.com/juststealthit/Solana-BC) |
| **Stealth AMM** | Just Stealth It's own automated market maker. One coin / SOL pool per coin, its liquidity locked for good | [Solana-AMM](https://github.com/juststealthit/Solana-AMM) |

Both repositories hold the design and a code shell. The curve and fee math is written and tested. The rest isn't finished.

## Where a coin graduates

The creator picks at launch where the coin graduates. The choice is locked and shown on the coin's page from the first second.

| Destination | Pool |
| --- | --- |
| **Stealth AMM** (the default) | A Stealth AMM pool |
| **Raydium** | Raydium CPMM |
| **PumpSwap** | Pump.fun's AMM |
| **Meteora** | Meteora DAMM v2 |

## What's planned to change

| | Solana today | With Stealth BC |
| --- | --- | --- |
| The curve | Pump.fun, Raydium LaunchLab or Meteora | Just Stealth It's own program |
| Where a coin graduates | Fixed by the venue | Picked by the creator |
| The fee split on the curve | Depends on the venue | 70 / 30 of the tier on every tier |
| Anti-sniper fee | Meteora only | Every coin |

The supply, the tax tiers, the launch types and the first-buy rule stay the same as on the rest of these pages.

On the Stealth AMM, the plan is that a coin keeps its tax tier and its launch type after graduation, the way an EVM coin does. On Raydium, PumpSwap and Meteora, the venue's own fee rules take over after graduation.

The numbers in the two repositories are defaults and can change before launch. They describe a design, not a live product.

Just Stealth It is not affiliated with Pump.fun, Raydium or Meteora.

Next: [Safety and trust](safety.md)
