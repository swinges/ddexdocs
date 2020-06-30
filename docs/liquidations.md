---
id: liquidations
title: How Liquidations Work
---

This article describes how the liquidation process works on DDEX.

## What are Liquidations

A liquidation is a process where some of an account's margin assets are traded off quickly to pay back the account's loan. A liquidation typically only occurs when an account is getting severely close to being unable to repay their loan (this is called being "undercollateralized").

## Liqudiations on DDEX

On DDEX, if an account's position drops below 110% collateral rate, it is eligible to be liquidated. The liquidation event is performed as a "dutch auction", where the liquidated account's assets (in that market) are auctioned off to pay back the loan. There is no liquidation penalty on DDEX, so the liquidations often return some assets (called a liquidation refund) back to the account owner's wallet address.

Liquidations on DDEX are designed to protect losses to lending pools while not overly punishing the borrower for their position status.

## Dutch Auctions

A dutch auction auctions of increasing percentages of the total amount of assets in the liquidated account. The auction always has a fixed price (the amount of the loan), but the amount of assets offered in the auction increases with time until a liquidator purchases the assets for the loan price. This process usually takes several minutes.

Initially, only a small amount of the assets are offered. Every block increases the amount until at some point liquidators find the amount offered to be profitable and will finalize the liquidation. Any remaining assets left in the liquidated margin account are then transferred back to the liquidated account's wallet address.

The dutch auction provides an additional level of security for those who take margin positions on DDEX. On the off chance that there was a problem with an oracle that resulted in a liquidation, the dutch auction could still avoid major losses. Another benefit is that there are no penalties for being liquidated. At the point when an account is triggered for liquidation, about 10% of the total account value remains - often times the majority of that value makes it back to the original account.

## Robust Liquidations

The liquidation's primary goal is to protect lending pool losses, so the process must be robust. There are insurance pools on DDEX that also kick into play if the value of a market changes extremely quickly to further help the liquidations succeed. We constantly monitor the nature of our liquidations on DDEX to make sure that the timing is quick enough to avoid losses to the lending pool without penalizing borrowers. It's a tricky balance!

**To date, no lenders have sustained net losses on DDEX**, and there have been no issues with our oracles resulting in false liquidations.

## Reviewing Liquidations

If you happen to be liquidated on DDEX, you'll see a notification with some details. You can also review your full position history at [https://ddex.io/history](https://ddex.io/history) which will show each transaction involved in the liquidation process. This also shows your liquidation refund, which is automatically sent back to your account address.

## Participating in Liquidations

Anyone can participate in the liquidation process! We encourage users to get involved, as there is often some profit to be had in the process. We have an open source liquidation bot for those interested in getting more involved: https://github.com/HydroProtocol/liquidation_bot

As always, if you have any additional questions you can reach us anytime on our [discord channel](https://discord.gg/g6C6jfB).
