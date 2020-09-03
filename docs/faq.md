---
id: faq
title: FAQ
sidebar_label: Frequently Asked Questions
---

Wow Kalm is amazing! Welcome to [DDEX](https://ddex.io)'s frequently asked questions page. If you can't find the info you're looking for, come chat with us on our [discord channel](https://discord.gg/g6C6jfB).

# Overview

## What is DDEX?

DDEX is a decentralized borrowing, lending, and trading platform. You can margin trade *(up to 5x leverage)*, spot trade, lend assets to earn interest, and borrow assets. DDEX runs on the [Ethereum blockchain](https://ethereum.org/en/) primarily hosting ETH, BTC, and stablecoin pairs (USDT, USDC, DAI).

## Is DDEX secure?

DDEX uses [professionally audited](https://github.com/HydroProtocol/audit-reports/blob/master/2.0/hydro_audit_report_2019_14_en_1_0.pdf) Ethereum smart contracts to process transactions. We have had no security problems to date since we launched our alpha back in July of 2019.

Security is our top priority - DDEX's structure was built from the ground up to prioritize security above all else: from price oracles, to liquidation mechanisms, to the underlying smart contracts.

## Who can use DDEX?

Anyone can use DDEX. There's no account creation process - simply connect any digital wallet that we support.

Our most popular wallet type is [Metamask](https://metamask.io/). We also support several mobile friendly options such as [Fortmatic](https://fortmatic.com/), [WalletConnect](https://walletconnect.org/), and [Coinbase Wallet](https://wallet.coinbase.com/). Additionally, [Ledger](https://www.ledger.com/), [Trezor](https://trezor.io/), and [D'CENT](https://dcentwallet.com/) hardware wallets are all supported. Lastly, we have support for [Torus](https://tor.us/) through Google or Facebook OAuth.

# Lending and Borrowing

## How are interest rates set?

In short, lending and borrowing interest rates are set based upon supply and demand. The greater the demand, the higher the interest rates. We measure demand through "utilization", which is the percentage of the total lending pool that is in use.

For more specific details on our formulas, check out the [How Interest Rates Work article](interest).

## Can I use my borrowed assets outside of DDEX?

You sure can! However, you cannot achieve leverage rates quite as high as if you kept your assets in DDEX. We use the borrowed assets as part of your collateral as long as it remains within DDEX, which allows you to borrow a lot more (and apply greater leverage to positions as desired).

The minimum collateral rate we allow is 125%, which is consistent with other similar DeFi platforms.

## How does DDEX determine asset prices?

We use a combination of on-chain price oracles, off-chain liquidity sources, and automated logical checks. The exact price oracle process varies by market.

## How do liquidations work on DDEX?

Liquidations on DDEX are performed through dutch auctions which trigger when an account drops to below 110% collateral rate.

For more detailed information on how our liquidations work, check out the [How Liquidations Work article](liquidations).

## Is lending risk free?

While there is always some risk in lending, a percentage of interest gets sent to an insurance pool, to help avoid losses for the lending pool. In the case where the borrowed amount became less than the collateral, the auction will increment the collateral beyond 100% and tap into the insurance pool to provide additional incentive for this collateral to be purchased in the auction.
