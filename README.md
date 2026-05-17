## Company Info
**NovaDash** is a B2B SaaS platform providing workflow automation and analytics tools to technology companies across Southeast Asia. Serving 500 enterprise and SME clients across five verticals — DevTools, FinTech, HealthTech, EdTech, and Cybersecurity — NovaDash has experienced rising churn over the past two quarters, prompting an urgent review by the Head of Customer Success.
    
## Dataset Info
    
[Simulated data for SaaS user behavior analysis](https://www.kaggle.com/datasets/rivalytics/saas-subscription-and-churn-analytics-dataset/data)
The dataset spans 5 CSV files:
- accounts.csv (500) – customer metadata
- subscriptions.csv (5,000) – subscription lifecycles and revenue
- feature_usage.csv (25,000) – daily product interaction logs
- support_tickets.csv (2,000) – support activity and satisfaction scores
- churn_events.csv (600) – churn dates, reasons, and refund behaviors
This dataset is fully synthetic and distributed under a permissive MIT-like license.

### Data Pipeline
SQL -> Python -> Tableau

## Objective
Identify the behavioural, demographic, and subscription-level signals that precede customer churn at NovaDash, and quantify the revenue impact to inform a targeted retention strategy.

## Key Findings
[NovaDash Churn Analysis Dashboard](https://public.tableau.com/app/profile/yichin.peh/viz/NovaDash_tableau_TBD/Dashboard1)

- DevTools has the highest churn rate (31%), particularly among event (43.5%) and ad-acquired accounts (38.5%).
- Nearly half of churn occurs within the first 90 days.
- Only 75 provided a reason code (68%), 35 left without providing any feedback.
- Budget, features, support each account for 21.3% of churn reasons.
- Of those 28 DevTools accounts, 25% cited missing features and 21.4% cited support-related issues.
- 21.3% of churned accounts upgraded within 90 days preceding churn, with most belonging to customers under 90 days tenure.
- 80% of subscription changes among long-tenure churners were downgrades.
- DevTools contributes the highest total revenue loss at $61K.
- Cybersecurity accounts generate the highest MRR loss per churned account ($2.6K).
- Accounts churning after 365+ days contribute the highest loss rate but relatively lower absolute churn volume.
- Of 26 reactivated accounts, 88.5% remain retained after returning.

## Recommendations

Based on the findings, four strategic layers are proposed to address NovaDash's 
retention problem across the full customer lifecycle from acquisition to recovery.

| Layer | Focus | Priority |
|---|---|---|
| 1. Acquire the Right Customers | Improve lead quality and channel mix to reduce structural churn risk at the source | Medium to long-term |
| 2. Accelerate Early Value Realization | Reduce dropout in the critical 0–90 day window through onboarding and activation improvements | High, immediate impact |
| 3. Protect High-Value Customer Relationships | Retain long-tenure and high-value accounts through dedicated success management and proactive engagement | Medium-term |
| 4. Learn From and Recover Lost Customers | Close the feedback gap and convert churned accounts into reactivation opportunities | Quick wins available |
