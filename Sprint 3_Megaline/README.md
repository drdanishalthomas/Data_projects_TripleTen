# 📊 Sprint 3 — Megaline Plan Analysis: Statistical Testing

![Python](https://img.shields.io/badge/Python-3.x-blue) ![SciPy](https://img.shields.io/badge/SciPy-Statistics-orange) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Project Overview

Megaline, a telecom operator, offers two prepaid plans: **Surf** and **Ultimate**. The commercial department wants to know which plan generates more revenue to optimize their advertising budget. This project analyzes 500 customer accounts across calls, messages, and internet usage to determine the more profitable plan using statistical hypothesis testing.

---

## Dataset

Five interconnected datasets covering 500 Megaline customers:

| Dataset | Records | Description |
|---|---|---|
| `calls.csv` | 137K+ | Call records with duration and dates |
| `internet.csv` | 104K+ | Internet session data with volume |
| `messages.csv` | 76K+ | Text message records |
| `plans.csv` | 2 | Plan details (Surf & Ultimate) |
| `users.csv` | 500 | Customer demographics and plan info |

---

## Methodology

1. **Data Preparation:** Cleaned and merged five datasets; converted date columns to datetime; rounded call durations up per billing rules
2. **Aggregation:** Calculated monthly usage per customer — total calls, messages, and data consumed
3. **Revenue Engineering:** Computed monthly revenue incorporating plan-specific overage charges
4. **Statistical Testing:** Used Welch's t-test to compare average revenue between Surf and Ultimate plans
5. **Regional Analysis:** Tested whether NY-NJ area users generate different revenue than other regions

---

## Results

| Metric | Surf Plan | Ultimate Plan |
|---|---|---|
| **Average Monthly Revenue** | $60.17 | **$72.25** |
| **Revenue Std Dev** | $53 (high variance) | $11 (low variance) |
| **Plan Comparison (p-value)** | — | **p < 0.001** |

| Test | Result |
|---|---|
| Surf vs Ultimate Revenue | **Significant difference** (p < 0.001) |
| NY-NJ vs Other Regions | **No significant difference** (p = 0.079) |

---

## Key Findings

- **Ultimate plan generates 20% more revenue** ($72.25 vs $60.17) with statistical confidence
- Ultimate plan provides **more predictable cash flow** — low revenue variance ($11 std dev) vs Surf's high variance ($53 std dev)
- Call duration patterns were nearly identical between plans (~7.3 min average), but Ultimate users consumed more data and sent more messages
- **Geographic targeting is not recommended** — no statistically significant revenue difference between NY-NJ and other regions
- **Recommendation:** Allocate 70% of advertising budget to Ultimate plan promotion; use national campaigns rather than regional targeting

---

## How to Run

> **Note:** Dataset path references the TripleTen platform (`/datasets/`). Cell outputs are preserved for viewing without re-execution.

```bash
pip install pandas numpy matplotlib seaborn scipy
jupyter notebook notebook.ipynb
```

---

## Skills Demonstrated

`pandas` · `numpy` · `matplotlib` · `seaborn` · `scipy` · statistics · hypothesis testing · Welch's t-test · revenue analysis · data cleaning · merging datasets · groupby aggregation · business-driven analysis
