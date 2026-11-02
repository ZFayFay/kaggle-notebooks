# Synthetic vs original: does it help? (Playground S6E11, credit card fraud)

**Kaggle:** https://www.kaggle.com/code/zfayfay/s6e11-synthetic-vs-original-does-it-help
**Competition:** Playground Series S6E11 – Predicting Credit Card Fraud (ROC AUC)

Playground data is generated from an original dataset. Before heavy modelling, three questions:

1. **What drifted?** Money columns moved most: `amount_usd` (KS 0.38), `account_balance_usd` (0.19), `distance_from_home_km` (0.16).
   A model separates competition rows from original rows with **AUC 0.90**; train vs test is **0.50** (no shift).
2. **Is the fraud signal the same?** Mostly yes (merchant risk, velocity, CVV retries lead in both).
   `customer_age` is much stronger in the competition data; `time_of_day_hour` only matters in the original.
3. **Do the original rows help?** No: CV AUC 0.94619 without vs 0.94604 with (same folds).

Baseline: LightGBM, 5-fold stratified CV, no feature engineering.
