## Dataset Review and Variable Assessment

### Dataset

`business_regression_data.xlsx`

Sheet analyzed:

* `store_performance`

### Dataset Overview

* Total rows: **320**
* Duplicate rows detected: **0**
* Multiple stores observed across multiple monthly periods

---

## Dependent Variable (Target Variable)

### Recommended Target

**monthly_profit**

Reason:

* Represents the business outcome to predict.
* Directly measures financial performance.
* Suitable for regression modeling because it is continuous.

Alternative target (optional depending on objective):

* `monthly_sales`

---

## Potential Independent Variables (Predictors)

Variables that may explain changes in monthly profit:

* `marketing_spend`
* `footfall`
* `avg_discount_pct`
* `staff_count`
* `inventory_availability_pct`
* `competitor_distance_km`
* `holiday_flag`
* `customer_rating`
* `region`
* `store_type`
* `month`

These variables may influence store profitability through customer demand, operations, competition, and seasonality.

---

## Numerical Variables

Continuous / numeric features:

* `marketing_spend`
* `footfall`
* `avg_discount_pct`
* `staff_count`
* `inventory_availability_pct`
* `competitor_distance_km`
* `holiday_flag` *(binary numeric)*
* `customer_rating`
* `monthly_sales`
* `monthly_profit`

---

## Categorical Variables

Variables requiring encoding before regression:

* `store_id`
* `month`
* `region`
* `store_type`

Suggested transformations:

* One-hot encoding for `region`
* One-hot encoding for `store_type`
* Extract month features from `month`

---

## Variables That May Need Cleaning or Transformation

### Missing Values

Detected:

* `competitor_distance_km` → missing values present
* `customer_rating` → missing values present

Suggested handling:

* Numerical imputation using median
* Validate business meaning before replacement

---

### Date Transformation

`month`

* Convert into:

  * month number
  * quarter
  * seasonal indicators

---

### Scaling Candidates

Variables with different ranges may benefit from normalization:

* `marketing_spend`
* `footfall`
* `monthly_sales`
* `competitor_distance_km`

---

## Variables That May Not Be Useful for Regression

### `store_id`

Reason:

* Identifier only.
* Does not contain predictive business behavior.
* Should generally be excluded.

### `monthly_sales` *(conditional)*

Reason:

* If predicting `monthly_profit`, sales may dominate prediction and potentially create leakage depending on business objective.

---

## Recommended Modeling Inputs

Target:

* `monthly_profit`

Candidate Features:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* holiday_flag
* customer_rating
* region
* store_type
* engineered month features

Excluded:

* store_id
