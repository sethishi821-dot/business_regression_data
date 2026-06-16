# Dummy Variable Creation

## Purpose

The dataset contains categorical variables that cannot be used directly in a linear regression model. Therefore, categorical variables were converted into dummy (binary) variables using one-hot encoding.

## Variable Selected

### Region

The variable `region` contains four categories:

- East
- North
- South
- West

To avoid the dummy variable trap, one category was selected as the reference category and removed.

Reference category:

- East

Dummy variables created:

- region_North
- region_South
- region_West

Interpretation:

- region_North = 1 if the store is in the North region, otherwise 0.
- region_South = 1 if the store is in the South region, otherwise 0.
- region_West = 1 if the store is in the West region, otherwise 0.

Stores in the East region have all dummy variables equal to 0 and serve as the baseline group.

## Regression Equation

For a model predicting monthly sales:

Monthly Sales =
β0
+ β1(Marketing Spend)
+ β2(Footfall)
+ β3(Avg Discount %)
+ β4(Staff Count)
+ β5(Inventory Availability %)
+ β6(Customer Rating)
+ β7(region_North)
+ β8(region_South)
+ β9(region_West)
+ ε

The coefficients of the dummy variables represent the expected difference in monthly sales relative to the East region, holding all other variables constant.
