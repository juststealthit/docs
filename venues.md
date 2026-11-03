# Venues

A venue is where a coin launches. You pick it at launch.

| Venue | Pairs | Tax | Anti-sniper | After graduation |
| --- | --- | --- | --- | --- |
| **Pump.fun** | SOL, or what Pump lists | Pump's own fee | No | PumpSwap pool |
| **Raydium LaunchLab** | All of Raydium's pairs | 1.25% to 5.75% | No | Raydium CPMM pool |
| **Meteora** | 20 shared pairs, or a token you search for | 1.25% to 5.75% | Yes | Meteora DAMM v2 pool |
| **Robinhood Chain** | ETH | 1.25% to 5.75% | Yes | Same pool, from launch |
| **HyperEVM** | HYPE | 1.25% to 5.75% | Yes | Same pool, from launch |
| **Base** | ETH | 1.25% to 5.75% | Yes | Same pool, from launch |
| **Arc** | USDC | 1.25% to 5.75% | Yes | Same pool, from launch |
| **BNB Chain** | BNB | 1.25% to 5.75% | Yes | Same pool, from launch |

Avalanche, Arbitrum and X Layer show as coming soon in the launch list. Just Stealth It's own Solana curve and pool are coming soon too. See [Stealth BC and Stealth AMM](stealth-bc-amm.md).

## Pump.fun

The default while it's on. A coin pairs with SOL or what Pump lists: USDC, tokenized stocks, wrapped majors and other pump coins. There are no tax tiers. Pump sets its own fee and can change it. On pairs where Pump allows it, you set the coin's creator fee at launch, for good.

The coin moves into a PumpSwap pool at graduation, which Pump's own program runs.

## Raydium LaunchLab

The default otherwise. Every pair Raydium has a config for: SOL, stablecoins, tokenized stocks (xStocks such as SPYx) and listed tokens. Five tax tiers from 1.25% to 5.75%, which include Raydium's 0.25% protocol fee.

The coin moves into a Raydium CPMM pool at graduation, and its LP is locked forever.

## Meteora

Meteora's Dynamic Bonding Curve. It has 20 shared pairs on the default 1.25% rate. Any other rate, or another token you search for, makes that coin's own config for about 0.006 SOL.

Shared pairs: SOL, USDC, USDT, USD1, ANSEM, BOME, TRX, cbBTC, ZEC, Fartcoin, ETH, BP, $WIF, TRUMP, MET, CARDS, PENGU, STONK, USELESS and HYPE.

Tokenized stocks and tokens with extra Token-2022 extensions can't launch here yet. They can on Raydium LaunchLab.

Meteora is the only venue with the optional [Global tax](fees.md#global-tax), which is built and currently off.

The coin moves into a Meteora DAMM v2 pool at graduation, and its liquidity is locked forever.

## EVM chains

Robinhood Chain, HyperEVM, Base and Arc run on Uniswap v4. BNB Chain runs on PancakeSwap Infinity. The source is the same for all five.

There's no migration. The pool exists from launch, its liquidity can't be removed, and graduation is a price level. The pair is the chain's native coin. On Arc that's USDC.

See [EVM chains](evm-chains.md).

## Which should I pick?

| You want | Look at |
| --- | --- |
| Pump's audience and flow | Pump.fun |
| The widest choice of pairs, stocks included | Raydium LaunchLab |
| The coin to keep a larger share at higher tax tiers on Solana | Meteora |
| An anti-sniper fee on Solana | Meteora |
| Liquidity locked from the first block | An EVM chain |
| The largest coin share of any tier | An EVM chain |

The last row compares percentages only. What a coin earns depends entirely on trading.

Next: [Bonding curve and graduation](curve-and-graduation.md)
