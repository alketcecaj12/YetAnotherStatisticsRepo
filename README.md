# 📊 Yet Another Statistics Repo
> *Because you can never have too many hypothesis tests — with Python code, real use cases, and zero fluff.*

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![SciPy](https://img.shields.io/badge/SciPy-statistical%20tests-8CAAE6?logo=scipy&logoColor=white)](https://scipy.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

## 🎯 What Is This?

Hypothesis testing is one of the most misunderstood — and most misused — tools in data science. This repository cuts through the noise with **clear explanations, decision logic, and working Python code** for the most frequently used statistical tests.

Whether you're validating an A/B test, checking model assumptions, or analysing survey data, this is your practical reference.

---

## 🧭 Which Test Should I Use?

```
Is your data categorical?
├── Yes → Chi-Square Test (goodness of fit or independence)
└── No (continuous)
    ├── Comparing to a known mean?
    │   ├── Large sample (n > 30) → Z-Test
    │   └── Small sample → One-Sample T-Test
    ├── Comparing two groups?
    │   ├── Independent groups, normal → Independent T-Test
    │   ├── Paired / repeated measures, normal → Paired T-Test
    │   ├── Independent groups, non-normal → Mann-Whitney U
    │   └── Paired, non-normal → Wilcoxon Signed-Rank
    ├── Comparing three or more groups?
    │   ├── Normal → ANOVA (One-Way or Two-Way)
    │   └── Non-normal → Kruskal-Wallis
    ├── Comparing variances? → F-Test
    ├── Measuring association?
    │   ├── Linear relationship → Pearson Correlation
    │   └── Monotonic / non-normal → Spearman Rank Correlation
    └── Comparing survival curves? → Log-Rank Test
```

---

## 📋 Tests Covered

### Parametric Tests *(assume normality)*

| Test | Use Case | Key Assumption |
|------|----------|----------------|
| **Z-Test** | Sample mean vs. population mean | n > 30, known σ |
| **One-Sample T-Test** | Group mean vs. known value | Normal distribution |
| **Independent T-Test** | Two independent group means | Normal, equal-ish variance |
| **Paired T-Test** | Same group, two time points | Normal differences |
| **One-Way ANOVA** | 3+ group means, one factor | Normal, homoscedastic |
| **Two-Way ANOVA** | 3+ group means, two factors | Normal, homoscedastic |
| **F-Test** | Comparing two variances | Normal distribution |

### Non-Parametric Tests *(distribution-free)*

| Test | Parametric Equivalent | Use Case |
|------|----------------------|----------|
| **Mann-Whitney U** | Independent T-Test | Two independent groups, non-normal |
| **Wilcoxon Signed-Rank** | Paired T-Test | Paired samples, non-normal |
| **Kruskal-Wallis** | One-Way ANOVA | 3+ groups, non-normal |
| **Spearman Correlation** | Pearson Correlation | Monotonic relationships |

### Association & Survival

| Test | Use Case |
|------|----------|
| **Chi-Square (GoF)** | Does observed match expected distribution? |
| **Chi-Square (Independence)** | Are two categorical variables associated? |
| **Pearson Correlation** | Strength of linear relationship |
| **Log-Rank Test** | Compare survival curves between groups |

---

## ⚡ Quick-Start Example

```python
from scipy import stats
import numpy as np

# Independent T-Test: do two groups have different means?
group_a = np.array([23, 25, 28, 22, 27, 30])
group_b = np.array([30, 35, 33, 28, 32, 36])

t_stat, p_value = stats.ttest_ind(group_a, group_b)

print(f"T-statistic: {t_stat:.4f}")
print(f"P-value:     {p_value:.4f}")

if p_value < 0.05:
    print("✅ Reject H₀ — significant difference between groups")
else:
    print("❌ Fail to reject H₀ — no significant difference")
```

---

## 🛠️ Installation

```bash
git clone https://github.com/alketcecaj12/YetAnotherStatisticsRepo.git
cd YetAnotherStatisticsRepo

pip install scipy numpy pandas matplotlib seaborn jupyter

jupyter notebook
```

---

## 🔑 Core Concepts at a Glance

| Concept | Meaning |
|---------|---------|
| **H₀ (Null hypothesis)** | No effect / no difference |
| **H₁ (Alternative hypothesis)** | There is an effect / difference |
| **p-value** | Probability of observing the data if H₀ is true |
| **α (significance level)** | Threshold — typically 0.05 |
| **Type I Error** | Rejecting H₀ when it's actually true (false positive) |
| **Type II Error** | Failing to reject H₀ when it's actually false (false negative) |
| **Statistical power** | Probability of correctly detecting a real effect |

---

## 👤 Author

**Alket Cecaj**  
Quantitative Risk Analyst & Data Scientist | PhD | Copenhagen  
📎 [GitHub @alketcecaj12](https://github.com/alketcecaj12)

---

## ⭐ Found it useful? Give it a star and save yourself a Google search next time.
