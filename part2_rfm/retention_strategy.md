# Retention Strategy

## Overview

Customer segmentation was performed using RFM metrics combined with behavioural signals including support complaints, return rate, website activity, campaign engagement, category diversity, and discount usage.

The objective is to identify customer groups requiring different retention approaches and optimize a limited retention budget before deploying a machine learning churn prediction model.

---

## Segment Retention Actions

| Segment                | Customer Behaviour                                                                  | Recommended Retention Action                                                              | Expected Business Value                                                                                                                       
| ---------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Champions              | Recent, frequent, high-spending customers with strong website engagement            | VIP rewards, early access to new products, referral incentives, premium loyalty benefits  | 47 customers averaging ₹6,075 spend. Approximate segment value ≈ ₹285,525. Retaining a small number of Champions protects significant revenue and encourages referrals. |
| Loyal Customers        | Frequent purchasers with strong campaign engagement and stable purchasing behaviour | Cross-selling, bundle offers, loyalty-point boosters, personalized recommendations        | 258 customers averaging ₹4,880 spend. Approximate segment value ≈ ₹1.26 million. Increasing purchase frequency can substantially improve customer lifetime value.       |
| At-Risk High Value     | Historically valuable customers showing long inactivity periods                     | Personalized win-back campaigns, premium offers, direct outreach, account-level follow-up | 11 customers averaging ₹5,165 spend. Approximate segment value ≈ ₹56,815. Small segment size but very high recovery value per customer.                                 |
| Discount Sensitive     | Customers whose purchasing behaviour is heavily influenced by discounts             | Targeted coupons, seasonal promotions, limited-time offers, controlled discounting        | 421 customers averaging ₹1,351 spend. Approximate segment value ≈ ₹568,771. Revenue can be maintained through efficient promotion strategies.                           |
| High Value But Unhappy | High-spending customers with complaints, returns, or negative support signals       | Service recovery, issue resolution, customer-success intervention, selective compensation | 184 customers averaging ₹5,790 spend. Approximate segment value ≈ ₹1.07 million. Recovering dissatisfaction in this segment protects substantial revenue.               |
| Dormant Customers      | Low engagement and weak recent purchasing behaviour                                 | Low-cost reactivation campaigns, reminder emails, product recommendations                 | 1,479 customers averaging ₹1,950 spend. Approximate segment value ≈ ₹2.88 million, but recovery probability is lower than other segments.                               |

---

## Campaign Budget Prioritization

Assume a total retention budget of **₹50,000**.

### Priority Order

1. At-Risk High Value
2. High Value But Unhappy
3. Champions
4. Loyal Customers
5. Discount Sensitive
6. Dormant Customers

### Budget Allocation

| Segment                | Suggested Spend | Retention Approach                                      |
| ---------------------- | --------------: | ------------------------------------------------------- |
| At-Risk High Value     |          ₹8,000 | Personalized win-back campaigns and direct outreach     |
| High Value But Unhappy |         ₹15,000 | Service recovery, issue resolution, compensation offers |
| Champions              |          ₹7,000 | VIP programs, loyalty rewards, referral incentives      |
| Loyal Customers        |         ₹12,000 | Cross-selling campaigns and loyalty boosters            |
| Discount Sensitive     |          ₹5,000 | Controlled promotional campaigns                        |
| Dormant Customers      |          ₹3,000 | Low-cost email reactivation campaigns                   |
| **Total**              |     **₹50,000** |                                                         |

---

## Budget Justification

The highest investment is allocated to **High Value But Unhappy** customers because they represent approximately ₹1.07 million in historical spending while showing strong dissatisfaction signals. These customers remain valuable but are at elevated churn risk.

**At-Risk High Value** customers receive the second-highest priority because they have already demonstrated high spending behaviour and can often be recovered through timely intervention.

**Champions** and **Loyal Customers** are protected through loyalty and growth-focused initiatives because they contribute consistently to revenue and customer lifetime value.

**Discount Sensitive** customers receive controlled promotional spending because their purchasing behaviour is heavily discount-driven.

**Dormant Customers** receive the smallest allocation because their recovery probability is lower, making large retention investments less cost-effective.

---

## Expected Business Impact

The recommended strategy prioritizes customers with the highest combination of revenue contribution and churn risk. By focusing retention spending on At-Risk High Value and High Value But Unhappy customers first, the company can maximize potential revenue recovery while maintaining efficient marketing spend allocation.
