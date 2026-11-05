# Addresses

## Official coin

**$STEALTH** on Solana: `GoDSW31bTxfkoup9yA1qcGGx9RMXdTEWgApv3xzBmoA`

Any other address claiming to be the official coin isn't.

## Solana programs

These belong to the venues, not to Just Stealth It.

| Program | Used for | Address |
| --- | --- | --- |
| Pump.fun | Bonding curve | `6EF8rrecthR5Dkzon8Nwu78hRvfCKubJ14M5uBEwF6P` |
| PumpSwap | Pool after graduation | `pAMMBay6oceH9fJKBRHGP5D4bD4sWpmSwMn52FMfXEA` |
| Raydium LaunchLab | Bonding curve | `LanMV9sAd7wArD4vJFi2qDdfnVhFxYSUg6eADduJ3uj` |
| Raydium CPMM | Pool after graduation | `CPMMoo8L3F4NbTegBCKVNunggL7H1ZpdTHKxQB5qKP1C` |
| Meteora DBC | Bonding curve | `dbcij3LWUppWqq96dh6gJWwBifmcGfLSB5D4DuSMaqN` |
| Meteora DAMM v2 | Pool after graduation | `cpamdpZCGKUy5JxQXB4dcpGPiikHawvSWAd6mEn1sGG` |

Raydium platforms, the lookup table and Meteora configs are in [smart-contracts](https://github.com/juststealthit/smart-contracts).

## EVM contracts

Robinhood Chain, Base and Arc share most addresses:

| Contract | Address |
| --- | --- |
| Factory | `0xF828FD2DB63E3aF84f950eFcF601dE1B679B567d` |
| Fee vault | `0x5F15d599BA849554A40975333a7e39F537c37e61` |
| Locker | `0x6e0C6a185ACd0b5CB8050823aB570A5565Bebf34` |
| Router | `0x887724eBE323e7C4aBF4a240DDBa6828Bc89F6a6` |
| Token deployer | `0x5d30FE70B12ABB4728741A7fF38295e5Dab0ed27` |
| Token implementation | `0x005BDc162F7bCF6D5fEbB30a845698061F8AE3af` |

The hook differs by chain:

| Chain | Hook |
| --- | --- |
| Robinhood Chain | `0xa12B34E4a5968163A2FBa4cdE85656dDAe5078Ec` |
| Arc | `0xa12B34E4a5968163A2FBa4cdE85656dDAe5078Ec` |
| Base | `0x485155E2160A62EECc33fC86fB6fA01C6c9FF8ec` |

BNB Chain uses the same addresses for everything above but the hook. Its contracts are the PancakeSwap Infinity build, and its hook is `0x4bE4973112a5e053B790Fa99dF2012F96bcD0e1a`.

HyperEVM has its own set:

| Contract | Address |
| --- | --- |
| Factory | `0xB138Cb32B62e23eb148Ccbd94f089396c09D24e7` |
| Fee vault | `0x5d30FE70B12ABB4728741A7fF38295e5Dab0ed27` |
| Hook | `0x12772A9DeeD523527172452e1Ed2d12154ECF8Ec` |
| Locker | `0xF828FD2DB63E3aF84f950eFcF601dE1B679B567d` |
| Router | `0x5F15d599BA849554A40975333a7e39F537c37e61` |
| Token deployer | `0x6e0C6a185ACd0b5CB8050823aB570A5565Bebf34` |
| Token implementation | `0x15D2eA82F366581BB472A5243C1f6a7cC0373Da1` |

### Deploying: Ethereum, Arbitrum and Avalanche

The same contracts are being deployed on these three. Each address goes here once its deploy is checked on chain. Until then, nothing on these chains is ours.

| Contract | Ethereum | Arbitrum One | Avalanche C-Chain |
| --- | --- | --- | --- |
| Factory | Deploying | Deploying | Deploying |
| Fee vault | Deploying | Deploying | Deploying |
| Hook | Deploying | Deploying | Deploying |
| Locker | Deploying | Deploying | Deploying |
| Router | Deploying | Deploying | Deploying |
| Token deployer | Deploying | Deploying | Deploying |
| Token implementation | Deploying | Deploying | Deploying |

An address can mean different contracts on different chains. Always match the chain to the table.

Each contract's job is in [EVM chains](evm-chains.md#how-a-launch-works).

Next: [FAQ](faq.md)
