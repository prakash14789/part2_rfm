# Manual Review Cases

## Purpose
Certain customers display conflicting behavioural signals that make 
automated retention decisions difficult. These customers require manual 
review before assigning a final retention strategy.

---

## Customer: CUST00001
**Current Segment:** Discount Sensitive

**Data:**
- Recency: 107 days | Frequency: 6 orders | Monetary: ₹2,955
- Avg Discount: 36% | Ticket Count: 2 | Negative Ticket Rate: 50%
- Sessions (30d): 1 | Campaign Clicks: 0

**Why Review Is Needed:**
This customer has 6 orders and ₹2,955 in spend — Loyal-level 
frequency — but was assigned Discount Sensitive due to 36% avg 
discount. At the same time, 2 support tickets with 50% negative 
sentiment indicate growing dissatisfaction. The segment misses the 
service risk entirely. Without intervention, a customer purchasing 
at this frequency could churn silently.

**Recommended Action:**
Targeted retention offer combined with a proactive customer support 
follow-up to resolve the outstanding dissatisfaction before it 
escalates.

---

## Customer: CUST00007
**Current Segment:** Dormant Customers

**Data:**
- Recency: 3 days | Frequency: 1 order | Monetary: ₹719
- Avg Discount: 18% | Ticket Count: 0 | Negative Ticket Rate: 0%
- Sessions (30d): 11 | Campaign Clicks: 3

**Why Review Is Needed:**
Recency of 3 days means this customer visited the site 3 days ago. 
They have 11 sessions and 3 campaign clicks in the last 30 days — 
the highest campaign engagement of any customer in the manual review 
list. Yet they have only 1 purchase. This is not a dormant customer; 
it is a warm prospect who is actively engaging but not converting. 
The Dormant label is likely incorrect.

**Recommended Action:**
Personalized product recommendations targeting their purchase 
category. Do not send a dormant win-back message — this customer 
is already engaged and needs a conversion nudge, not a reactivation.

---

## Customer: CUST00009
**Current Segment:** Discount Sensitive

**Data:**
- Recency: 31 days | Frequency: 1 order | Monetary: ₹376
- Avg Discount: 49% | Ticket Count: 0 | Negative Ticket Rate: 0%
- Sessions (30d): 11 | Campaign Clicks: 0

**Why Review Is Needed:**
This customer used a 49% discount on their only order and has 11 
sessions in 30 days but 0 campaign clicks. The conflict is between 
high browsing activity and zero campaign response — they are 
browsing independently but ignoring marketing emails. It is unclear 
whether a promotional campaign will convert them or whether they 
are waiting for a specific product to go on sale. Spending retention 
budget on a broad discount campaign may deliver no return.

**Recommended Action:**
Test a limited-time category-specific offer rather than a broad 
discount. Monitor click response before committing further spend.

---

## Customer: CUST00010
**Current Segment:** Discount Sensitive

**Data:**
- Recency: 9 days | Frequency: 1 order | Monetary: ₹636
- Avg Discount: 45% | Ticket Count: 0 | Negative Ticket Rate: 0%
- Sessions (30d): 13 | Campaign Clicks: 0

**Why Review Is Needed:**
Recency of 9 days and 13 sessions in 30 days shows this customer 
is actively using the site. However they have only 1 purchase and 
have never clicked a campaign. The 45% discount on that single 
order raises the question of whether they will only purchase again 
under heavy discount conditions. The decision between a conversion 
nudge and a discount offer is not obvious — one builds a habit, 
the other confirms discount dependency.

**Recommended Action:**
Send a conversion-focused recommendation email first without a 
discount. If no purchase within 14 days, follow up with a 
controlled promotional offer.

---

## Customer: CUST00011
**Current Segment:** Dormant Customers

**Data:**
- Recency: 1 day | Frequency: 2 orders | Monetary: ₹925
- Avg Discount: 15% | Ticket Count: 0 | Negative Ticket Rate: 0%
- Sessions (30d): 10 | Campaign Clicks: 0

**Why Review Is Needed:**
Recency of 1 day means this customer was on the site yesterday. 
They have 10 sessions in 30 days and the lowest avg discount (15%) 
of any customer in this review list — suggesting they are not 
purely discount-driven. Despite this, they have only 2 orders and 
0 campaign clicks. Calling this customer Dormant is factually wrong 
given their activity. They are a low-converter with clear intent, 
not an inactive customer.

**Recommended Action:**
Product discovery campaign targeting their purchase category. 
No discount needed given the low discount dependency — a 
well-timed recommendation is more appropriate.

---

## Customer: CUST00014
**Current Segment:** High Value But Unhappy

