# IBM HR Attrition Analysis

End-to-end analysis of IBM HR data: EDA, attrition prediction model, and an interactive dashboard.

## Problem
Why do employees leave, and can we predict who is likely to?

## Dataset
IBM HR Analytics Employee Attrition dataset (Kaggle), 1,470 employees, 35 features.

## What I Did
- **Analysis:** explored the data to find what drives attrition
- **Prediction:** built a model with Logistic Regression to predict who will leave
- **Dashboard:** built an interactive dashboard in Power BI

## Summarized Findings
  **Problem:**
    - Employee attrition is heavily concentrated among younger, overworked, and undercompensated mid-level staff. Baseline unmitigated turnover costs       the organization $253,000(assumed figures) on holdout evaluation data alone, driven primarily by burnout, travel fatigue, and severe compensation compression.

  **Approach:**
    - Developed an interpretable risk-scoring model combined with financial threshold optimization (t = 0.45). By mapping model outputs directly to         level-specific intervention costs and replacement expenses, the pipeline targets retention resources strictly where financial ROI is maximized.
    
  **Key Findings:**
    - Financial Impact: Deploying the model-driven strategy reduces total turnover expenditures from 253,000 to 139,100, achieving a 45.02% net cost        reduction ($113,900 net savings).
    - Primary Risk Drivers: Overtime is the single largest operational catalyst—high-risk employees are 4.6x more likely to work overtime (49.39% vs        11.88%). Frequent business travel increases attrition odds by 2.14x 28.28% vs 11.55%
    - Compensation Gap: High-risk personnel face a 42.67% monthly pay deficit (4,741/month vs 8,270/month baseline), making them highly susceptible         to external recruitment.
      
  **Recommendation:**
    - Targeted Overtime Caps: Mandate workload reviews for staff logging consistent overtime, as workload stress represents the single highest              operational flight risk.
    - Selective Pay Adjustment: Allocate intervention budgets toward recalibrating salary compression for mid-30s employees in high-demand roles            before they reach exit intent.
    - Deployment Strategy: Operationalize the $0.45$ probability threshold in HR systems to automatically trigger proactive retention interventions         for flagged high-risk staff.

## Model Results (On Test Set)
- Model: Logistic Regression
- Accuracy: 72.1%
- Recall: 82.9%

## Cost Effect of model

<img width="327" height="91" alt="Cost effect of model on test" src="https://github.com/user-attachments/assets/b7f582c3-efff-471e-a89b-47e1a6c59a38" />

## Dashboard
![Dashboard](images/dashboard.png)

## Tools
Python, pandas, scikit-learn, Power BI
