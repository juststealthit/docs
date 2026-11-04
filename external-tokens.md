# External tokens

Just Stealth It also shows coins that didn't launch here: the coins trending right now on Solana and the other chains we run. They sit next to the coins launched on Just Stealth It, and you can trade them from the same page.

This page explains how they get in and how trading them works. It is an explanation, not a recommendation. See [Not advice](#not-advice).

## Where they show

| Place | What you see |
| --- | --- |
| **Coins → All** | External coins mixed in with ours. The chain filter works on them too |
| **Trending** | The Feed's Trending column and side card, and the ticker on Coins |
| **New, Graduating, Graduated** | Never. These lists are for coins launched on Just Stealth It only |

Solana comes first. Other chains add a few coins each, so the lists stay mostly Solana.

### Telling them apart

On Coins and in the Feed, every coin shows where it comes from, in the spot beside its ticker:

| Mark | Meaning |
| --- | --- |
| The Stealth logo | Launched on Just Stealth It |
| A launchpad's logo | An external coin, with the logo of the launchpad it came from (Pump.fun, Bonk, Four.meme, Clanker, Zora and more) |
| No mark | An external coin from a launchpad we don't have a logo for |

The chain's logo sits on the coin's picture, as it does for our own coins.

## How coins are picked

We fetch the data on chain and keep the list fresh through the day. A coin only makes it in if it passes metrics we've chosen to filter out as much nonsense as possible. Coins that look thin, tiny or easy to pull drop out, and a coin that stops passing leaves the list.

These checks remove a lot of noise. They don't catch everything, and they don't make a coin safe.

## The coin page

An external coin opens a page laid out like the page of a coin launched here: header, chart, figures and the trade form.

| Part | What it shows |
| --- | --- |
| Header | Price, market cap, 24h change, liquidity, volume, holders and the share held by the top 10. The bar under it shows whether the coin is still on its launchpad's curve or has graduated |
| Chart | The coin's history, from its launch where it's available. Opens on 1 minute candles |
| Info | Market figures: all-time high, buys and sells, holder spread, smart wallets |
| Creator fees | Shown when the coin shares its creator fees and we can see how |
| Dev | The launcher's other coins, on Solana |

External coins have no Activity or Holders tab.

## Trading

You sign every trade in your own wallet. Just Stealth It never holds your money or your coins.

| Coin on | Pay with | Routed by | Coins arrive in |
| --- | --- | --- | --- |
| Solana | SOL | Jupiter, across Solana's pools | Your Solana wallet |
| Another chain | SOL from your Solana wallet | Relay, which swaps across chains for you | Your EVM wallet |
| Another chain | That chain's coin, from your EVM wallet | Relay | Your EVM wallet |

Selling works the same way back. A Solana coin sells through Jupiter for SOL. A coin on another chain sells from your EVM wallet, for that chain's coin or for SOL in your Solana wallet.

Every quote shows what you'll receive, the worst case your slippage allows, the route and its costs before you sign. Your slippage and buy amounts are the same settings as for any other trade.

On phones, the Buy and Sell bar stays at the foot of the page and opens the trade form in a sheet, as on any coin's page.

To receive a coin on another chain you need an EVM wallet connected. Sending them to the EVM wallet built into your Just Stealth It account is coming next.

## Fees

There is **no trading fee from Just Stealth It** on external coins. You pay only what the trade costs to make: the pools' own fees, Relay's fee when it crosses chains, and network fees. Each is in the quote before you sign.

A trading fee will be introduced later, to fund referral rewards and callouts, which are being built now.

Launching a coin and the creator fees of coins launched here are unchanged. See [Fees](fees.md).

## Not advice

External coins aren't launched on Just Stealth It, and nobody here checks the people behind them. Our filters and mechanisms don't guarantee anything about a coin, its price or its liquidity. A coin that passes today can lose everything tomorrow.

This page explains how things work. Nothing here is financial advice or a promise of any return. Do your own research, and only put in what you can lose.

Next: [Trading](trading.md)
