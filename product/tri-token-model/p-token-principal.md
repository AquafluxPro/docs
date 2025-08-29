---
description: “Discounted Principal, Leverage Ready”
icon: circle-dollar
---

# P-Token (Principal)

### **What is&#x20;**<mark style="color:blue;">**P-Token**</mark>

P-Token represent the <mark style="color:blue;">**principal part**</mark> of a RWA, it likes the on-chain version of a **zero-coupon bond.**

You buy it **below 1.00**, receive **1.00 at maturity**, and you can **sell anytime** before maturity in the pool. If losses occur, S-Token (first-loss buffer) is designed to take the hit before P-Token.

### Why it matters

* **Clear principal** – Principal is unbundled from coupons and default risk, so you always know what you hold.
* **Discounted principal** – Pay less today, redeem 1.00 later, your spread is locked in from day one.
* **Higher borrow limit** – Because S-Token takes first losses, lenders may accept P-Tokens as **stronger collateral**, often allowing a **higher LTV** than the raw RWA—so you can unlock bigger loans.
* **Leverage loop** – Stake P-Tokens → borrow stablecoins → buy more P-Tokens → repeat, compounding yield.

> P is for people who want principal first, clear timelines, and optional leverage without juggling coupons.

### How to get P-Token

* **Stablecoin users:** Open AquaFlux **Swap**, choose a pool, **buy P-Token** directly.
* **RWA holders:** **Wrap** the asset, then **Split** to mint **P/C/S**—keep **P** (swap out C/S if needed).

### How it works

* **Cash flow**: No interim coupons; **redeem 1.00 at maturity** (e.g., 1 USDC).
* **Intuitive pricing**: “What should I pay today to receive 1.00 in T years?”

$$
\begin{aligned}
P &\approx \frac{1}{(1+r)^T} \\ \\
r &= \text{discount rate},\quad T=\text{years to maturity}
\end{aligned}
$$

*   **Quick example**: 12 months to go, r=6% → **0.9434**.

    As time passes, price **pulls toward 1.00**; if rates fall, price rises faster.
* **Intuition:**
  * **Time passes → P** naturally **pulls** to **1.00**.
  * **Rates down → P up** (closer to 1.00).

> Tips: Real trades can differ from the simple model due to S-coverage, asset quality, and pool liquidity.

### Collateral & leverage

* **Why lenders like it**: First-loss protection from S can make P-Token **strong collateral**; some markets may grant **higher borrow limits** than the original RWA.
* **Leverage loop (example)**:
  1. Stake P-Tokens in a lending market
  2. Borrow stablecoins
  3. Buy more P-Tokens
  4. Repeat prudently to **amplify yield**

> Tips: Leverage magnifies both gains and losses. Know your limits.

### Playing P with C / S (LEGO® combos)

* **P + C → “classic bond”** (principal + coupons).
* **P + S → “cash-plus”** (principal-heavy with a small yield kicker).
* **P only → clean rate/duration** exposure.

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
  No. It behaves like a zero-coupon bond—value accretes toward 1.00, and rate moves can change price.
* **How does redemption work?**\
  At maturity, it redeems **1:1** to the settlement asset (e.g., USDC), per dApp instructions.
* **What if the underlying defaults?**\
  S-Token absorbs first, then C-Token. Only after those buffers could P-Token be affected. Always check asset disclosures and S-coverage.
* **Can I “redeem” early?**\
  You **sell** early in the pool (T+0), at the current market price—not a fixed 1:1 redemption.
* **Why do different P-Tokens have different prices?**\
  Different maturities (duration), discount rates, S-coverage, and liquidity profiles.
