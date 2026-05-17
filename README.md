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

| Layer | Focus |
|---|---|
| 1. Acquire the Right Customers | Improve lead quality and channel mix to reduce structural churn risk at the source |
| 2. Accelerate Early Value Realization | Reduce dropout in the critical 0–90 day window through onboarding and activation improvements |
| 3. Protect High-Value Customer Relationships | Retain long-tenure and high-value accounts through dedicated success management and proactive engagement |
| 4. Learn From and Recover Lost Customers | Close the feedback gap and convert churned accounts into reactivation opportunities |

### 1. Acquire the Right Customers
- Shift acquisition focus from volume to fit

  Event and ads channels produce the highest churn rates (30–43%) while partner and organic referrals retain significantly better (13–17%). Refining the acquisition channel mix, introducing lightweight qualification criteria for high-churn channels, and redesigning event flows to emphasise product understanding over immediate sign-ups may collectively improve the quality of incoming accounts without necessarily increasing acquisition cost.
  
**Priority: Medium-term — requires marketing and sales alignment.**

- Develop a clearer Ideal Customer Profile (ICP)

  Retention and churn patterns suggest that certain industries - particularly Cybersecurity and EdTech, demonstrate stronger retention quality despite smaller account volume. Formalising these observations into a defined ICP can guide targeting strategy, acquisition messaging, and onboarding expectations, reducing structural churn risk at the source.
  
**Priority: Long-term — requires cross-functional alignment.**

### 2. Accelerate Early Value Realization

- Redesign onboarding around early value realization

    Nearly half of all churn occurs within the first 90 days, and early-stage accounts that upgraded their plan before churning still failed to find sufficient value, indicating an activation problem rather than a pricing one. NovaDash should prioritise getting new accounts to their first meaningful workflow output within the first two weeks, through a guided onboarding path tailored by industry vertical. Defining and tracking specific activation milestones such as completing a first automated workflow, inviting a second team member, or integrating with an existing tool creates measurable checkpoints that surface at-risk accounts before they reach the cancellation decision.

**Priority: High - directly addresses the largest churn window. Requires product instrumentation and cross-functional definition of success metrics.**


- Implement structured touchpoints and early subscription change monitoring

    Structured outreach at day 14, day 30, and day 60 for all new accounts with a technical review component for DevTools accounts specifically can create proactive intervention opportunities before dissatisfaction escalates. Subscription changes in the first 90 days should be monitored as risk signals: an upgrade event warrants immediate outreach to ensure the higher tier delivers on expectations, while a downgrade event can trigger an automated low-touch follow-up at negligible operational cost.
  
**Priority: High - process-driven with minimal investment. Audit of upgrade flow requires no product changes.**


### 3. Protect High-Value Customer Relationships

- Invest in structured relationship management for long-tenure and high-value accounts

    Accounts churning after 365+ days carry the highest revenue loss rate at 36.1%, and Cybersecurity accounts represent the highest revenue loss per churn at USD 2.6K. Assigning dedicated Customer Success Managers (CSMs), conducting quarterly business reviews (QBRs), and introducing priority support SLAs for these segments creates a relationship infrastructure that surfaces retention risks earlier and signals to strategically important customers that their partnership is valued. Renewal conversations should be initiated several months before contract expiry, with loyalty incentives such as early renewal discounts or multi-year pricing structures available for high-value accounts.

**Priority: Medium-term — requires Customer Success capacity planning, SLA definition, and QBR framework.**

- Monitor downgrade events as early warning signals

    Among long-tenure churners, 80% made a downgrade before exiting - a classic cost-cutting signal preceding full cancellation. Instrumenting downgrade events as automated churn risk triggers for established accounts allows NovaDash to initiate proactive, personalised outreach before the cancellation decision is made, converting a reactive process into a predictive one.

**Priority: Quick win - requires CRM automation and workflow setup, no additional headcount.**

### 4. Learn From and Recover Lost Customers

- Close the feedback loop from collection to action

    35 of 110 churned accounts left no reason code, limiting analytical depth and intervention quality. Introducing a structured exit survey at the point of cancellation to improve visibility into churn drivers over time. Even a single mandatory churn reason field may meaningfully improve data quality over time. Critically, collected insights should be systematically shared with product, support, and customer success teams to ensure recurring pain points influence roadmap prioritisation, service improvements, and onboarding design. Feedback collection without a closed loop has limited organisational value.

**Priority: Quick win for collection, medium-term for cross-functional process alignment.**

- Expand or Formalise win-back initiatives

    Of 26 reactivated accounts, 88.5% are currently retained, suggesting that customers who return after churning tend to stay. A structured win-back campaign targeting recently churned accounts within 90 days of exit, with tailored messaging and low-friction re-entry incentives based on known churn reasons, may recover meaningful revenue at relatively low cost.

**Priority: Medium-term, requires campaign design and CRM segmentation.**
