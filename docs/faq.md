---
id: faq
title: FAQ
sidebar_label: Frequently Asked Questions
---

Welcome to DDEX's frequently asked questions page. If you can't find the info you're looking for, come check out our discord!

# Overview

## What is DDEX?

DDEX is a decentralized borrowing, lending, and trading platform. You can margin trade (up to 5x leverage), spot trade, lend assets to earn interest, and borrow assets. DDEX runs on the Ethereum blockchain primarily hosting ETH, BTC, and stablecoin pairs (USDT, USDC, DAI).

## Is DDEX secure?

```
DDEX uses professionally audited Ethereum smart contracts to process transactions. Since we launched our alpha back in July of 2019, we have had no security problems.

Security is our top priority - DDEX's structure was built from the ground up to prioritize security above all else: from price oracles, to liquidation mechanisms, to the underlying smart contracts.
```

## Who can use DDEX?

Anyone canuse DDEX. There's no account creation process - simply connect any digital wallet that we support (we support a ton!)

# Lending and Borrowing

## How are interest rates set?

In short, lending and borrowing interest rates are set based upon supply and demand. The greater the demand, the higher the interest rates. We measure demand through "utilization", which is the percentage of the total lending pool that is in use. The curve is exponential, so that lending is greatly encouraged when utilization reaches 100%.

For more specific details on the algorythms and logic, check out our interest rate article here.

## Can I use my borrowed assets outside of DDEX?

You sure can! However, you cannot acheive leverage rates quite as high as if you kept your assets in DDEX. We use the borrowed assets as part of your collateral as long as it remains within DDEX, which allows you to borrow a lot more (and apply greater leverage to positions as desired).

The minimum collateral rate we allow is 125%, which is consistent with other similar DeFi platforms.

## How does DDEX determine asset prices?

We use a combination of on-chain price oracles, off-chain liquidity sources, and automated logical checks. The exact price oracle process varies by market.

## How do liquidiations work on DDEX?

Liquidations on DDEX are triggered by a 3rd party initiator. When initiated, our smart contracts will check to see if the flagged address is qualified for liquidation (i.e. their collateral rate is below the respective threshold for that market). If it is not below the threshold, nothing happens. If it is, a liquidation event is triggered.

DDEX uses a form of dutch auctions for liquidation events. The dutch auction attempts to sell the borrower’s collateral to repay their debt. However, it doesn’t just start with selling the entire collateral — initially, only a small percentage of the collateral is offered up for auction. As time passes, each subsequent block offers a bit more of the collateral.

Eventually the value of the percentage of collateral offered will make a profitable trade for outsiders. If the auction is completed before 100% of the collateral is used, the remaining collateral will be returned to the borrower, with a small amount going to the initiator as a reward.

By performing liquidations in this method, even if a price oracle were to fail and a position got liquidated prematurely, the losses for the borrower would be minimized. The borrower effectively has an additional layer of protection from price oracle failures through our dutch auction liquidation method.

## Is lending risk free?

While there is always some risk in lending, a percentage of interest gets sent to an insurance pool, to help avoid losses for the lending pool. In the case where the borrowed amount became less than the collateral, the auction could increment the collateral beyond 100% and tap into the insurance pool to provide additional incentive for this collateral to be purchased in the auction.