# DA5401 Assignment 4 — GMM-Based Synthetic Sampling

**Student:** Harshit Shukla  
**Roll No:** DA25S003  
**Topic:** Credit Card Fraud Detection with Imbalanced Data

---

## Project Overview

This assignment explores the challenge of **highly imbalanced datasets** (fraud detection).  
The workflow is divided into three main parts:

### Part A — Baseline Analysis
- Loaded the `creditcard.csv` dataset (PCA-transformed features).
- Explored class distribution and confirmed extreme imbalance (fraud ≪ non-fraud).
- Trained a **baseline Logistic Regression** on the imbalanced data.
- Showed why **accuracy is misleading** in imbalanced problems, and emphasized **precision, recall, F1** for the minority class.
- Plotted class distribution, Precision–Recall curve, and ROC curve.

### Part B — Synthetic Sampling with GMM
- Extracted minority (fraud) and majority (non-fraud) subsets from training data.
- Scaled minority data and fit a **Gaussian Mixture Model (GMM)**.
- Used **BIC/AIC** to select the optimal number of mixture components.
- Performed **clustering-based undersampling (CBU)** of the majority class using KMeans.
- Generated **synthetic minority samples** from the fitted GMM to balance the training data.
- Constructed a new balanced training dataset.

### Part C — Evaluation and Comparison
- Trained Logistic Regression on the balanced dataset (pipeline: StandardScaler + LogisticRegression).
- Evaluated model on the original imbalanced test set.
- Compared **precision, recall, F1** of baseline vs. GMM-balanced model.
- Plotted bar charts for metrics comparison.

---

## Key Insights
- **Baseline model:** High accuracy but very low recall for frauds (misses most fraud cases).
- **Balanced model:** Recall improves significantly, precision may decrease (trade-off), but F1 usually improves — more useful for fraud detection where missing fraud is very costly.
- **Conclusion:** GMM-based synthetic sampling + CBU is effective in handling imbalance, but care is needed to avoid synthetic overfitting.

---

## Files
- `da25s003_A4_completed.ipynb` — Main notebook with all code, figures, explanations (Parts A, B, C).
- `DA5401 A4 GMM.pdf` — Task description (assignment sheet).
- `README.md` — This documentation.

---

## How to Run
1. Create a virtual environment and install dependencies:
   ```bash
   python -m venv .venv
   source .venv/bin/activate      # Linux/macOS
   .venv\Scripts\Activate.ps1   # Windows PowerShell

   pip install -r requirements.txt
   ```

2. Launch Jupyter or open in VS Code:
   ```bash
   jupyter notebook da25s003_A4_completed.ipynb
   ```

3. Run all cells in order.

---
