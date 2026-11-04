# Trading

Every trade is prepared for you and you approve it. On Solana you sign it in your wallet. On EVM chains a hidden wallet signs after your wallet signs for it. A wallet you connect stays yours.

## Where a coin trades

| Stage | Solana | EVM |
| --- | --- | --- |
| Before graduation | Its bonding curve: Pump.fun, Raydium LaunchLab or Meteora | Its pool |
| After graduation | PumpSwap, Raydium CPMM or Meteora DAMM v2 | The same pool |

These are standard programs and contracts, so the coin trades in other apps too, at the same fees.

## The quote

| Line | What it means |
| --- | --- |
| You receive | The quoted amount, with its dollar value |
| Tax | The coin's tax on this trade, in the pair token |
| Price impact | How far this trade moves the price |
| Min received | The worst case your slippage setting allows. If the price moves further, the trade is refused and nothing is spent |

## Settings

Slippage and the one-tap buy amounts are in the trade panel's settings. They're saved in this browser only.

On phones the trade sheet also has an **Instant** mode: preset buy amounts and sell percentages, one tap each. See [Trading on phones](token-page.md#trading-on-phones).

Perpetuals and spot on Hyperliquid, Jupiter and Aster are in their own section. See [Perps](perps.md).

## External coins

Trending coins from other launchpads trade from their own page. Solana coins go through Jupiter. Coins on other chains go through Relay, paid with SOL or with that chain's coin, and arrive in your EVM wallet. Just Stealth It takes no trading fee on them. See [External tokens](external-tokens.md#trading).

## Prices and PnL

Prices, charts and PnL are in the pair token and in US dollars. You always need a little of the chain's coin for network fees.

During a coin's first 15 seconds on Meteora or an EVM chain, the [anti-sniper fee](anti-sniper.md) applies to every trade but the launcher's first buy.

Next: [The token page](token-page.md)