**Data:**
- Recency: 51 days | Frequency: 11 orders | Monetary: ₹8,130
- Avg Discount: 26% | Ticket Count: 2 | Negative Ticket Rate: 50%
- Sessions (30d): 11 | Campaign Clicks: 0

**Why Review Is Needed:**
This is the highest-spending customer in the manual review list at 
₹8,130 across 11 orders. They have 2 support tickets with 50% 
negative sentiment and 0 campaign clicks despite 11 sessions — 
indicating they are still browsing but have stopped responding to 
marketing. The segment assignment is correct, but the urgency is 
higher than a standard High Value But Unhappy case given the spend 
level. Every week without intervention increases churn probability.

**Recommended Action:**
Immediate service recovery outreach from a senior support 
representative. Acknowledge the complaint history explicitly. 
Offer account credit of ₹500–700 given the ₹8,130 lifetime value. 
Do not send a promotional email — this customer needs human contact.

---

## Customer: CUST00022
**Current Segment:** Dormant Customers

**Data:**
- Recency: 29 days | Frequency: 1 order | Monetary: ₹454
- Avg Discount: 31% | Ticket Count: 0 | Negative Ticket Rate: 0%
- Sessions (30d): 10 | Campaign Clicks: 1

**Why Review Is Needed:**
This customer clicked a campaign in the last 30 days and has 10 
sessions — they are not disengaged. Recency of 29 days means they 
purchased less than a month ago. The Dormant label appears 
incorrect. The non-obvious decision is whether to treat them as a 
new customer still evaluating the brand, or as a genuine dormant 
case. Given the campaign click, they have shown responsiveness to 
marketing, which dormant customers typically do not.

**Recommended Action:**
Low-cost follow-up email referencing their last purchase category. 
Given the single campaign click, a gentle nudge is more appropriate 
than a high-value win-back offer.

---

## Customer: CUST00024
**Current Segment:** Dormant Customers

**Data:**
- Recency: 4 days | Frequency: 1 order | Monetary: ₹481
- Avg Discount: 34% | Ticket Count: 0 | Negative Ticket Rate: 0%
- Sessions (30d): 13 | Campaign Clicks: 0

**Why Review Is Needed:**
Recency of 4 days and 13 sessions in 30 days makes this one of 
the most actively browsing customers in the entire manual review 
list. They have 0 campaign clicks despite the high session count — 
meaning they are arriving organically, not through marketing. 
Calling this customer Dormant directly contradicts their behaviour. 
The non-obvious question is why a customer with 13 sessions in 30 
days and a purchase 4 days ago has not repurchased.

**Recommended Action:**
Category-specific product recommendation based on their single 
purchase. No discount initially — test whether organic interest 
converts before offering promotions.

---

## Customer: CUST00025
**Current Segment:** Loyal Customers

**Data:**
- Recency: 165 days | Frequency: 7 orders | Monetary: ₹4,868
- Avg Discount: 31% | Ticket Count: 3 | Negative Ticket Rate: 67%
- Sessions (30d): 11 | Campaign Clicks: 1

**Why Review Is Needed:**
This customer has 7 orders and ₹4,868 spend which justifies the 
Loyal label. However, 165 days recency and 3 tickets with 67% 
negative sentiment are serious warning signals. The negative ticket 
rate of 67% is the highest of any Loyal customer in this review. 
Combined with 165 days since last purchase, this customer is 
closer to At-Risk than Loyal. The segment assignment understates 
the churn risk significantly.

**Recommended Action:**
Loyalty reward offer combined with a direct support follow-up 
addressing the 3 tickets. Do not send a standard loyalty campaign 
without resolving the dissatisfaction first — it will likely be 
ignored given the 165-day inactivity.

---

## Customer: CUST00027
**Current Segment:** Dormant Customers

**Data:**
- Recency: 70 days | Frequency: 1 order | Monetary: ₹2,128
- Avg Discount: 30% | Return Rate: 100% | Ticket Count: 1
- Negative Ticket Rate: 100% | Sessions (30d): 11 | Campaign Clicks: 2

**Why Review Is Needed:**
This customer spent ₹2,128 on a single order and returned all of 
it — 100% return rate. They also have 1 ticket with 100% negative 
sentiment. Despite this, they have 11 sessions and 2 campaign 
clicks in the last 30 days, meaning they are still browsing and 
engaging with marketing after a completely negative first 
experience. The non-obvious decision is whether the continued 
browsing signals intent to repurchase if the issue is resolved, 
or whether they are a fraud or serial-return risk.

**Recommended Action:**
Manual investigation of the return reason before allocating any 
retention budget. If the return was due to a product or delivery 
issue, a resolution offer may recover the customer. If the pattern 
suggests serial return behaviour, suppress from retention campaigns.