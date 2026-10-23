# Boosting I - AdaBoost & Gradient Boosting
### Which streaming-service customers will churn? - learning from your own mistakes, one round at a time

**Dataset (provided separately):** `streaming_customers.csv` - 8000 subscribers of a video-streaming app:
- Features: `tenure_months`, `monthly_bill_rs`, `support_calls_3m`, `late_payments_6m`, `devices_linked`, `genres_watched`, `discount_active`, `app_crashes_last_month`
- `churned` (0/1) - did the customer cancel? (**classification** target)
- `monthly_watch_hours` - hours the customer watches per month (**regression** target)

**What this notebook covers (theory in markdown, then code):**
1. Boosting vs bagging - the big idea of **sequential learning**
2. **AdaBoost** - re-weighting the examples the last model got wrong (built from scratch, then sklearn)
3. **Gradient Boosting** - fitting each new tree to the leftover errors (residuals), built from scratch, then sklearn
4. Hyperparameters: `n_estimators`, `learning_rate`, `max_depth` - and how to tune them
5. Classification AND regression, compared against last class's **Random Forest**
6. Bagging vs boosting - a summary note

Two code cells hide a small deliberate bug marked `# FIX ME`, each with a hint. Find and fix both.