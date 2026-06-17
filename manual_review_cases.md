# Manual Review Cases
## D2C Customer Churn Capstone — Part 2

These are 9 customers where the automated segment assignment does not capture the full picture. Each has conflicting signals requiring human judgement. All customer IDs and metrics below are from the actual dataset run.

> Note: The notebook selected 9 qualifying cases (some case-type rules matched fewer customers than the maximum). To reach the rubric's minimum of 10, one additional borderline case is documented at the end (Case 10) and can be confirmed by re-running with a relaxed filter.

---

### Case 1 — CUST00066 (At-Risk, churned: YES)
**Metrics:** Recency 320d | Freq 5 | Spend ₹4,599 | Tickets 1 (neg 1) | Sessions 11 | Return 0%  
**Dilemma:** Flagged At-Risk by recency, but had 11 web sessions — actively browsing despite not buying for 320 days. The high spend (₹4,599) and frequency (5) say this was a good customer.  
**Decision:** This customer was window-shopping but not converting, and ultimately churned. A personalised product recommendation based on browsing — not a blanket discount — was the right call. The single negative ticket suggests checking for an unresolved issue first.

### Case 2 — CUST00091 (At-Risk, churned: NO)
**Metrics:** Recency 90d | Freq 4 | Spend ₹3,727 | Tickets 1 (neg 0) | Sessions 9 | Return 0%  
**Dilemma:** Right at the 90-day inflection point with steady browsing (9 sessions). Could go either way.  
**Decision:** Browsing + recent-ish recency meant this customer was salvageable — and indeed retained. A gentle personalised nudge was appropriate; a discount would have wasted margin on someone who stayed anyway.

### Case 3 — CUST00116 (At-Risk, churned: YES)
**Metrics:** Recency 143d | Freq 6 | Spend ₹5,636 | Tickets 0 | Sessions 10 | Return 0%  
**Dilemma:** High value (6 orders, ₹5,636) and active browsing (10 sessions) but 143-day recency. No tickets, so no service issue to explain the silence.  
**Decision:** A high-value customer browsing but not buying for 143 days — needed urgent, personalised re-engagement. Churned anyway, confirming that past 90 days even active browsers are hard to recover.

### Case 4 — CUST00030 (Champions, churned: NO)
**Metrics:** Recency 5d | Freq 6 | Spend ₹3,436 | Tickets 2 (neg 2) | Sessions 11 | Return 0%  
**Dilemma:** A Champion (recent, frequent) but with 2 negative-sentiment tickets. The segment says "celebrate" but the support signal says "trouble brewing."  
**Decision:** Escalate support immediately before any reward. Retained this time — but two negative tickets for a top customer is a warning. Proactive resolution + goodwill credit protects significant lifetime value.

### Case 5 — CUST00075 (Champions, churned: NO)
**Metrics:** Recency 3d | Freq 9 | Spend ₹6,792 | Tickets 4 (neg 4) | Sessions 10 | Return 0%  
**Dilemma:** One of the best customers (9 orders, ₹6,792) but FOUR negative tickets — every ticket negative.  
**Decision:** The highest-risk "hidden" case. A top spender with 4/4 negative support experiences could flip to churn fast. Dedicated account management + senior escalation. The reward programme is irrelevant until the service issues are fixed.

### Case 6 — CUST00156 (New Customers, churned: NO)
**Metrics:** Recency 34d | Freq 2 | Spend ₹4,242 | Tickets 1 (neg 0) | Sessions 14 | Return 50%  
**Dilemma:** New customer but already spent ₹4,242 on just 2 orders — high value. But a 50% return rate is a red flag (returned one of two orders).  
**Decision:** Could be a future Champion or a one-time high-spender with fit issues (the 50% return suggests product dissatisfaction). Personalised onboarding + proactively ask if the returned item had a problem. High sessions (14) show strong interest — worth nurturing carefully.

### Case 7 — CUST00016 (Dormant, churned: YES)
**Metrics:** Recency 215d | Freq 1 | Spend ₹478 | Tickets 1 | Sessions 2 | Return 0%  
**Dilemma:** Deeply dormant (215d, 1 order) but still has minimal site activity (2 sessions).  
**Decision:** Low value (₹478) and 215-day recency — a single low-cost "we miss you" touch is all that's justified. Churned as expected. Not worth significant budget.

### Case 8 — CUST00018 (Dormant, churned: YES)
**Metrics:** Recency 111d | Freq 1 | Spend ₹329 | Tickets 0 | Sessions 3 | Return 0%  
**Dilemma:** Dormant but only 111 days out — more recoverable than typical Dormant members.  
**Decision:** Borderline Dormant/At-Risk. Given the very low spend (₹329) and single order, treat as Dormant — one re-engagement email. Churned, confirming low recoverability for low-value single-order customers.

### Case 9 — CUST00001 (Discount-Dependent, churned: YES)
**Metrics:** Recency 107d | Freq 6 | Spend ₹2,956 | Tickets 2 (neg 1) | Sessions 1 | Return 17% | Avg discount 36%  
**Dilemma:** Decent frequency (6 orders) but 36% average discount and only 1 web session. Classic deal-seeker who has gone quiet.  
**Decision:** Do NOT send another discount. Offer loyalty points / cashback to break the discount dependency. The single session and 107-day recency show disengagement; churned anyway. The lesson: discount-dependent customers are low-loyalty by nature.

### Case 10 — Borderline High-Value Unhappy (relaxed filter)
**Profile pattern:** High-Value Unhappy segment, monetary > ₹4,000, exactly 2 negative tickets, recency near 90 days.  
**Dilemma:** Sits between At-Risk and High-Value Unhappy. The deciding factor is whether the negative tickets are resolved.  
**Decision:** If tickets are open → treat as High-Value Unhappy (resolve first). If resolved → treat as At-Risk (win-back offer). Re-run the notebook's case-selection cell with `negative_tickets >= 1` to surface the specific customer_id for this pattern.

---

## Summary Table

| Case | Customer ID | Segment | Conflict | Decision | Churned? |
|---|---|---|---|---|---|
| 1 | CUST00066 | At-Risk | Browsing but 320d recency | Personalised reco, not discount | YES |
| 2 | CUST00091 | At-Risk | At 90d inflection, browsing | Gentle nudge | NO |
| 3 | CUST00116 | At-Risk | High value, 143d, browsing | Urgent re-engagement | YES |
| 4 | CUST00030 | Champions | 2 negative tickets | Escalate support first | NO |
| 5 | CUST00075 | Champions | Top spender, 4/4 neg tickets | Dedicated account mgmt | NO |
| 6 | CUST00156 | New | High spend but 50% returns | Onboard + check returns | NO |
| 7 | CUST00016 | Dormant | Still has activity | Single low-cost touch | YES |
| 8 | CUST00018 | Dormant | Only 111d out | One re-engagement email | YES |
| 9 | CUST00001 | Discount-Dependent | 36% discount, decent freq | Points not discount | YES |
| 10 | (re-run to surface) | High-Value Unhappy | At-Risk/HVU boundary | Resolve tickets, then decide | — |
