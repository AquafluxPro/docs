---
icon: money-check-dollar
---

# C-Token (Coupon)

### **What is&#x20;**<mark style="color:purple;">**C-Token**</mark>

**C-Token** represent the **coupon part** of a RWA, it is the <mark style="color:purple;">**income leg**</mark>**.** It can capture **the return** of the underlying asset, such as **interest** of a bond, **rent** of a REI&#x54;**.**

### Why it matters

* **Income first** – Hold C to receive the bond’s coupon cash flows on-chain.
* **Flexible exit** – You can **sell anytime** in the pool (T+0), instead of waiting for every coupon date.
* **Composable yield** – LP, stake, or combine with P/S to build custom payoffs.

### Acquire & exit

* **Acquire**
  * Wrap a supported RWA and **Split** into P/C/S, or
  * **Buy C** directly in the pool/AMM.
* **Exit**
  * **Sell anytime** (T+0) at the market price, or
  * **Hold to collect** upcoming coupons per schedule.

### FAQ

**Does C-Token have a fixed redemption like 1.00?**\
No. C is a claim on **coupon income**, not on par value.

**What if the asset underpays or defaults?**\
**S takes losses first**. If losses exceed S, **C can be reduced**; only after that might P be affected.

**Why does C’s price move?**\
Interest rates, default expectations, time until the next coupons, and pool liquidity.
