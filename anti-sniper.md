# Anti-sniper fee

Meteora and EVM launches start with an anti-sniper fee: **90%** at launch, stepping down every second to the coin's tax over the first **15 seconds**.

A bot buying right after launch pays most of its buy as a fee. Buys and sells pay the same rate.

Pump.fun and Raydium LaunchLab launches have no such fee.

## The line

The fee falls in a straight line, one step per whole second:

```
rate = 90% − (90% − tier) × seconds since launch / 15
```

On a 1.25% coin:

| Second | Rate |
| --- | --- |
| 0 | 90.00% |
| 3 | 72.25% |
| 6 | 54.50% |
| 9 | 36.75% |
| 12 | 19.00% |
| 14 | 7.17% |
| 15 | 1.25% |

## The first buy

A launcher's first buy, in the launch itself, skips it and pays the tier.

## Who gets the surplus

| Where | What happens |
| --- | --- |
| Meteora | The pool's fee splits in fixed shares, so the surplus splits the same way as the tax |
| EVM chains | The coin still gets 70% of its tier on the trade. Everything above the tier goes to Just Stealth It |

On EVM chains, this stops a launcher profiting from sniping their own coin. At the top tier in the window's last second, the closest it comes, a self-snipe pays 11.37% and gets 4.025% back.

On EVM chains the sniper fee is a compiled constant. The admin can't change it.

## Timing

On EVM chains, the block timestamp decides each step. On Robinhood Chain, the sequencer sets those timestamps.

Next: [Marketing ladder](marketing.md)
