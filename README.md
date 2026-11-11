# Insurance Pricing A/B-Test - Conversion and Profitability Analysis

**Tools:** Python, Pandas, NumPy, SciPy, Matplotlib, Jupyter Notebook

**Project type:** Academic case study

## Project Overview

This project evaluates the results of pricing expertiment for travel insurance policies. The business question is whether a test pricing approach should replace the existing one when both purchase conversion adn financial performance are considered.

The analysis combines experiment assignments, issued isurance contracts and insurance claim payouts. It compares control and test groups, estimates differnces in per-user business metrics, tests statistical significance and proposes a rollout decision.

> **Decision:** Do **not** roll out the test price yet. The test group has a significantly lower purchase conversion rate, while improvements in revenue and margin per user are not statistically confirmed.

## Business questions
* Does the test group have a different purchase conversion rate?
* Does higher average policy price translate into higher revenue per exposed customer?
* Do insurace payouts and margin improve enough to justify lower conversion?
* Is the evidence strong enough to recommend a rollout?

## Data preparation
| Tables       | Contents                | Rows |
| ------------- |------------------| -----:|
| `CASE_CONTRACTS.xlsx`     | Issued policies, customer IDs, currencies and prices | 3,711 |
| `CASE_LOSSES.xlsx`     | Insurance payouts associated with customers | 45 |
| `experiment_group.xlsx`  | Customer assignments to pricing groups | 14,842 |

## Findings

1. **The conversion rate has decreased significantly.** The purchase conversion decreased from 32.25% in the control group to 26.44% in the control group (**-5.82 percentage points**), which is a statistically significant difference.
2. **The average price among buyers has increased.** In the test group, the average price of the purchased policy was higher (5,227.87 yen versus 4,154.56 yen), but this did not lead to an increase in revenue per connected customer.
3. **Revenue per user was not statistically different.** The observed change by 42.06 had a p = 0.739 and a 95% confidence interval covering negative and positive values.
4. **Insurance payments and margins in the observed sample have changed for the better, but uncertainty is high.** Test payouts per user were lower and the margin per user was higher; none of the differences reached the selected threshold of significance.

## Business recommendation

**Maintain the existing pricing approach and do not extend the test price to all customers yet.** The decrease in conversion has been confirmed by statistical testing, while the possible financial benefit has not been established. In the course of subsequent work, check the compliance of applications and clients, establish key decision-making indicators, evaluate the effectiveness of the experiment and the volatility of payments, and collect a sufficient number of additional observations before making a new decision on implementation.

## Limitations
- The analysis is an academic project, not evidence of a realized change in product prices.
- The data set does not contain labels of experimental groups that were excluded from the primary comparison.
- The notebook contains payments for insurance claims by client; the exact period of observation and the period of consideration of claims are not specified here.
- Insurance payments are scattered and potentially highly variable, which affects confidence in short-term profitability comparisons.
- The results depend on the assumption of a fixed currency conversion in circulation and on the correct connections by customer ID.
- Hypothesis testing is exploratory in nature and does not involve multiple comparisons.
