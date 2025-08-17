---
description: Lifecycle — From Bond to LEGO® and Back
---

# Lifecycle

_Tokenize → Split → Compose → Merge → Unwrap_

### TL;DR

Start with a supported real-world asset, turn it into an on-chain position, split it into **P / C / S**, mix them as you like, and—whenever you want—rejoin and exit back to the original asset.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### The 5 Actions at a glance

The 5 actions are independent, you may only need to perform one.

* &#x20;`wrap()` — Tokenize the asset
  * **What you do:** Lock a verified RWA into AquaFlux.
  * **What you get:** An on-chain position (aqToken) with clear **maturity**, **coupon schedule**, and **S-coverage**.
  * **You can:** hold it, or move to step 2 to split.
  * **Note:** Fees and docs depend on the pool’s settings.
* &#x20;`split()` — Create P / C / S
  * **What you do:** Turn the aqToken into three tokens:
    * **P** = Principal (redeems 1.00 at maturity)
      * **C** = Coupon (income stream)
      * **S** = Shield (first-loss + surplus streams)
  * **You can:** trade them, LP them, or use them as collateral (market-dependent).
* &#x20;**Compose** — Build your payoff
  * **What you do:** Mix P / C / S to match your goal:
    * **P only** → principal + time value
    * **C only** → income
    * **S only** → higher carry with first-loss risk
    * **P + C** → “classic bond”
    * **P +  S** → “cash-plus”
    * **C + S** → “enhanced carry”
    * ...
  * **You can:** automate strategies or just hold what fits your view.
* &#x20;`merge()` — Rejoin the pieces
  * **What you do:** Combine P / C / S back into an aqToken.
  * **Why useful:** simplifies positions, prepares for unwrap, or resets strategy.
* `unwrap()` — Exit back to the original asset
  * **What you do:** Convert the aqToken to the off-chain claim per pool rules.
  * **When:** at maturity or as allowed by the pool (some pools only settle at maturity).

### What you can do at each stage

* **Trade anytime (T+0):** buy/sell P / C / S in the pool.
* **Provide liquidity:** earn fees and incentives (where offered).
* **Borrow/lend (market-dependent):** P often gets **higher LTV**, C medium, S low/ineligible.
* **Manage duration:** roll P to nearer maturities; time coupon calendars with C.

### Quick example timeline

1. Wrap a 12-month bond → get aqToken.
2. Split → receive **P / C / S**.
3. Hold **P** (principal), sell **C** (you don’t want income), keep a **small S** for extra yield.
4. Three months later, merge everything you still hold → unwrap or keep until maturity.

### FAQ

**Do I have to merge to redeem P?**\
No. **P** redeems **1:1 at maturity**. Merging is optional.

**Can I exit early?**\
Yes—sell P / C / S in the pool at market price (T+0), subject to liquidity.

**Is S principal-protected?**\
No. **S is first-loss**; it earns surplus streams but can be impaired.

**Who sets parameters like S-coverage and fee shares?**\
Each pool defines them. Check the pool panel before acting.
