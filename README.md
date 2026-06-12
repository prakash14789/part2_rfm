# Part 2: RFM Segmentation & Retention Strategy

## Project Objective

The objective of this project is to identify customer groups requiring retention attention before deploying a machine learning churn prediction model.

The analysis combines traditional RFM metrics with behavioural and support signals to create actionable customer segments and recommend targeted retention strategies.

---

## Business Problem

Customer churn directly impacts revenue and customer lifetime value.

Before building a predictive churn model, the business wants to understand:

- Which customers are most valuable?
- Which customers are showing signs of churn risk?
- Which customers should receive retention attention first?
- How should a limited retention budget be allocated?

To answer these questions, customer segmentation was performed using RFM analysis and additional behavioural indicators.

---

## Dataset

Dataset source: https://drive.google.com/drive/folders/1PmLapJI1VSDgvl_AxARNKwM1MCd3WFX0?usp=sharing

The project uses the following four datasets:

| File | Description |
|---|---|
| customers.csv | Customer-level demographic and account information |
| orders.csv | Order history used to create RFM metrics and behavioural features |
| support_tickets.csv | Customer support interactions used to identify dissatisfaction signals |
| web_events_snapshot.csv | Website activity and campaign engagement data |

---

## Methodology

### Step 1: RFM Feature Creation

Three core RFM metrics were created for every customer using data on or before the snapshot date of **2025-09-30** to prevent data leakage.

| Metric | Definition |
|---|---|
| Recency | Days since last purchase before snapshot date |
| Frequency | Total number of completed orders |
| Monetary | Total customer spend in ₹ |

---

### Step 2: Additional Behavioural Signals

To improve segmentation quality, six additional non-RFM features were engineered:

| Feature | Source | Purpose |
|---|---|---|
| Return Rate | orders.csv | Measures refund and return behaviour |
| Average Discount Usage | orders.csv | Identifies discount dependency |
| Category Diversity | orders.csv | Measures breadth of purchasing behaviour |
| Ticket Count | support_tickets.csv | Measures volume of support interactions |
| Negative Ticket Rate | support_tickets.csv | Measures customer dissatisfaction level |
| Sessions (30 Days) | web_events_snapshot.csv | Website engagement signal |
| Campaign Clicks (30 Days) | web_events_snapshot.csv | Marketing engagement signal |

---

### Step 3: Customer Segmentation

Six customer segments were created using a rule-based approach with quantile thresholds applied to RFM and behavioural features.

| Segment | Definition |
|---|---|
| Champions | Recency ≤ 20th percentile, frequency ≥ 80th percentile, monetary ≥ 80th percentile, sessions ≥ 80th percentile |
| Loyal Customers | Frequency ≥ 80th percentile and campaign clicks ≥ 80th percentile |
| High Value But Unhappy | Monetary ≥ 80th percentile with tickets ≥ 2, return rate ≥ 20%, or negative ticket rate ≥ 50% |
| At-Risk High Value | Monetary ≥ 80th percentile and recency ≥ 80th percentile |
| Discount Sensitive | Average discount percentage ≥ 80th percentile |
| Dormant Customers | All remaining customers not meeting the above conditions |

---

## Segment Distribution

| Segment | Customers | Avg Monetary |
|---|---:|---:|
| Dormant Customers | 1,479 | ₹1,950 |
| Discount Sensitive | 421 | ₹1,351 |
| Loyal Customers | 258 | ₹4,880 |
| High Value But Unhappy | 184 | ₹5,790 |
| Champions | 47 | ₹6,075 |
| At-Risk High Value | 11 | ₹5,165 |

---

## Retention Strategy Summary

Each segment receives a targeted retention approach based on its behavioural profile.

| Segment | Retention Action |
|---|---|
| Champions | VIP rewards, early product access, referral incentives |
| Loyal Customers | Cross-selling, loyalty-point boosters, personalized recommendations |
| At-Risk High Value | Personalized win-back campaigns, direct outreach, premium offers |
| Discount Sensitive | Controlled promotional offers, seasonal discounts |
| High Value But Unhappy | Service recovery, complaint resolution, customer success intervention |
| Dormant Customers | Low-cost reactivation campaigns, reminder emails |

