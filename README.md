# Prediction-of-Product-Sales
This first project will be a sales prediction for food items sold at various stores. 

We start with Part1 outlines the flow of the project. Then for Part2, we load the data, present the initial information about the data and proceed with cleaning. Part 2 ends with saving the cleaned data for future reference.

For Part 3, we are exploring data analysis through visualizations to help understand, explain or model the sales data.

The following visuals to guide the next steps of this project:

![project_regplot](https://github.com/eccecarreon/Prediction-of-Product-Sales/assets/153371886/ccbdcaf4-9abe-448f-95c4-df68c842796a)

The regplot above shows the positive relationship of the items' maximum retail price and outlet sales. As the maximum retail price goes up, the outlet sales increase as well. It would be interesting to check and confirm for this data if higher prices and high sales volume will help sales prediction. 

![project_scatterplot_hued](https://github.com/eccecarreon/Prediction-of-Product-Sales/assets/153371886/817f6afe-78a7-43c8-b4ed-889a3f8993f8)

We can see that more items sold from Tier 3 locations are at the higher maximum retail prices at 250+. This scatterplot, with additional information for the graph above, gives us an indication that the data might help us explain the positive, moderate correlation of item MRP and outlet sales by also looking at the location type of an outlet or tier type in predicting sales for food items at various stores. 

The mean maximum price per item are the following:

* Household	- $149.42
* Dairy	- $148.50
* Starchy Foods	- $147.84
* Snack Foods	- $146.19
* Fruits and Vegetables	- $144.58
* Seafood	- $141.84
* Breakfast	- $141.79
* Breads - $140.95
* Meat - $139.88
* Canned - $139.76
* Frozen Foods - $138.50
* Hard Drinks	- $137.08
* Others - $132.85
* Soft Drinks	- $131.49
* Health and Hygiene - $130.82
* Baking Goods - $126.38

In terms of sales instances:

![project-count-plot](https://github.com/eccecarreon/Prediction-of-Product-Sales/assets/153371886/e372413a-886b-4ba1-95d8-b1d112e96855)

With food is the basic necessity, it is not suprising alrgest number of sales instance are food items as Fruits and Vegetables followed by Snack Foods and Household item with the highest maximum item price.

* Fruits and Vegetables    1232
* Snack Foods              1200
* Household                 910
* Frozen Foods              856
* Dairy                     682
* Canned                    649
* Baking Goods              648
* Health and Hygiene        520
* Soft Drinks               445
* Meat                      425
* Breads                    251
* Hard Drinks               214
* Others                    169
* Starchy Foods             148
* Breakfast                 110
* Seafood                    64

The tier type or outlet location type displays that item outlet sales are the highest for Tier 3 locations, while Tier 2 locations closely follows.

![project-categorical-plot](https://github.com/eccecarreon/Prediction-of-Product-Sales/assets/153371886/8361a5c4-41f7-480f-81d4-b2f7eb78f0ed)

**Machine Learning Using the Following Models:**
- Linear Regression Model
- Random Forest Regressor Model
- Tuned Random Forest Regressor Model

**Models Evaluated and Results**

* Linear Regression Model (Testing Set)

  - R^2 = 0.567
  - RMSE = 1,092.793
  - MAE = 804.026
  - MSE = 1,194,197.603
    
* Random Forest Regressor Model (Testing Set)
  - R^2 = 0.555
  - RMSE = 1,108.120
  - MAE = 770.716
  - MSE = 1,227,929.363

* Tuned Random Forest Regressor Model (Testing Set)
  - R^2 = 0.590
  - RMSE = 1,063.139
  - MAE = 746.682
  - MSE = 1,130,264.385

* The final model that was chosen is Tuned Random Forest Regressor Model, with max_depth of 10, n_estimators of 100 and max_samples is 150.
* For the testing set on the model, 59.0% of of variance in the target y (item outlet sales) is explained by features matrix X.
* The Root Mean Squared Error is calculated at $1,063.139.
* The Mean Absolute Error deviates by $746.628.
* The Mean Squared Errors is off by $1,130,264.385.

In using the Tuned Random Forest Regressor, we were able to make predictions on future Item Outlet Sales.

**Recommendations**

Outlet Sales
  - We can delve more on how the level of sales for Tier 3 locations with focus on necessities such as Fruit and Vegetables are higher compared to other tiers. A close inspection might also be beneficial in devising ways or boost efforts in improving item outlet sales for other locations such Tier 1 locations.
  - It was expected that items with higher maximum price will generate higher item outlet sales such, Household items but these purchase of these items are less often and focusing on making the prices competitive for items that are bought on a daily basis such as Fruits and Vegetables will likely benefit the stores in the future.

Model Performance
  - Overall, the best model is the Tuned Random Forest Regressor. It outperformed the Linear Regression Model and the Random Forest Regressor.

**Next Steps**
There are opportunities to further improve the model. Other features can explored by asking more questions such as "Why do Tier 3 locations have more sales? What kind of buyers purchase in Tier 3 locations?", or boosting the model (eg. using XGBoost).


  


