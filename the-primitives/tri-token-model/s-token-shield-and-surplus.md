---
description: '"Shield + Surplus Yield = Smart Alpha"'
icon: shield-halved
---

# S-Token (Shield & Surplus)

**S-Token** is the "High Yield" engine of AquaFlux. It is designed for users who want to earn significantly more than the standard rate and are comfortable taking on the role of a **Risk Underwriter**.

### What it is <mark style="color:$warning;">S-Token</mark>

S-Token is the <mark style="color:$warning;">Shield</mark>, first-loss buffer that protects P and C. In return, it can earn a <mark style="color:$warning;">Surplus yield</mark><mark style="color:orange;">:</mark> a slice of _coupons_, a share of _protocol fees,_ and a possible _points or airdrop_ reward from issuer.

### The Core Concept: You are the Insurer

The best way to understand S-Token is through an insurance analogy:

* P-Token Holders are the **Insured**. They accept a lower return in exchange for safety.
* S-Token Holders are the **Insurers**. You provide that safety (First-Loss protection).

Why do it? Because insurers get paid **Premiums**. In AquaFlux, these "premiums" come in two powerful forms:

1. **Intrinsic Yield** (S-Token): The base asset's yield + fees.
2. **Extrinsic Rewards** (SS, Staked S-Token): The protocol's incentive rewards + upside.

### <mark style="color:$warning;">S-Token</mark> (Shield, The Underwriter) <a href="#id-2-layer-1-s-token-the-premium" id="id-2-layer-1-s-token-the-premium"></a>

By holding S-Token, you are the **Underwriter** of the pool. This position gives you two powerful rights:

1. **The Yield**: You earn a share of the **underlying asset's principal and coupon**. It's the intrinsic cash flow from the asset itself.
2. **The Exclusive Ticket**: S-Token is the **only way** to access **SS (Surplus)**. Think of S-Token as your membership pass—without it, you cannot participate in the underlying's future upside.

**The Risk (First-Loss)**

Just like an insurance company, if valid claims are made (i.e., the asset defaults or loses value), you pay first. Your capital absorbs the loss to protect P-Token holders.

### <mark style="color:purple;">SS</mark> (Staked S, The Bonus) <a href="#id-3-layer-2-ss-the-bonus" id="id-3-layer-2-ss-the-bonus"></a>

This is the "Hidden Gem" of the system. While S-Token captures the asset's yield, **SS (Surplus)** captures the protocol's upside.

**Crucial Rule:**&#x20;

1. **Stake S-Token**:  Stake your S-Tokens into the protocol.
   * _Note: Once staked, your S-Tokens are **locked until the asset matures**. You cannot unstake early._
2. **Earn SS Linearly**: SS is generated continuously based on your staked amount. The more you stake and the longer you wait, the more SS you earn.
3. **Claim & Trade Anytime**: While your S-Token is staked, your earned **SS is liquid**. You can claim your SS rewards at any time and sell them on the secondary market if you wish.

**Think of it this way**:

* **Staking S** = Planting a tree. You can't move the tree until harvest season (Maturity).
* **Receiving SS** = Gathering fruit. You can pick and sell the fruit (SS) whenever you want, while the tree continues to grow.

***

### How it works

* **Loss waterfall**
  * **S-Token** absorbs losses first (up to its coverage).
  * If losses exceed S, **C-Token** is reduced next.
  * Only extreme residual loss may reach **P-Token**.
* **Cash flows to S**
  * **Coupon share:** A fixed % of each coupon payment.
  * **Protocol fees:** A defined % of AquaFlux fees (swap/wrap/split/merge/LP fees, etc.—see dApp).
  * **Issuer incentives:** A possible points or airdrop reward from issuer.
* **Pricing (no hard par):**\
  S’s fair value ≈ _(expected coupon share + expected fees + expected residual)_ − _(expected losses)_.\
  Expectations change with asset quality, coverage ratio, time to maturity, and market sentiment.

### Who it’s for

* **Yield hunters / risk takers** who understand first-loss dynamics.
* **Structured-yield strategies** selling downside in exchange for higher carry.

### Acquire & Exit

* **Acquire**
  * Wrap a supported RWA and **Split** into P/C/S.
  * **Buy** S-Token directly in the pool/AMM.
* **Exit**
  * **Sell anytime** at market price (T+0).
  * **At maturity**: if the bond repays in full, any **unused** S buffer + final fee/coupon shares are distributed to S holders. If losses occurred, your S position may be partially/fully reduced.

### S Tranche Valuation

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
  No. Buying S-Token is like **selling** insurance—you act as the first-loss provider (the underwriter). You earn coupon/fee shares and potential residuals for taking that risk, and you’re hit first if losses occur. If you want to **buy** protection instead, do the opposite: **short the S-Token** or avoid S and hold **P (or P + C)** so the first-loss buffer works in your favor.
* **When do I earn?**\
  Throughout the term (coupon/fee distributions) and potentially at maturity (unused buffer), provided performance is on track.
* **What happens if there’s a default?**\
  S is reduced first. If the loss exceeds S, it then hits C, and only then P.
* **Can S-Token go to zero?**\
  Yes, in severe loss scenarios. Size positions accordingly.
* **Why do S-Tokens price so differently?**\
  Coverage %, asset quality, expected recoveries, time to maturity, and market liquidity all drive expected carry vs. expected loss.