Full segment-level reasoning, expected business value, and budget allocation are documented in `retention_strategy.md`.

---

## Campaign Budget Prioritization

Assumed retention budget: **₹50,000**

| Priority | Segment | Budget | Rationale |
|---|---|---:|---|
| 1 | At-Risk High Value | ₹8,000 | Highest revenue recovery per customer |
| 2 | High Value But Unhappy | ₹15,000 | Largest revenue at risk — urgent intervention needed |
| 3 | Champions | ₹7,000 | Protect highest-value active customers |
| 4 | Loyal Customers | ₹12,000 | Large responsive segment with growth potential |
| 5 | Discount Sensitive | ₹5,000 | Controlled promotions only |
| 6 | Dormant Customers | ₹3,000 | Low-cost email to top 20% by monetary value only |
| | **Total** | **₹50,000** | |

---

## Manual Review Cases

Automated segmentation cannot fully capture every customer situation.

Ten customers showing conflicting behavioural signals were selected for manual review. Examples include:

- Customers with high engagement but low purchase conversion
- High-value customers with negative support sentiment
- Customers whose recent activity directly contradicts their assigned segment label
- Customers with 100% return rates still actively browsing the site

Dataset-backed case-by-case reasoning for all 10 customers is documented in `manual_review_cases.md`.

---

## Repository Structure

```
part2_rfm/
│
├── README.md                        # Project overview and methodology
├── rfm_segmentation.ipynb           # Full analysis notebook
├── segments.csv                     # Customer-level segment assignments
├── retention_strategy.md            # Segment retention actions and budget plan
├── manual_review_cases.md           # 10 dataset-backed manual review cases
├── manual_review_customers.csv      # Data table for manual review customers
├── requirements.txt                 # Python dependencies
│
└── charts/
    └── rfm_distribution.png         # Recency, frequency, monetary distributions
```

---

## Key Deliverables

### rfm_segmentation.ipynb
Complete analysis notebook containing:
- RFM feature creation with data leakage prevention
- Behavioural and support signal engineering
- Rule-based customer segmentation with quantile thresholds
- Visual analysis of RFM distributions and segment profiles
- Segment summary table with mean values per group
- Manual review customer identification and export

### segments.csv
Customer-level segmentation output containing:
- `customer_id`, `segment_name`
- RFM metrics: `recency`, `frequency`, `monetary`
- Behavioural features: `return_rate`, `avg_discount_pct`, `category_diversity`
- Support features: `ticket_count`, `negative_ticket_rate`
- Engagement features: `sessions_30d`, `campaign_clicks_30d`

### retention_strategy.md
Contains for each segment:
- Customer behaviour description
- Recommended retention action
- Expected business value with actual customer counts and spend figures
- Full budget allocation table with justification

### manual_review_cases.md
Ten customers with dataset-backed reasoning including exact figures for recency, frequency, monetary value, discount usage, ticket count, negative sentiment rate, sessions, and campaign clicks for each case.

---

## Technologies Used

| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| Pandas | Data manipulation and feature engineering |
| NumPy | Numerical operations |
| Matplotlib | Chart generation |
| Seaborn | Statistical visualisation |
| Jupyter Notebook | Interactive analysis environment |

---

## How to Run

```bash
# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook rfm_segmentation.ipynb
```

Data files are located in the `data/` folder at the root of the project:

```
data/
├── customers.csv
├── orders.csv
├── support_tickets.csv
├── web_events_snapshot.csv
├── churn_labels.csv
├── intervention_history.csv
└── rfm_modeling_snapshot.csv
```

The notebook reads from the `data/` folder at the root of the project.

---

## Conclusion

RFM analysis combined with behavioural and support signals provides a practical framework for identifying retention opportunities before a machine learning churn model is deployed.

The resulting segmentation enables targeted retention actions, efficient budget allocation, and focused customer review — delivering immediate business value without requiring a predictive model.