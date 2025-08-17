---
description: “Discounted Principal, Leverage Ready”
---

# P-Token (Principal)

### **What is P-Token**

**P-Token is the on-chain version of a zero-coupon bond.** You don’t receive coupons during the term; instead, you redeem **1 unit at maturity** (e.g., 1 USDC). Losses—if any—are designed to hit **S-Token (first-loss buffer)** before touching P-Token.

### What P-Token Solves

* **Clear principal exposure** – Principal is unbundled from coupons and default risk, so you always know what you hold.
* **Better liquidity** – Don’t want to wait? Sell P-Token in the pool with T+0 settlement.
* **Rate visibility** – P-Token prices reflect a **discount rate / yield to maturity**, just like zero-coupon bonds.

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
