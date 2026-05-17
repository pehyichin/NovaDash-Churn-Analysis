![Python](https://img.shields.io/badge/Python-3.x-blue)
![Tableau](https://img.shields.io/badge/Tableau-Public-orange)
![SQL](https://img.shields.io/badge/SQL-SQLite-lightgrey)

## Company Info
<img width="300" alt="NovaDash-lockup-light" src="https://github.com/user-attachments/assets/8b1709e4-6e72-44fd-be2a-6936cf07bbae" />

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
[View Dashboard on Tableau Public](https://public.tableau.com/app/profile/yichin.peh/viz/NovaDash_tableau_TBD/Dashboard1)

<img width="1873" height="2030" alt="Dashboard 1" src="https://github.com/user-attachments/assets/23ad68dc-3337-49cf-8ec4-d77ed704d165" />

*Figure 1: NovaDash Churn Analysis Dashboard*

> 22% overall churn rate — 110 customers lost, representing $2.76M in annual recurring revenue.**
- **DevTools has the highest churn rate at 31%**, particularly among event (43%) and ad-acquired accounts (38%).
- **46.7% of churn occurs within the first 90 days** — indicating an onboarding and activation gap.
- **No single churn driver dominates** — budget, features, and support each account for 21% of churned accounts with a recorded reason.
- **33% of churned accounts made a subscription change in the 90 days before leaving** — more upgraded (21%) than downgraded (12%), suggesting unmet product expectations rather than budget constraints.
- **80% of subscription changes among long-tenure churners were downgrades** — a leading indicator of impending cancellation.
- **DevTools accounts for the largest absolute revenue loss at $61K** — a volume problem.
- **Each Cybersecurity churn costs $2.6K** — the highest of any industry, making it a value problem.
- **Long-tenure accounts (365+ days) carry the highest revenue loss rate at 36.1%** — each departure carries disproportionate individual impact.
- **88.5% of reactivated accounts remain retained** — win-back efforts show strong potential.


## Recommendations

Based on the findings, four strategic layers are proposed to address NovaDash's retention problem across the full customer lifecycle from acquisition to recovery.

| Layer | Focus |
|---|---|
| 1. Acquire the Right Customers | Improve lead quality and channel mix to reduce structural churn risk at the source |
| 2. Accelerate Early Value Realization | Reduce dropout in the critical 0–90 day window through onboarding and activation improvements |
| 3. Protect High-Value Customer Relationships | Retain long-tenure and high-value accounts through dedicated success management and proactive engagement |
| 4. Learn From and Recover Lost Customers | Close the feedback gap and convert churned accounts into reactivation opportunities |

### 1. Acquire the Right Customers

<img width="710" height="279" alt="image" src="https://github.com/user-attachments/assets/e5a9ea8b-e0f4-43cc-921f-29567f1d0eff" />

*Figure 2: Churn Rate by Industry and Referral Source — DevTools and Event Channel Carry Highest Risk*

- Shift acquisition focus from volume to fit

  Event and ads channels produce the highest churn rates (30–43%) while partner and organic referrals retain significantly better (13–17%). Refining the acquisition channel mix, introducing lightweight qualification criteria for high-churn channels, and redesigning event flows to emphasise product understanding over immediate sign-ups may collectively improve the quality of incoming accounts without necessarily increasing acquisition cost.
  
  **Priority: Medium-term — requires marketing and sales alignment.**

- Develop a clearer Ideal Customer Profile (ICP)

  Retention and churn patterns suggest that certain industries - particularly Cybersecurity and EdTech, demonstrate stronger retention quality despite smaller account volume. Formalising these observations into a defined ICP can guide targeting strategy, acquisition messaging, and onboarding expectations, reducing structural churn risk at the source.
  
  **Priority: Long-term — requires cross-functional alignment.**

### 2. Accelerate Early Value Realization
<img width="508" height="285" alt="image" src="https://github.com/user-attachments/assets/1fd2c398-0577-48e6-8185-9bf5724d29c2" />

*Figure 3: Churn Rate by Tenure Bucket — 46.7% of Churn Occurs Within the First 90 Days*


- Redesign onboarding around early value realization

    Nearly half of all churn occurs within the first 90 days, and early-stage accounts that upgraded their plan before churning still failed to find sufficient value, indicating an activation problem rather than a pricing one. NovaDash should prioritise getting new accounts to their first meaningful workflow output within the first two weeks, through a guided onboarding path tailored by industry vertical. Defining and tracking specific activation milestones such as completing a first automated workflow, inviting a second team member, or integrating with an existing tool creates measurable checkpoints that surface at-risk accounts before they reach the cancellation decision.

  **Priority: High - directly addresses the largest churn window. Requires product instrumentation and cross-functional definition of success metrics.**

<img width="496" height="291" alt="image" src="https://github.com/user-attachments/assets/f9e522f5-ac3a-4f3c-a1f1-a94ab75318a5" />

*Figure 4: Pre-Churn Subscription Changes — More Accounts Upgraded Than Downgraded Before Leaving*

- Implement structured touchpoints and early subscription change monitoring

    Structured outreach at day 14, day 30, and day 60 for all new accounts with a technical review component for DevTools accounts specifically can create proactive intervention opportunities before dissatisfaction escalates. Subscription changes in the first 90 days should be monitored as risk signals: an upgrade event warrants immediate outreach to ensure the higher tier delivers on expectations, while a downgrade event can trigger an automated low-touch follow-up at negligible operational cost.
  
  **Priority: High - process-driven with minimal investment. Audit of upgrade flow requires no product changes.**


### 3. Protect High-Value Customer Relationships

<img width="523" height="259" alt="image" src="https://github.com/user-attachments/assets/13de1590-d4b4-4898-ad24-e38d58b15ac2" />

*Figure 5: MRR Lost per Churned Account by Industry — Cybersecurity Accounts Carry the Highest Individual Revenue Risk at $2.6K*

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
