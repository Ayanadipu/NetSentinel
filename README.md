# NetSentinel: Phishing Website Detection

## Overview
NetSentinel is a machine learning classification project that distinguishes phishing websites from legitimate websites using URL, domain, security, and webpage-related features.

## Dataset
- **Dataset:** Phishing Websites — Training Dataset
- **Samples:** 11,055
- **Input features:** 30
- **Target:** `Result`
- **Class labels:** -1 and +1, mapped to 0 (phishing) and 1 (legitimate) for evaluation.
- **Missing values:** None reported in the initial inspection.

## Methodology
1. Inspected the dataset, feature types, class distribution, and duplicates.
2. Split the data into training and test sets using stratified sampling (80/20).
3. Built a Logistic Regression baseline.
4. Compared it with an RBF-kernel Support Vector Machine (SVM).
5. Tuned the SVM using five-fold stratified cross-validation and F1-score.
6. Evaluated the selected model on the held-out test set.

## Evaluation
Models were compared using accuracy, precision, recall, and F1-score. The tuned SVM was selected using cross-validation, not test-set performance.

### Results
Add the actual values from `reports/results/model_comparison.csv` here.

## Limitations
- Results depend on the dataset's representativeness and quality.
- Duplicate rows require careful treatment to avoid overly optimistic evaluation.
- High test performance does not guarantee reliable detection on previously unseen phishing techniques.

## Reproducibility
The analysis is provided in `notebooks/01_phishing_detection.ipynb`. Dependencies are managed using `uv` and listed in `pyproject.toml`.
