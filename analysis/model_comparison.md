# Model Comparison

## Overview

Three regression models were developed to predict monthly sales.

| Model   | Dependent Variable | Independent Variable(s)                                                             |
| ------- | ------------------ | ----------------------------------------------------------------------------------- |
| Model 1 | monthly_sales      | marketing_spend                                                                     |
| Model 2 | monthly_sales      | footfall                                                                            |
| Model 3 | monthly_sales      | marketing_spend, footfall, customer_rating, region_North, region_South, region_West |

---

## Comparison of Models

| Item                  | Model 1: Marketing Spend        | Model 2: Footfall                          | Model 3: Multiple Regression                                       |
| --------------------- | ------------------------------- | ------------------------------------------ | ------------------------------------------------------------------ |
| R-squared             | 0.167                           | 0.736                                      | 0.794                                                              |
| Significant Variables | marketing_spend                 | footfall                                   | marketing_spend, footfall, region_North, region_South, region_West |
| Weak Variables        | None                            | None                                       | customer_rating                                                    |
| Business Usefulness   | Moderate                        | High                                       | Very High                                                          |
| Decision-Making Value | Helps estimate marketing impact | Helps estimate sales from customer traffic | Supports broader business planning and forecasting                 |

---

## R-Squared Comparison

Model 1 explains approximately 16.7% of variation in monthly sales.

Model 2 explains approximately 73.6% of variation in monthly sales.

Model 3 explains approximately 79.4% of variation in monthly sales and provides the strongest overall fit.

Therefore, Model 3 has the greatest explanatory power.

---

## Significant Variables

### Model 1

* marketing_spend (p < 0.001)

### Model 2

* footfall (p < 0.001)

### Model 3

Significant variables:

* marketing_spend
* footfall
* region_North
* region_South
* region_West

Statistically weak variable:

* customer_rating (p = 0.0849)

---

## Business Usefulness

### Model 1

Useful for evaluating the effectiveness of marketing spending. However, many other drivers of sales are not included.

### Model 2

Provides a strong estimate of sales based on customer traffic and is highly useful for store performance planning.

### Model 3

Provides the most comprehensive understanding of sales drivers. It combines marketing, customer traffic, and regional differences, making it the most useful model for forecasting and decision-making.

---

## Limitations

### Model 1

* Uses only one predictor.
* Ignores customer traffic and regional effects.

### Model 2

* Uses only customer traffic.
* Does not account for marketing activities or location differences.

### Model 3

* Does not include all possible business factors.
* Customer rating is difficult to interpret due to weak statistical significance.
* Results are based on historical data and may not fully predict future market changes.

---

## Final Conclusion

The multiple regression model (Model 3) is the preferred model because it has the highest R-squared value (0.794), includes multiple business drivers, and provides the strongest support for business decision-making.
