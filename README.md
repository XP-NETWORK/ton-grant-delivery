# The Open Network (TON) Grant Delivery Report

Project Repository: [the-open-network](https://github.com/XP-NETWORK/xp-the-open-network/)

<hr>

## `Milestone 1` — Smart Contract Development

Began: April, 1st, 2022

Finished: May, 9th, 2022

| # | Deliverable | Proof |
|-|-|-|
|1| We researched Ton NFT standards |[TIP-62](https://github.com/ton-blockchain/TIPs/issues/62)<br/>[TIP-64](https://github.com/ton-blockchain/TIPs/issues/64)|
|2| We developed for Native NFTs: <br/>+ Freeze<br/>+ Unfreeze |<br/>+ [Freeze](https://github.com/XP-NETWORK/xp-the-open-network/blob/b019727c7d9a48c299ed948aec93796011029997/src/contracts/bridge.ts#L179-L193)<br/>+ [Unfreeze](https://github.com/XP-NETWORK/xp-the-open-network/blob/b019727c7d9a48c299ed948aec93796011029997/src/contracts/bridge.ts#L153-L177)|
|3| We developed for wrapped NFTs:<br/>+ Mint <br/>+ Burn |<br> + [Minting](https://github.com/XP-NETWORK/xp-the-open-network/blob/b019727c7d9a48c299ed948aec93796011029997/src/contracts/bridge.ts#L99-L133)<br/>+ [Burning](https://github.com/XP-NETWORK/xp-the-open-network/blob/b019727c7d9a48c299ed948aec93796011029997/src/contracts/bridge.ts#L135-L151)|
|4| We implemented withdrawing<br/> the TX fees on the target chain in native tokens|+ [Withdrawing](https://github.com/XP-NETWORK/xp-the-open-network/blob/b019727c7d9a48c299ed948aec93796011029997/src/contracts/bridge.ts#L219-L240)|

<hr>

## `Milestone 2` — Smart Contract Development

Began: May, 10th, 2022

Finished: May, 26th, 2022 (2 weeks ahead of schedule)

| # | Deliverable | Proof |
|-|-|-|
||We have developed smart contracts that can:||
|5|Trust the multisig of the bridge oracle validators|+ [Code](https://github.com/XP-NETWORK/xp-the-open-network/search?q=check_signature)|
|6|Whitelist NFT smart contracts|+ [Code](https://github.com/XP-NETWORK/xp-the-open-network/blob/91bffbcc4d884c8bc630599557bfb41a964a3be1/func/bridge.func#L177)|
|7|+ Pause<br/>+ Unpause<br/>for maintenance or if compromised|+ [Pause](https://github.com/XP-NETWORK/xp-the-open-network/blob/91bffbcc4d884c8bc630599557bfb41a964a3be1/func/bridge.func#L195)<br/>+ [Unpause](https://github.com/XP-NETWORK/xp-the-open-network/blob/91bffbcc4d884c8bc630599557bfb41a964a3be1/func/bridge.func#L213)<br/><br/>|
|8|Reimburse the bridge validators their expenses|+ [Code](https://github.com/XP-NETWORK/xp-the-open-network/blob/main/func/bridge.func#L126-L156)|

<hr>

## `Milestone 3` — Testing & Documenting

Began: May, 26th, 2022

Finished: June, 20th, 2022 (10 days ahead of schedule)

| # | Deliverable | Proof |
|-|-|-|
|1|Inline Documentation|+ [bridge](https://github.com/XP-NETWORK/xp-the-open-network/blob/main/func/bridge.func)<br/>+ [burner](https://github.com/XP-NETWORK/xp-the-open-network/blob/main/func/burner.func)|
|2|Functional Tests with min 85% code coverage|+ [Link](#functional-tests)|
|3|Deployed in the testnet environment|+ [burner contract](https://testnet.tonscan.org/address/kQBkPHU3Fo4FEQGZYh6a-4SbjqaTfA6wfMDcyT-U5TCN__jC)<br/>+ [bridge contract](https://testnet.tonscan.org/address/kQBHIUR8NXBPZM6UZsgn5sBhFunoLvCJZteoj_6SUJcIjPoY)<br/>+ [collection](https://testnet.tonscan.org/address/EQBCZps88OUB5o2bGObx_2e002s3BtLp4Gq27NF3fqlRMKdJ)|
|4|Tested the functionality:|+ [minting](https://testnet.tonscan.org/tx/985319000001:UNfD1lL5jXCTmu+unyO2KOvlmxjirLOMTkTkgqkhHJ0=:EQALnbCowLoBEVmvSGGYKOIYySPbLKeUDTWWsl0AmqqzApek)<br/>+ [freezing](https://testnet.tonscan.org/tx/985525000003:OT%2F0Pa0dB5vzhiFybrxYYHQiomlWD0JFGih2wPT4BPM=:EQD-y4PUC7N5Rr-9qJRDLe9PDu4-R_ieKfm0kPvqSgPQHsSe)<br/>+ [unfreezing](https://testnet.tonscan.org/tx/985674000003:x0GngVfN5e%2FNASW+vsSVvkzx796r4kbwB99cTbuxuik=:EQBHIUR8NXBPZM6UZsgn5sBhFunoLvCJZteoj_6SUJcIjEGS)<br/>+ [withdrwing](https://testnet.tonscan.org/tx/981042000001:oXNsZOZPos5X8kWXUwdyD+saAbgQpz87CDo%2FWyjVPHQ=:EQAxZV60jjRcLtENLjNv-4I4SjS1HBBdI1ilvzbUuXaHK3Pk)<br/>+ [whitelisting](https://testnet.tonscan.org/tx/980723000003:SPYrGao80FFol32ioFv9D0C+W91x290tl%2FUorcTcTeg=:EQBHIUR8NXBPZM6UZsgn5sBhFunoLvCJZteoj_6SUJcIjEGS)|


## Functional Tests

Test source code: https://github.com/XP-NETWORK/xp-the-open-network/blob/main/tests/bridge.ts

Running:
```
yarn test
```
Outcome:
![Outcome-1](./assets/test-1.png)

Test Source code:https://github.com/XP-NETWORK/xp-the-open-network/blob/main/src/test-nft.ts

Running:
```
yarn test-nft
```
Outcome:
![Outcome-2](./assets/test-2.png)

## `Milestone 4` — Integrating into the Live Bridge


| # | Deliverable | Proof |
|-|:-:|:-:|
|1| Developed validation logic for TON|Link|
|2|Added TON to NFT-Indexer|Indexer|
|3|Implemented fee estimation for TON|Proof|
|4|Added TON to the bridge Explorer|Explorer|
|5|Integrated TON RPC nodes|RPC|
|6|Adde TON to the bridge UI|UI|
|7|Deployed Smart contracts on TON|Testnet \| Mainnet|
|8|Adde TON to the JS Libabry|XPJS|
|9|Added TON to the bridge Widget|Widget|

### 1. Validation Logic

### 2. NFT-Indexer

### 3. Fee Estimation

### 4. Bridge Explorer


### 5. RPC Node Integration


### 6. Bridge UI


### 7. Deployed Smart Contracts


### 8. JavaScript / TypeScript Library


### 9. Bridge Widget

