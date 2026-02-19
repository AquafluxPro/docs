---
description: “Discounted Principal, Leverage Ready”
icon: circle-dollar
---

# P-Token (Principal)

### **What is&#x20;**<mark style="color:blue;">**P-Token**</mark>

P-Token represents the **principal portion** of a RWA. It works like a zero-coupon bond: you buy it at a discount today, and it targets face value (e.g., $1.00) when the bond matures. No coupons, no complexity -- just a clean, predictable return.

If something goes wrong with the underlying asset, the S-Token (the "airbag") absorbs losses before P-Token is affected.

### Why it matters

* **Clear principal** – Principal is unbundled from coupons and default risk, so you always know what you hold.
* **Discounted principal** – Pay less today, redeem face value later. Think of buying a dollar bill for 94 cents and getting the full dollar back later.&#x20;
* **Leverage loop** – Stake P-Tokens → borrow stablecoins → buy more P-Tokens → repeat, compounding yield.
* **Higher borrow limit** – Because S-Token takes first losses, lenders may accept P-Tokens as **stronger collateral**, allowing a higher LTV than the raw RWA.

> P is for people who want principal first, clear timelines, and optional leverage without juggling coupons.

### How to Get P-Token

* **Stablecoin users:** Open AquaFlux **Swap**, choose a pool, **buy P-Token** directly.
* **RWA holders:** **Wrap** the asset, then **Split** to mint **P/C/S**—keep **P** (swap out C/S if needed).

### How it works

* **Cash flow**: No interim coupons; redeem face value at maturity (e.g., 1 USDC).
* **Intuitive pricing**: “What should I pay today to receive principal in T years?”

$$
\begin{aligned}
P &\approx \frac{1 - s}{(1+r)^T} \\ \\
s &= \text{\% allocated to S-Token (principalToS)} \\
r &= \text{discount rate},\quad T=\text{years to maturity}
\end{aligned}
$$

* **Quick example**: 12 months to go, discount rate = 6%, **s = 0%**:

> P = (1 - 0) / (1.06)^1 = **$0.9434**
>
> You pay $0.9434 today and receive $1.00 in a year, a $0.0566 profit per token.

* **What moves the price:**
  * **Time passes** -- P naturally pulls toward $1.00 as maturity (like a countdown).
  * **Rates drop** -- P rises (closer to $1.00), because the market demands a smaller discount.
  * **Rates rise** -- P falls (farther from $1.00), because the market demands a bigger discount.

> Tips: Real trades can differ from the simple model due to S-coverage, asset quality, and pool liquidity.

### Collateral & leverage

* **Why lenders like it**: First-loss protection from S can make P-Token **strong collateral**; some markets may grant **higher borrow limits** than the original RWA.
* **Leverage loop (example)**:
  1. Stake P-Tokens in a lending market
  2. Borrow stablecoins
  3. Buy more P-Tokens
  4. Repeat prudently to **amplify yield**

> Tips: Leverage magnifies both gains and losses. Know your limits.

### Acquire & Exit

* **Acquire**
  * Wrap a supported RWA and **split** it into P/C/S in AquaFlux.
  * **Buy** P-Token directly in the pool/AMM.
* **Exit**
  * **Hold to maturity** → auto redemption at **1:1** (e.g., 1 P → 1 USDC).
  * **Sell anytime** → T+0 liquidity at prevailing market price.

### Who It’s For

* **Conservative treasuries & DAOs** seeking low-volatility principal exposure.
* **Cash management** users who want short duration, predictable redemption.
* **Rate traders** who want to express a view on interest rates (discount rates).

### FAQ

* **Does P-Token pay coupons?**\
  No. It behaves like a zero-coupon bond.
* **How does redemption work?**\
  At maturity, P-Token redeems to the settlement asset (e.g., USDC) based on the asset's specific parameters (typically **1:1**, but subject to `principalToS` settings).
* **What if the underlying defaults?**\
  S-Token absorbs first, then C-Token. Only after those buffers could P-Token be affected. Always check asset disclosures and S-coverage.
* **Can I “redeem” early?**\
  You **sell** early in the pool (T+0), at the current market price—not a fixed 1:1 redemption.
* **Why do different P-Tokens have different prices?**\
  Different maturities (duration), discount rates, S-coverage, and liquidity profiles.
