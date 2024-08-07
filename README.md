# First Flight #10: One Shot

# Contest Details

### Prize Pool

- High - 100xp
- Medium - 20xp
- Low - 2xp

- Starts: February 22, 2024 Noon UTC
- Ends: February 29, 2024 Noon UTC

### Stats

- nSLOC: 201
- Complexity Score: 143

[//]: # (contest-details-open)

## Disclaimer

_This code was created for Codehawks as the first flight. It is made with bugs and flaws on purpose._
_Don't use any part of this code without reviewing it and audit it._

_Created by equious.eth_

# About

When opportunity knocks, you gunna answer it? One Shot lets a user mint a rapper NFT, have it gain experience in the streets (staking) and Rap Battle against other NFTs for Cred.

## OneShot.sol

The Rapper NFT.

Users mint a rapper that begins with all the flaws and self-doubt we all experience.
NFT Mints with the following properties:

- `weakKnees` - True
- `heavyArms` - True
- `spaghettiSweater` - True
- `calmandReady` - False
- `battlesWon` - 0

The only way to improve these stats is by staking in the `Streets.sol`:

## Streets.sol

Experience on the streets will earn you Cred and remove your rapper's doubts.

- Staked Rapper NFTs will earn 1 Cred ERC20/day staked up to 4 maximum
- Each day staked a Rapper will have properties change that will help them in their next Rap Battle

## RapBattle.sol

Users can put their Cred on the line to step on stage and battle their Rappers. A base skill of 50 is applied to all rappers in battle, and this is modified by the properties the rapper holds.

- WeakKnees - False = +5
- HeavyArms - False = +5
- SpaghettiSweater - False = +5
- CalmAndReady - True = +10

Each rapper's skill is then used to weight their likelihood of randomly winning the battle!

- Winner is given the total of both bets

## CredToken.sol

ERC20 token that represents a Rapper's credibility and time on the streets. The primary currency at risk in a rap battle.

## Roles

User - Should be able to mint a rapper, stake and unstake their rapper and go on stage/battle

[//]: # (contest-details-close)

[//]: # (getting-started-open)

# Getting Started

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
- [foundry](https://getfoundry.sh/)
  - You'll know you did it right if you can run `forge --version` and you see a response like `forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)`

# Usage

## Testing

```
forge test
```

### Test Coverage

```
forge coverage
```

and for coverage based testing:

```
forge coverage --report debug
```

[//]: # (getting-started-close)

[//]: # (scope-open)

# Audit Scope Details

- In Scope:

```
├── src
│   ├── CredToken.sol
│   ├── OneShot.sol
│   ├── RapBattle.sol
│   ├── Streets.sol
```

## Compatibilities

- Solc Version: `^0.8.20`
- Chain(s) to deploy contract to:
  - Ethereum
  - Arbitrum
 
[//]: # (scope-close)

[//]: # (known-issues-open)

# Known Issues

None

[//]: # (known-issues-close)
