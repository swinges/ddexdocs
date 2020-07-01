---
id: margin
title: How To Margin Trade On DDEX
---

This article provides information on how to margin trade on DDEX. If you're more of a visual learner, you can check out our youtube tutorials for [basic mode margin trading](https://youtu.be/tQGsDNMvh9o) or [pro mode margin trading](https://youtu.be/DYCiQUwQ864).

# Margin Trading Modes

We have two modes of margin trading on DDEX - basic and pro mode. 

Basic mode is a simplified form of margin trading: you just enter in what you want your final position to look like and DDEX helps composite the transactions to get there. 

Pro mode unlocks the full power of margin trading, giving you complete control over your position. You can modify existing positions, place limit and stop-limit orders, and more.

## Basic Margin Trading

There are 3 things you need to select to open a margin position in our Basic Mode:

1. Are you Long or Short? (Side)
2. How large should the position be? (Amount)
3. What percentage of that position should be borrowed? (Leverage)

We'll discuss these three choices here, but first let's take a step back and review how a margin position is opened.

### Two Transactions

A margin position is created by depositing some assets as collateral into a market, borrowing assets, and trading those borrowed assets to create leverage. In the basic mode, we compose these transactions for you based on what you enter in the orders field, then you sign the transactions through your wallet interface. 

You'll have two transactions to sign: one for depositing and borrowing *(you select the gas price on this one)*, and another for performing the trade *(we select the gas price on this one)*.

### Creating your first position

To begin, select what Side of the market you want to be on - whether you want to go "Long" or "Short" on an asset.

- Going Long means you think the base asset is going to gain value over the quote asset.
- Going Short means you think that the base asset will lose value compared to the quote asset.

*Note - on the ETH-USDT market, ETH is the base asset and USDT is the quote asset*

Next, select the leverage rate you'd like for the final position. The leverage rate indicates how much you'd like to borrow vs how much you want to deposit. If I wanted to deposit 1 ETH, a 2x leverage would borrow an additional 1 ETH worth of assets. A 3x leverage would borrow 2 ETH, 4x would borrow 3 ETH, etc.

Lastly, decide how much you want in your final position. If you select 10 ETH, your final position will combine to total 10 ETH of assets (deposited assets + borrowed assets = 10 ETH of value).

Once you have your side, leverage, and amount selected, you're ready to create your first position! Sign the two transactions and your position will be officially open.

## Pro Margin Trading

Our pro mode margin trading is like traditional spot trading, but with the ability to borrow extra funds to provide additional leverage to your trades. There are 3 steps to creating a position in the pro mode:

1. Deposit some assets into the market as collateral
2. Borrow some assets to trade with
3. Trade

The amount that you can borrow is dependent on your deposited amount. When you go to borrow assets, you'll see a slider that indicates your leverage.

## Closing Your Position

Both Basic and Pro modes have a "Close Position" button. DDEX will guide you through the closing process which involves two transactions:

1. Trading assets so that you have enough to pay back your loan
2. Repaying the loan

Once a loan is completely repaid, your position is considered closed! At this point you can fully transfer assets out of the margin account.

## Additional Resources

Having any issues or want to share some margin trading victories? Hop into our [discord channel](https://discord.gg/g6C6jfB)!