# Retention Strategy
## D2C Customer Churn Capstone — Part 2

**Budget:** ₹50,000 | **Snapshot:** 2025-09-30 | **Customers:** 2,400 | **Overall churn:** 47.0%

---

## Final Segment Profiles (from actual data)

| Segment | Customers | Avg Recency | Avg Freq | Avg Monetary | Avg Tickets | Avg Sentiment | Avg Sessions | Churn Rate |
|---|---|---|---|---|---|---|---|---|
| Dormant | 317 | 172 d | 1.25 | ₹782 | 0.33 | −0.12 | 3.7 | **87.0%** |
| At-Risk | 451 | 163 d | 3.86 | ₹3,086 | 0.66 | −0.20 | 3.8 | **78.0%** |
| Discount-Dependent | 214 | 102 d | 2.96 | ₹1,900 | 0.63 | −0.21 | 5.0 | **56.0%** |
| High-Value Unhappy | 162 | 110 d | 6.21 | ₹4,795 | 2.62 | −0.56 | 5.1 | **56.0%** |
| Promising | 309 | 51 d | 2.20 | ₹1,774 | 0.57 | −0.20 | 6.1 | **36.0%** |
| Loyal Customers | 190 | 55 d | 5.11 | ₹3,552 | 0.83 | −0.25 | 6.4 | **26.0%** |
| New Customers | 413 | 20 d | 1.24 | ₹909 | 0.30 | −0.11 | 6.7 | **23.0%** |
| Champions | 344 | 21 d | 6.37 | ₹4,916 | 1.46 | −0.36 | 7.3 | **10.0%** |

The segmentation cleanly separates churn risk: Dormant/At-Risk churn at 78–87%, while Champions/New churn at 10–23%. This validates the RFM + behavioural approach.

---

## Segment Definitions & Retention Actions

### 1. Dormant (2% budget = ₹1,000)
**Profile:** 317 customers, 172-day avg recency, 1.25 orders, ₹782 spend, 87% churn.  
**Who:** Customers who bought once or twice long ago and have essentially left.  
**Action:** Minimal investment. Single "We miss you" email + a short exit survey to learn why they left. Do not spend retention budget chasing an 87%-churn group — most are already gone.

### 2. At-Risk (Priority 1 — 30% budget = ₹15,000)
**Profile:** 451 customers, 163-day recency, 3.86 orders, ₹3,086 spend, 78% churn.  
**Who:** Previously solid buyers (nearly 4 orders, ₹3K spend) who have gone quiet. The highest-value recoverable group.  
**Action:** URGENT personalised win-back. Reference their actual purchase history ("your favourite [category] is back in stock"). Time-bound offer.  
**Why Priority 1:** Big segment (451), high spend, and at 78% churn there is enormous upside to recovering even a fraction.

### 3. High-Value Unhappy (Priority 2 — 25% budget = ₹12,500)
**Profile:** 162 customers, 6.21 orders, ₹4,795 spend, 2.62 tickets, −0.56 sentiment (most negative), 56% churn.  
**Who:** High-spending, frequent customers who are actively dissatisfied — most support tickets and worst sentiment.  
**Action:** Resolve open tickets FIRST via a dedicated agent. Only then send goodwill credit (₹200–500) + loyalty upgrade. Never send a marketing offer to someone with an unresolved complaint.  
**Why Priority 2:** Highest spend-at-risk. Negative sentiment (−0.56) shows these are fixable service failures, not natural attrition.

### 4. Discount-Dependent (Priority 5 — 8% budget = ₹4,000)
**Profile:** 214 customers, 2.96 orders, ₹1,900 spend, 40% avg discount (highest), 56% churn.  
**Who:** Buy only on heavy discounts. 40% average discount vs ~27% for other segments.  
**Action:** Do NOT send another discount. Offer loyalty points / cashback to shift value perception. Gradual discount weaning.  
**Why:** Recoverable but margin-eroding. Worth keeping only if we can change their buying behaviour.

### 5. Promising (Priority 3 — 15% budget = ₹7,500)
**Profile:** 309 customers, 51-day recency, 2.20 orders, ₹1,774 spend, 36% churn.  
**Action:** Product recommendations + light bundle offers + educational content. Build the habit.  
**Why Priority 3:** Below-average churn but large enough that small improvements compound.

### 6. Loyal Customers (Priority 6 — 5% budget = ₹2,500)
**Profile:** 190 customers, 5.11 orders, ₹3,552 spend, 26% churn.  
**Action:** Reward, don't discount. Early access to launches + referral programme.

### 7. New Customers (Priority 4 — 12% budget = ₹6,000)
**Profile:** 413 customers, 20-day recency, 1.24 orders, ₹909 spend, 23% churn.  
**Action:** Onboarding series + first-reorder incentive. Auto-enrol in loyalty if second order lands within 30 days.  
**Why mid-priority:** Large group (413), low churn now but unproven — onboarding window determines lifetime value.

### 8. Champions (Priority 8 — 3% budget = ₹1,500)
**Profile:** 344 customers, 6.37 orders, ₹4,916 spend (highest), 10% churn (lowest).  
**Action:** VIP perks, ambassador programme. Zero discounts — they don't need them.

---

## Budget Prioritisation

| Priority | Segment | Budget | Rationale |
|---|---|---|---|
| 1 | At-Risk | ₹15,000 (30%) | Largest high-value recoverable group, 78% churn |
| 2 | High-Value Unhappy | ₹12,500 (25%) | Highest spend-at-risk; fixable via support |
| 3 | Promising | ₹7,500 (15%) | Large nurture opportunity |
| 4 | New Customers | ₹6,000 (12%) | Onboarding window critical |
| 5 | Discount-Dependent | ₹4,000 (8%) | Behaviour change, not more discounts |
| 6 | Loyal Customers | ₹2,500 (5%) | Reward, low risk |
| 7 | Champions | ₹1,500 (3%) | Already retained at 90% |
| 8 | Dormant | ₹1,000 (2%) | 87% churn — survey only |

**Total: ₹50,000**

Budget is deliberately concentrated on **At-Risk + High-Value Unhappy** (55% of budget), which together hold 613 high-spend customers with fixable, recoverable churn. We spend almost nothing on Dormant (87% churn — unrecoverable) and Champions (10% churn — already safe).
