# Social vaults

> Built and **currently off**. This page describes how it works once it's switched on.

A Social launch names a person by their account on X, Twitch or GitHub, where those are on. Creator fees wait in a vault for that person. **The launcher gets none of them.**

TikTok isn't available for naming, because it has no public lookup of an account's permanent id.

**The person named hasn't agreed to anything.** Being named doesn't mean they know about the coin, made it or endorse it. Treat any such claim as unverified.

## How it works

1. Pick a platform, then type a username or pick from the list of well-known accounts. A live lookup binds the coin to the account's permanent id, so a rename doesn't break it.
2. The coin launches like any other. Its creator fees go to the person's vault, which Just Stealth It controls. Every coin naming them stacks in the same vault. A public page shows their coins and fees on every chain.
3. To claim, the person signs in with that account and signs with a wallet. The first claim binds that wallet to the vault, and later claims need the same one.

Token pages show an **Is this you?** banner, so the person can find their fees.

## Limits

| Default limit | Amount |
| --- | --- |
| One claim | About 10 SOL's worth |
| One vault, per day | 25 SOL |
| All vaults together, per day | 200 SOL |

The rest waits.

- On a non-SOL pair the vault holds the pair token and pays it as it is. A token with no price waits.
- Fees stay in the vault with no deadline, until they're claimed or Just Stealth It moves them. Nothing redirects or expires them, and they never go back to the launcher.
- A social slice on an EVM coin routes to the person's Solana vault, where their claims pay out. Until [routing](multi-chain.md#fees-across-chains) is on, it waits on its own chain.

## Trust

Just Stealth It holds the keys of every Social vault and can move its funds. Nothing does that on a timer. A claim can only pay what's still there.

Next: [The Feed](feed.md)
