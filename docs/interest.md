---
id: interest
title: How Interest Rates Work
---

This article provides details on how interest rates are calculated on DDEX

# Overview

Interest rates on DDEX are dynamic, fluctuating based on supply and demand. The balance of supply and demand is often referred to as the utilization, or the percent of the total lending pool that is being borrowed at any given time.

The interest rate formulas are designed to encourage the lending pools to always have funds for borrowers. If utilization is high, the interest rates will be high to encourage more lenders to supply funds.

## Formulas

The formulas for lending and borrowing vary slightly by asset. Currently, the formulas for ETH's interest rates are slightly different than the rest of the assets (Stablecoins and WBTC). The ETH rates are designed to start slightly lower than the others, as the demand tends to be quite low respectively.

All interest rates are influenced by a Utilization parameter (U in the formulas below). Utilization is defined as:

- U = Amount currently being borrowed / Total assets in the pool

### Stablecoins and WBTC Interest Rates
Lending and borrowing interest rates for Stablecoins and WBTC are defined by the following functions:

##### Borrowing Interest Rate
- B<sub>i</sub> = 0.05 + (0.4 $\times$ U<sup>4</sup>) + (0.55 $\times$ U<sup>8</sup>)

##### Lending Interest Rate
- L<sub>i</sub> = B<sub>i</sub> $\times$ U $\times$ 0.95

The lending and borrowing interest rates for Stablecoins and WBTC are displayed graphically below. Lending is in <span style="color:purple"> purple </span> while borrowing is in <span style="color:green"> green</span>.

![normal_lending_borrowing](/img/Normal_Lending_Borrowing.png)

### ETH Interest Rates

ETH has a slightly modified interest rate compared to other assets, as defined by the following functions:

##### ETH Borrowing Interest Rate

- B<sub>i</sub> = 0.02 + (0.48 $\times$ U<sup>4</sup>) + (0.5 $\times$ U<sup>8</sup>)

##### ETH Lending Interest Rate

- L<sub>i</sub> = B<sub>i</sub> $\times$ U $\times$ 0.95

The lending and borrowing interest rates for ETH are displayed graphically below. Lending is in <span style="color:purple"> purple </span> while borrowing is in <span style="color:green"> green</span>.

![eth_lending_borrowing](/img/Eth_Lending_Borrowing.png)

## Insurance Pools

You may have noticed the 0.95 in the lending rate formulas. A small fraction (0.5%) of the interest generated by borrowers goes to an insurance pool. The insurance pools help prevent any losses to the lending pools, in case of failed liquidations. **To date, no lenders have incurred net losses on DDEX!**

If you have any additional questions about our interest rates, come chat with us on our [discord channel](https://discord.gg/g6C6jfB).