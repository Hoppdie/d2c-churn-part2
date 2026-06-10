# Part 2 — RFM Segmentation & Retention Strategy

## Overview
RFM-based customer segmentation enriched with support, web activity, return rate, and discount signals. Includes retention actions, budget allocation, and 10 manual review cases.

**Snapshot date:** `2025-09-30` | **Customers:** 2,400

---

## Repository Structure

```
├── README.md
├── rfm_segmentation.ipynb    ← Main notebook (run in Google Colab)
├── segments.csv              ← Generated after running notebook
├── retention_strategy.md     ← Segment-level retention actions + budget
├── manual_review_cases.md    ← 10 ambiguous customer cases with reasoning
├── requirements.txt
```

---

## How to Run

1. Open [Google Colab](https://colab.research.google.com)
2. Upload `rfm_segmentation.ipynb`
3. Update `DATA_DIR` in cell 2 to your Drive path:
   ```python
   DATA_DIR = '/content/drive/MyDrive/d2c_churn_data/'
   ```
4. **Runtime → Run all**
5. Download the generated `segments.csv` and commit it to this repo

---

## Segments Created

| Segment | Description |
|---|---|
| Champions | Recent, frequent, high-spend — best customers |
| Loyal Customers | Frequent buyers, consistently engaged |
| New Customers | Very recent, low frequency — still onboarding |
| Promising | Moderate across all dimensions |
| At-Risk | Previously good, but recency is poor |
| Dormant | Low on everything — likely already gone |
| High-Value Unhappy | High spend but negative support experience |
| Discount-Dependent | Only buys with heavy discounts (>35% avg) |

## Non-RFM Signals Used
1. **Support tickets** — count, sentiment, reopened rate
2. **Web activity** — sessions, product views, cart adds, email opens
3. **Return rate** and **average discount usage**
4. **Campaign history** — last campaign received, CRM priority bucket

---

## Dataset
Download from: https://drive.google.com/drive/folders/1PmLapJI1VSDgvl_AxARNKwM1MCd3WFX0?usp=sharing
