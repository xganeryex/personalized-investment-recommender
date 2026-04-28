# Personalised Asset Advisory using Recommendation Systems

## Overview

This project builds a **personalised investment recommendation system** that suggests financial assets tailored to each investor’s **risk profile, behavior, and historical performance**.

Unlike traditional recommenders that optimise for clicks or popularity, this system integrates **financial profitability and risk awareness**, enabling more realistic and actionable investment recommendations.

---

## Problem Statement

Investors face challenges in selecting assets that:

* Align with their **risk tolerance**
* Match their **investment behavior**
* Maximize **long-term profitability**

We formulate this as a **hybrid recommendation problem**, balancing:

* Personalization (user preferences)
* Financial return (profitability)

---

## Solution Approach

### Pipeline

1. Data preprocessing & feature engineering
2. Investor segmentation using K-Means
3. Collaborative Filtering (User-CF & Item-CF)
4. Profitability & risk-aware weighting
5. Hybrid recommendation system

---

## Dataset

* ~30,000 investors
* ~400,000 transactions
* Asset + market data

 Source: University of Glasgow Investment Dataset

---

## Key Features Engineering

* Cumulative profitability
* Asset risk (volatility)
* ROI metrics (absolute & %)
* Transaction behavior (frequency, interval)

These features enable **financially-aware personalization**, beyond standard recommender systems. 

---

## Models

### 1. Baseline

* Global popularity
* Recent popularity (30-day)

### 2. Collaborative Filtering

* User-based CF (behavior similarity)
* Item-based CF (co-investment patterns)

### 3. Hybrid Model 

Combines:

* User-CF (personalization)
* Item-CF (stability)
* Profit & risk priors

---

## Results

| Metric       | Baseline | Hybrid Model |
| ------------ | -------- | ------------ |
| Precision@10 | ~0.025   | **~0.145**   |
| Recall@10    | ~0.12    | **~0.62**    |
| Hit Rate@10  | ~0.21    | **~0.79**    |

✅ **~5–6× improvement over baseline**
✅ Strong balance between **accuracy and profitability** 

---

##  Key Insights

* User behavior similarity is more informative than asset similarity
* Profit-weighted recommendations improve real-world usefulness
* Hybrid model balances:

  * Personalization
  * Financial return
  * Risk control

Optimal configuration:

* **User-CF : Item-CF ≈ 0.8 : 0.2** 

---

## Project Structure

```
project/
│
├── notebooks/        # Colab notebooks
├── data/             # Dataset (if included / sample only)
├── src/              # Model implementation
├── README.md
```

---

## Tech Stack

* Python
* Pandas / NumPy
* Scikit-learn
* Recommender Systems (CF, Hybrid)

---

## Evaluation Metrics

* Precision@K
* Recall@K
* Hit Rate@K
* Pref@K (preference alignment)
* Profit@K (financial return)
* Score@K (combined objective)

---

## Why This Project Matters

Traditional recommenders optimise for engagement.
This project demonstrates how to:

Integrate **machine learning + finance**
Align recommendations with **real-world profitability**
Build systems closer to **real financial advisory tools**

---

## Future Improvements

* Deep learning recommender (Neural CF)
* Real-time recommendation system
* Portfolio optimization layer
* Live market data integration

---
