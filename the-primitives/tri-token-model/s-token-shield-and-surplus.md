---
description: '"Shield + Surplus Yield = Smart Alpha"'
icon: shield-halved
---

# S-Token (Shield & Surplus)

### What it is <mark style="color:orange;">S-Token</mark>

S-Token is the “<mark style="color:orange;">**first-loss**</mark>” buffer that protects P and C.\
In return, it can earn a <mark style="color:orange;">**surplus yield**</mark><mark style="color:orange;">:</mark> a slice of **coupons**, a share of **protocol fees**, and a possible **points or airdrop** reward from issuer.

### Why it matters

* **Shield the system** – S absorbs first loss, stabilizing P and then C.
* **Multiple income sources** – Coupons + protocol fees + and, where applicable, issuer incentives/airdrops.
* **Risk-priced carry** – Higher expected yield for taking first-loss risk.

> Tip: **You sell protection and get paid for it.** If nothing bad happens, you keep the carry (coupon+fees+incentives) and the unused buffer. If losses occur, **you’re hit first**.

### How to get S-Token

* **Stablecoin users:** Open AquaFlux **Swap**, choose a pool, **buy S-Token** directly.
* **RWA holders:** **Wrap** the asset, then **Split** to mint **P/C/S**—keep S (swap out P/C if needed).

### How it works

* **Loss waterfall**
  * **S-Token** absorbs losses first (up to its coverage).
  * If losses exceed S, **C-Token** is reduced next.
  * Only extreme residual loss may reach **P-Token**.
* **Cash flows to S**
  * **Coupon share:** A fixed % of each coupon payment.
  * **Protocol fees:** A defined % of AquaFlux fees (swap/wrap/split/merge/LP fees, etc.—see dApp).
  * **Issuer incentives:** A possible points or airdrop reward from issuer.
* **Pricing intuition (no hard par):**\
  S’s fair value ≈ _(expected coupon share + expected fees + expected residual)_ − _(expected losses)_.\
  Expectations change with asset quality, coverage ratio, time to maturity, and market sentiment—so price **may not stable** as P.

### Who it’s for

* **Yield hunters / risk takers** who understand first-loss dynamics.
* **Structured-yield strategies** selling downside in exchange for higher carry.

### Playing S with P / C (LEGO® combos)

* **P + S → “cash-plus”**: principal-heavy with a small yield kicker from S income; S amount kept modest to cap drawdown.
* **C + S → “enhanced carry”**: harvest coupons and fee share at the same time.
* **S only → “pure protection seller”**: maximum exposure to first-loss in exchange for the highest potential carry.

### Acquire & Exit

* **Acquire**
  * Wrap a supported RWA and **Split** into P/C/S.
  * **Buy** S-Token directly in the pool/AMM.
* **Exit**
  * **Sell anytime** at market price (T+0).
  * **At maturity**: if the bond repays in full, any **unused** S buffer + final fee/coupon shares are distributed to S holders. If losses occurred, your S position may be partially/fully reduced.

### S-Token Valuation

**Definition**\
The S-Token is the junior, first-loss tranche. Its present value (PV) is the sum of upside components minus expected loss:

$$
\mathrm{PV}_{S}=\mathrm{PV}_{\text {coupon share }}+\mathrm{PV}_{\text {fee share }}+\mathrm{PV}_{\text {points/airdrop }}-\mathrm{PV}_{\text {expected loss }}
$$

***

Now, let's decompose each term in the formula, let's define

* Face value per unit: **N** (e.g., N=100).
* Time to maturity: **T** (years).
* Discount rate: **r** (annual; discount via (1+r)).
* Bond coupon rate: **c** (annual).
* Coupon share to S: **γ** (e.g., 20% of total coupon).
* Pool fee rate per swap: **f** (e.g., 0.20%).
* Annual turnover (volume/TVL): **v** (turnover per year).
* Protocol fee split to S: **α** (e.g., 50%).

1. **Coupon Share**&#x20;

&#x20; If coupon is realized at maturity:

$$
\text{PV}_{\text{coupon share}} = \frac{\gamma c N}{(1 + r)^T}
$$

2. **Fee Share**&#x20;

You can check the exact fee accumulation in the **on-chain vault**. And you can also use the following methods to make an estimate.

Currently this mainly considering AMM fees, and we will add split/merge, wrap/unwarp fees later.

Annual fees attributable to notional **N**:

$$
Feeyear=f⋅v⋅N
$$

S receives fraction:

$$
\text{PV}_{\text{fee share}} \approx \frac{\alpha f v N}{(1 + r)^{T}}
$$

3. **Points / Airdrop**&#x20;

You need to calculate according to the specific airdrop rules.

* **Check the rule:** emission pace, eligible actions (LP, stake, quests), and any **boosts**.
* **Time matters:** count only **active days** you expect to participate.
* **Apply a haircut:** reflect eligibility risk, snapshot timing, vesting/lockups, and token-price uncertainty.

4. **Expected Loss**

You can use different risk models to calculate.

S is the **first-loss** tranche. Keep it simple with a blended annual loss assumption:

* **Use bands, not a single number:** Conservative / Base / Optimistic.
* **What drives it:** issuer quality, asset health, **S coverage** (thicker S = more buffer), diversification, and historical behavior.
* **Cap awareness:** S’s annual loss cannot exceed its **coverage size**; excess loss would waterfall to senior tranches.
* **Update cadence:** revisit after material events (audits, covenant breaches, ratings watch, liquidity stress).
* **Presentation:** show the three bands alongside key context (coverage %, asset type, tenor) and note that it’s a **prudential estimate**.



### FAQ

* **Is S-Token principal-protected?**\
  No. It’s **first-loss** by design. You are compensated via coupon share, fee share, and potential residual—**not** by a 1:1 redemption promise.
* **Does buying S-Token give me insurance on the asset?**\
  No. Buying S-Token is like **selling** insurance—you act as the first-loss provider (the underwriter). You earn coupon/fee shares and potential residuals for taking that risk, and you’re hit first if losses occur. If you want to **buy** protection instead, do the opposite: **short the S-Token** (where supported) or avoid S and hold **P (or P + C)** so the first-loss buffer works in your favor.
* **When do I earn?**\
  Throughout the term (coupon/fee distributions) and potentially at maturity (unused buffer), provided performance is on track.
* **What happens if there’s a default?**\
  S is reduced first. If the loss exceeds S, it then hits C, and only then P.
* **Can S-Token go to zero?**\
  Yes, in severe loss scenarios. Size positions accordingly.
* **Why do S-Tokens price so differently?**\
  Coverage %, asset quality, expected recoveries, time to maturity, and market liquidity all drive expected carry vs. expected loss.

