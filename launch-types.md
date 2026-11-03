# Launch types

When you launch, you pick where creator fees go. The choice is part of the launch and is **locked**: it's stored with the coin and can't be changed afterwards.

On Solana, Just Stealth It's bot applies it, so it isn't locked on chain the way Pump.fun's split is. On EVM chains the contract knows the type and holds the money accordingly.

Every type gets 100% of creator fees. That means the coin's part of the fee, not the whole tax. See [Fees](fees.md).

| Type | Where 100% of creator fees go |
| --- | --- |
| **Social** | A vault for a social account you name, until that person claims. The launcher gets none |
| **Creator** | Your wallet, in the pair token. This is the default |
| **Wallet** | An address you pick |
| **Team** | 2 to 10 wallets, by shares you set |
| **Holders** | The coin's holders, every 10 minutes, in the pair token |
| **Diamond Hands** | Holders who never sold or moved tokens out |
| **Buy back and burn** | Buying the coin and burning it, on each claim |
| **Feed a Coin** | Buying another coin and burning it, on each claim |
| **Auto Liquidity** | A wallet of the coin's own, then its pool after graduation |
| **Marketing** | Promoting the coin. The creator takes none |
| **Mix** | 2 to 5 of the above, in shares you set |

A type that isn't set up on our side shows as unavailable in the launch flow.

## Social

Fees wait for the person you name, and they haven't agreed to anything. See [Social vaults](social-vaults.md). Social vaults are built and currently off.

## Wallet

Pick a chain and paste an address. The launch checks that the address fits the chain, and you confirm you checked it. A wrong address can't be undone.

On Solana the address is paid each time fees are claimed.

Payouts to other chains are built and **currently off**, so the picker shows Solana alone. Once on, fees wait in the coin's escrow until they're worth about **$25**, then cross through Relay, paid in that chain's coin, or a stablecoin where Relay won't quote it. A bridge that would cost more than about 3% waits, and a refund from Relay comes back to the escrow and tries again.

Exchange deposit addresses that need a memo or tag aren't supported. Use a wallet you control.

## Team

The launch form shows a wallet list. Add 2 to 10 wallets, yours too if you want a part, and give each a share. The shares must add up to 100%.

On Solana each wallet is paid straight from the escrow. There's nothing to claim and nothing to accept. On EVM chains a wallet claims its share from the fee vault.

The team is set at launch and can't be changed, so check every address. A lost team wallet keeps its share for good.

## Holders

Creator fees are paid every 10 minutes to every wallet holding at least **10,000** tokens, in proportion to what it holds.

- Payouts are in the **pair token**: SOL on a SOL pair, and the stablecoin or stock on other pairs.
- A round pays once its pot is worth about **$1**.
- A wallet is paid once it's owed about **0.0001 SOL**. Anything smaller carries over. A small amount still owed to a wallet that stops qualifying goes back to the pot after 30 days.
- Wallets holding more than **40,000,000** tokens are left out, and so are the pools and Just Stealth It's own wallets.

The token page shows what was paid, to how many holders, the next round's countdown and every recent round.

## Diamond Hands

The same rounds and minimums as Holders, with fewer holders.

A wallet that sells or moves tokens out, even part of its bag, earns nothing from then on and never gets back in. Sending a bag to a fresh wallet doesn't reset it. What a seller hadn't been paid yet goes back to the pot.

## Buy back and burn

Each time fees are claimed, creator fees stay in the escrow, buy the coin and burn what they bought.

- The escrow needs about **0.006 SOL** before a buy-back can start, and it keeps a small reserve for fees.
- Each buy is limited by price impact (2% by default) and size (5 SOL by default). The rest waits for the next claim.
- On a low-volume coin a buy-back can take a long time to start.
- On EVM chains a buy-back pays the coin's tier like any trade, and it's refused during the anti-sniper window. The token's own `burn` is called, so total supply falls by exactly what was bought.

A burn reduces the coin's supply, and the token page lists each buy and burn with its transactions. A burn isn't a promise of any price or value.

## Feed a Coin

Pick the coin at launch. The launch checks that it can be bought and burned, and refuses a coin with no route.

Each claim buys that coin and burns what it bought, within the same limits as a buy-back. The coin you feed hasn't agreed to anything, and feeding it doesn't connect the two coins.

## Auto Liquidity

1. On each claim, fees leave the escrow for a wallet of the coin's own.
2. After graduation, once that wallet is worth about **$50**, half buys the coin and the rest goes into the coin's pool.
3. On Pump.fun and Raydium the LP is burned in the same transaction. On Meteora the position is locked. Either way nobody can pull it.

A burned LP share earns nobody anything, and no job claims the pool fees of a locked Meteora position yet.

A coin still on its curve 30 days after launch has no pool to add to, so the wallet buys the coin and burns it until it graduates.

It doesn't work with a Global tax. On EVM chains only the locker can add liquidity, so this type buys the coin and burns it there.

## Marketing

The coin's creator fees all go to promoting it. The creator takes none. See [Marketing ladder](marketing.md).

## Mix

Pick 2 to 5 slices from Creator, Team, Wallet, Social, Marketing, Holders, Diamond Hands, Buy back and burn, Feed a Coin and Auto Liquidity. Each slice is at least 1%, and they add up to 100%. Each kind of slice can appear once.

A slice that pays someone pays on claim. One that holds money holds it in the escrow, and each slice can spend only its own balance.

- A Team slice holds up to 5 wallets, because a claim has to fit in one transaction.
- On EVM chains a Mix can't hold both Holders and Diamond Hands.

## Limits by chain

Every type runs on all three Solana venues and on the EVM contracts. On EVM chains, Wallet, Diamond Hands, Feed a Coin, Auto Liquidity and Mix use the contract's general `Pot` type, run by the ops bot.

On a multi-chain launch some types stay on their own chain and others go home. See [Fees across chains](multi-chain.md#fees-across-chains).

Next: [Anti-sniper fee](anti-sniper.md)
