BUSINESS CHALLENGE
Company A faced a 49.56% customer churn rate within 31-60 days across 100,000 subscribers, risking significant recurring revenue loss in a market where acquiring new customers costs 5-7x more than retention.

TECHNICAL APPROACH
• Data Integration & Cleaning: Merged Client and Record tables (100,000 rows × 100 features) via 1:1 key validation, handled >30% missing values using median/constant imputation with missingness indicators, and reduced high-cardinality categories.
• Feature Engineering: Created 16 behavioral and billing ratios (e.g., drop_rate, overage_rev_ratio, recent_usage_trend, custcare_per_attempt) to capture early silent-attrition signals.
• Modeling & Optimization: Benchmarked Logistic Regression, Random Forest, and XGBoost using Stratified 5-Fold Cross-Validation and out-of-fold F1 threshold tuning (optimal threshold: 0.358).

KEY RESULTS & BUSINESS IMPACT
• Model Performance: Tuned XGBoost achieved 0.6965 ROC-AUC, 0.6843 PR-AUC, and 89.21% Recall (capturing 8,842 of 9,912 churners in the hold-out test set).
• Actionable Strategy: Identified device age (eqpdays), contract renewal window (months 10-15), and usage drops (change_mou) as primary churn drivers, formulating the "SMART-Retain" 3-tier intervention engine projected to generate +118.6% ROI.
