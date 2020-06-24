---
id: liqudiations
title: How Liquidations Work
---

This article describes how the liquidation process works on DDEX.

# Overview

Liquidations are events designed to protect losses to lending pools. On DDEX, if an account's position gets below 110% collateral rate, it is eligible to be liquidated. The liquidation event is performed as a dutch auction, where the liquidated account's assets (in that market) are auctioned off to pay back the loan. There is no liquidation penalty on DDEX, so the liquidations often return some assets (called a liquidation refund) back to the account owner's wallet address.

## Dutch Auctions

A dutch auction takes the total amount of assets in the liquidated account and auctions them off at increasing percentages of the total. The auction always has a fixed price (the amount of the loan), but the amount of assets offered in the auction increases with time. So initially, only a small amount of the assets are offered. At some point, the liquidators will find the amount to be profitable and will finalize the liquidation. Any remaining amounts are then transferred back to the liquidated account's wallet.

The dutch auction provides an additional level of security to those who take margin positions on DDEX. On the off chance that there was a problem with an oracle that resulted in a liquidation, the dutch auction could still avoid major losses. Another benefit is that there are no penalties for being liquidated. At the point when an account is triggered for liquidation, about 10% of the total account value remains - often times the majority of that value makes it back to the original account.

## Robust Liquidations

The liquidation's primary goal is to protect lending pool losses, so the process must be robust. There are insurance pools on DDEX that also kick into play if the value of a market changes extremely quickly to further help the liquidations succeed. We constantly monitor the nature of our liquidations on DDEX to make sure that the timing is quick enough to avoid losses to the lending pool without penalizing borrowers. It's a tricky balance! To date, no lenders have sustained net losses on DDEX, and there have been no issues with our oracles resulting in false liquidations.