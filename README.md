
# DA5401: Assignment 4

**GMM-Based Synthetic Sampling for Imbalanced Data**

* **Course:** DA5401
* **Topic:** Credit Card Fraud Detection
* **Name:** Harshit Shukla
* **Roll No.:** DA25S003

### Documentation of code:

1. **Data Prep**

   * Load dataset, 
   * check imbalance,
   * stratified split.

2. **Baseline**

   * Train simple model, evaluate with Precision, Recall, F1, ROC, PR.
   * Accuracy not reliable for imbalanced data.

3. **GMM Sampling**

   * Advantage over SMOTE: distribution-based.
   * Choose $K$ via AIC/BIC.
   * Fit GMM to minority class.
   * Oversampling + GMM + CBU hybrid.

4. **Comparison**

   * Methods: Baseline, SMOTE, GMM-Full, GMM+CBU.
   * Results: bar charts, ROC/PR curves (full + zoomed).

5. **Conclusion**

   * GMM creates realistic samples.
   * GMM+CBU balances performance.
   * Improves recall → better fraud detection.


Folder Structure:
```
|_Models    // saved models from Assignment3, Assignment4
|   |_baseline_model.pkl
|   |_gmm_full_lr.pkl
|   |_gmm_cbu_lr.pkl
|   |_smote_model.pkl
|   |_cbo_model.pkl
|   |_cbu_model.pkl
|_da25s004_A4.ipynb  // code file
|_model_summary.csv  // summary of evaluation metrices
|_README.md
```