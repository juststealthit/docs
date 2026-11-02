# Multi-chain launches

One payment makes one launch on each chain: your Solana venue, unless you leave it out, and every EVM chain that can take it. The flow says which chains are left out and why.

**These are separate coins.** Each has its own address, its own 1,000,000,000 supply, its own price, pool and holders. They aren't bridged, and one can't be swapped for another. The Coins list folds them into one row and the token page has a tab per chain, and neither adds their numbers together.

## How it runs

1. **Home** is the chain that pays. A Solana wallet pays from Solana, and an EVM wallet pays from its chain. Hidden wallets, which Just Stealth It holds, do the rest.
2. **Simulate.** Real Relay quotes price every chain: gas, launch costs, Relay's fee, any dev buy and a buffer. Nothing moves and nothing is reserved. The total is an estimate, and it expires after 2 minutes.
3. **Pay.** One plain transfer to your home hidden wallet. Nothing starts until the chain shows it. An unpaid order closes after 15 minutes.
4. **Launch.** Each chain then runs alone, and the run shows how far each one got. You can leave the page and come back.

A multi-chain launch needs at least two chains that can launch it.

## It isn't all or nothing

A multi-chain launch isn't atomic. Some chains can land while others fail, and a coin that landed is never undone.

A failed try waits 30 seconds and runs again, up to 3 times, and you can press Retry. Out of tries, that chain's share comes back, less what was already spent.

Unused money comes back from each chain above about **$2**. Anything smaller stays in the sub wallet. The buffer is 5% on top of gas and Relay's fees, and it's refunded when it isn't used.

When every chain is final, the home wallet is emptied to you, which also returns a double payment. A payment that comes after that is swept back for 7 days.

## Fees across chains

Each coin's creator fees start on that coin's own chain. What happens next depends on the launch type:

| Goes home through Relay | Stays on its own chain |
| --- | --- |
| Creator, Team, Wallet, Social, Marketing, Feed a Coin | Holders, Diamond Hands, Buy back and burn, Auto Liquidity |

A Mix applies this per slice.

**Routing home is built and currently off.** Until it's switched on, home-bound fees wait in that chain's pot. Once on, a slice moves when it's worth about **$25** and the route costs under about 3%. Local types work as normal.

## Pairs, dev buys and limits

Each chain pairs with its native coin by default: SOL, ETH, BNB, HYPE, or USDC on Arc. A stock pair is matched by symbol where a chain lists it. The simulation says which chains matched, and the others pair with their native coin.

Team wallets and the coin you feed are on your home chain. With an EVM wallet paying, Team and Feed a Coin can't run on Solana, so leave Solana out or pay from Solana. A Mix on Solana can hold Creator or Wallet then, not both.

Dev buys are set chain by chain, and an empty chain gets none. Each amount becomes that chain's own coin, and each stops at 5% of supply.

- A Solana wallet's dev buy on an EVM chain stays in its sub wallet, where the site can sell it.
- An EVM wallet's dev buy on an EVM chain goes to that wallet.
- An EVM wallet can't hold a Solana coin, so the Solana dev buy goes to a Solana address you give.

| Default limit | Amount |
| --- | --- |
| One launch's total | $500 |
| One paying wallet, rolling 24 hours | $1,000 |
| Launches per wallet, rolling 24 hours | 5 |

You can only have one multi-chain launch in progress at a time.

Next: [EVM chains](evm-chains.md)
