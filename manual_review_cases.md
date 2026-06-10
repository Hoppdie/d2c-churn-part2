# Manual Review Cases
## D2C Customer Churn Capstone — Part 2

These are 10 customers where the automated segment assignment does not capture the full picture. Each case has conflicting signals that require human judgement before a retention action is taken.

> **Note:** The specific customer IDs, metrics, and churn outcomes below will be populated when the notebook is executed against the actual dataset. The reasoning framework below applies to each case type.

---

### Case 1–3: At-Risk Customers Still Browsing the Site

**Profile:** Segment = At-Risk | High recency (60–120 days since last order) | BUT 3+ web sessions in last 30 days

**Dilemma:** These customers are classified as At-Risk based on order recency, but they're still actively visiting the website. They're window-shopping but not converting. Are they comparison-shopping with competitors? Waiting for a sale? Experiencing a product-fit issue?

**Recommendation:** Do NOT send a blanket discount. Instead, send a personalised product recommendation based on their recent browsing behaviour (most-viewed category). If they have items in an abandoned cart, trigger a cart recovery email. A discount should only follow if the personalised nudge doesn't convert within 7 days.

---

### Case 4–5: Champions with Negative Support Tickets

**Profile:** Segment = Champions | High R/F/M scores | BUT 1+ negative sentiment support ticket(s)

**Dilemma:** These are top-tier customers by purchase behaviour, but they've had a bad support experience. The segment label says "celebrate," but the support signal says "fix this first." Sending a VIP reward to someone with an unresolved complaint would feel tone-deaf.

**Recommendation:** Escalate the support case immediately. A dedicated agent should call (not email) to resolve the issue. Once resolved, offer a proactive goodwill credit (₹200–500) and a personal note from the team. The goal is to prevent a Champion from becoming an At-Risk customer. The cost of the credit is trivial compared to the lifetime value at stake.

---

### Case 6–7: New Customers with Unusually High First Spend

**Profile:** Segment = New Customers | Recency < 30 days, Frequency = 1–2 | BUT monetary value in the top 20%

**Dilemma:** A brand-new customer who spends significantly above average on their first order could be a future Champion — or a one-time gifter (buying for someone else) who will never return. The segment says "onboard," but the spend level suggests this customer might deserve fast-track treatment.

**Recommendation:** Send the standard welcome series but add a personalised touch: "We noticed you loved [category] — here are three products our top customers pair with it." If a second order happens within 30 days, auto-enrol them in the loyalty programme at Silver tier (skip the earn-in period). If no second order in 45 days, send a "How did they like their gift?" email to determine if this was a gift purchase.

---

### Case 8–9: Dormant Customers Still Opening Marketing Emails

**Profile:** Segment = Dormant | No purchases in 150+ days | BUT 3+ email opens in last 30 days

**Dilemma:** By purchase behaviour, these customers are gone. But they're still opening marketing emails, which means they haven't fully disengaged. Standard Dormant treatment (minimal outreach, survey) might miss a reactivation window.

**Recommendation:** This is a hidden re-activation opportunity. Send a targeted "We miss you" offer with a specific product from their previously purchased category. Make it time-bound (72-hour expiry) to create urgency. If they click but don't buy, follow up with a "Was there something stopping you?" feedback prompt. Budget allocation: redirect ₹500 from the Dormant survey budget to fund this targeted outreach.

---

### Case 10: Discount-Dependent Customer with Decent Frequency

**Profile:** Segment = Discount-Dependent | Average discount > 35% | BUT frequency is moderate (3+ orders)

**Dilemma:** This customer buys regularly but only with heavy discounts. The segment treatment says "stop discounting," but cutting discounts abruptly might cause immediate churn. The customer has demonstrated loyalty — just not at full price.

**Recommendation:** Gradual discount weaning. Next campaign: offer 25% off (reduced from their usual 35%+) paired with 2x loyalty points. If they convert, next offer drops to 15% + 3x points. The goal is a 3-step transition from discount-driven to points-driven purchasing over 90 days. Track whether order frequency holds — if it drops by more than 50%, revert to the previous discount level and accept the margin trade-off.

---

## Summary

| Case | Customer ID | Segment | Key Conflict | Recommended Override |
|---|---|---|---|---|
| 1–3 | (from notebook) | At-Risk | Still browsing but not buying | Personalised product reco, not discount |
| 4–5 | (from notebook) | Champions | Negative support tickets | Escalate support FIRST, then goodwill credit |
| 6–7 | (from notebook) | New Customers | Unusually high first spend | Fast-track loyalty if second order comes |
| 8–9 | (from notebook) | Dormant | Still opening emails | Time-bound targeted offer, not just survey |
| 10 | (from notebook) | Discount-Dependent | Decent frequency | Gradual discount weaning over 90 days |

> **Important:** After running the notebook, the actual customer IDs and their specific metrics will fill in the table above. Each case was selected because the automated segment rule alone would have led to a suboptimal retention action.
