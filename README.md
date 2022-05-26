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