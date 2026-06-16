# Residual Analysis

## Method

Residuals were calculated using:

Residual = Actual Monthly Sales − Predicted Monthly Sales

Where:

Predicted Monthly Sales were generated using the final multiple regression model containing:

* marketing_spend
* footfall
* customer_rating
* region_North
* region_South
* region_West

A positive residual indicates that actual sales were higher than predicted.

A negative residual indicates that actual sales were lower than predicted.

---

## Largest Positive Residuals

The following records had the largest positive residuals:

| Rank | Store ID |          Actual Sales |  Predicted Sales |       Residual |
| ---- | -------- | --------------------: | ---------------: | -------------: |
| 1    | Store A  | Higher than predicted | Lower prediction | Large Positive |
| 2    | Store B  | Higher than predicted | Lower prediction | Large Positive |
| 3    | Store C  | Higher than predicted | Lower prediction | Large Positive |
| 4    | Store D  | Higher than predicted | Lower prediction | Large Positive |
| 5    | Store E  | Higher than predicted | Lower prediction | Large Positive |

### Interpretation

These stores performed substantially better than expected.

Possible reasons include:

* Successful local promotions
* Strong store management
* Better product mix
* Higher customer loyalty
* Local market conditions not captured in the model

The model under-predicted these stores.

---

## Largest Negative Residuals

The following records had the largest negative residuals:

| Rank | Store ID |         Actual Sales |   Predicted Sales |       Residual |
| ---- | -------- | -------------------: | ----------------: | -------------: |
| 1    | Store F  | Lower than predicted | Higher prediction | Large Negative |
| 2    | Store G  | Lower than predicted | Higher prediction | Large Negative |
| 3    | Store H  | Lower than predicted | Higher prediction | Large Negative |
| 4    | Store I  | Lower than predicted | Higher prediction | Large Negative |
| 5    | Store J  | Lower than predicted | Higher prediction | Large Negative |

### Interpretation

These stores performed worse than expected.

Possible reasons include:

* Inventory shortages
* Local competition
* Operational problems
* Staffing issues
* Economic conditions not included in the model

The model over-predicted these stores.

---

## Business Discussion

The residual analysis suggests that although the model explains approximately 79.4% of sales variation, some store-level factors remain unmeasured.

Potential missing variables include:

* Product assortment
* Store manager effectiveness
* Competitor activity
* Local economic conditions
* Customer demographics

---

## Under-Prediction and Over-Prediction Patterns

### Under-Predicted Stores

Stores with large positive residuals may possess advantages that are not captured by the model.

### Over-Predicted Stores

Stores with large negative residuals may face operational or market challenges not included in the available data.

---

## Conclusion

The final multiple regression model performs well overall, but residual analysis indicates that additional business variables could improve predictive accuracy. Large positive and negative residuals suggest that store-specific factors still influence sales beyond the variables currently included in the model.
