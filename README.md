# 🛡️ Credit Card Fraud Detection
### Machine Learning + Power BI Dashboard
 
> A project built while learning how computational economics actually works in the real world.
 
---
 
## A bit of context
 
I'm studying economics and I wanted to bridge the gap between theory and something tangible. This project started as a challenge: *can I build a real fraud detection system from scratch, with zero prior ML experience?*
 
Spoiler: yes. And it took way less time than I expected.
 
The idea is simple — every time you swipe your card, a model like this one decides in milliseconds whether you're buying a coffee or someone just stole your wallet. That's the kind of applied economics that actually moves money.
 
---
 
## What this project does
 
Takes 284,807 real European credit card transactions and trains a Random Forest model to classify each one as **legitimate or fraud** — then visualizes the economic impact of every mistake the model makes.

## Results
 
| Metric | Value |
|---|---|
| ROC-AUC Score | **0.9836** |
| Frauds Detected | **86 / 98** (87%) |
| Missed Frauds | 12 |
| False Alarms | 115 |
| 💰 Estimated Savings vs No Model | **$40,415** |

---
## Project structure
 
```
fraude_financiero/
│
├── creditcard.csv              ← dataset (not included, see below)
├── 01_exploracion.ipynb        ← EDA: distributions, imbalance, amounts
├── 02_modelo.ipynb             ← SMOTE + Random Forest + evaluation
└── outputs/
    ├── predictions.csv         ← model predictions with probabilities
    ├── confusion_matrix.csv    ← TP, FP, FN, TN counts
    ├── feature_importance.csv  ← top predictive variables
    └── economic_analysis.csv   ← cost model for Power BI
```
TO GET THE DATASET**
 
Download from Kaggle: [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
Place `creditcard.csv` in the project folder.

 ---
 
## Power BI Dashboard
 
Two pages built from the model outputs:
 
**Page 1 — Model Results**
- KPI cards: frauds detected, missed frauds, false alarms, true normal
- Feature importance (V14 is the most predictive variable by far)
- Fraud probability distribution
 
**Page 2 — Economic Impact Analysis**
- Cost of each type of error
- Model vs no-model total cost comparison
- Estimated savings
 
---

