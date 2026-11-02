# Bonding curve and graduation

## Supply

Every coin has a fixed supply of **1,000,000,000**. Nobody can mint more, the launcher included. Solana coins have 6 decimals and EVM coins have 18.

## Where the supply goes

| Venue | Sold along the curve | Goes into the pool |
| --- | --- | --- |
| Pump.fun | 79.31% | The rest, at graduation |
| Raydium LaunchLab | 79.31% | 20.69%, at graduation |
| Meteora | 80% | The rest, at graduation |
| EVM chains | 800M from launch price to graduation price | 200M from there to the end of the range |

On Solana, the pool gets its coins at graduation, together with what the curve raised.

On EVM chains the whole supply sits in two locked positions from the first block. They're shaped like a bonding curve, so no migration is needed.

## Pairs

The curve prices and trades in the pair token, and the tax is paid in it.

| Venue | Pairs |
| --- | --- |
| Pump.fun | SOL, or what Pump lists |
| Raydium LaunchLab | SOL, stablecoins such as USD1, USDC and USDT, tokenized stocks, listed tokens |
| Meteora | [20 shared pairs](venues.md#meteora), or a token you search for |
| EVM chains | The native coin |

Pair with a stock and pick the Holders launch type, and your holders are paid in that stock.

> Tokenized stocks are not for US persons. If you are in, resident in or a citizen of the United States, don't launch, trade or receive payouts in them.

## Graduation targets

A SOL-pair curve on Raydium LaunchLab or Meteora raises **85 SOL** before it graduates. Other pairs have their own target, sized to about the same value. A shared Meteora config's target is fixed, so its value can drift as prices move.

EVM launches choose a target inside the factory's range:

| Chain | Min | Default | Max |
| --- | --- | --- | --- |
| Robinhood Chain | 2.5 ETH | 3.5 ETH | 8 ETH |
| Base | 2.5 ETH | 3.5 ETH | 8 ETH |
| BNB Chain | 8 BNB | 11 BNB | 30 BNB |
| HyperEVM | 60 HYPE | 90 HYPE | 200 HYPE |
| Arc | 5,500 USDC | 8,000 USDC | 18,000 USDC |

These are the values on chain today. They apply to future launches, and the admin can move them within hard caps.

## Graduation

When the curve sells out, the coin graduates and keeps trading in a pool.

| Venue | Pool | Liquidity |
| --- | --- | --- |
| Pump.fun | PumpSwap | Pump's own program runs it |
| Raydium LaunchLab | Raydium CPMM | LP locked forever |
| Meteora | Meteora DAMM v2 | Locked forever, in two positions |
| EVM chains | Same pool | Locked from launch |

A graduated Raydium coin's Fee Key sits with Just Stealth It's bot wallet. It can collect the LP's fees and can't withdraw the liquidity. A graduated Meteora coin's LP is half the coin's escrow's and half Just Stealth It's. Both positions are locked and keep earning the pool's fees.

On EVM chains, graduation is a flag set when the price passes a level. It moves no money. Don't treat it, or volume, as proof of demand: a launcher who holds the coin's part gets 70% of the tier back on their own trades, so wash trades are cheap.

## The first buy

Your first buy goes in with the launch, so you buy at the launch price before anyone else can. It's capped at 5% of supply and pays the tier, not the [anti-sniper fee](anti-sniper.md).

Next: [Fees and tax tiers](fees.md)
