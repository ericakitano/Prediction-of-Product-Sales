# **Prediction of Product Sales**

## Using regression models to predict the sales of food products 

- **Author:** Erica Kitano



### Business problem:
Help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.

### Data:
The original source of the data used is `Big Mart Sales Prediction` from [this link](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/).

### Methods
- Data cleaning:
  - checked for duplicates
  - filled in missing values with median value for the numerical column: `Item_Weight` 
  - filled in missing values with 'Unknown' for the categorical column: `Outlet_Size`
  - fixed inconsistent values in `Item_Fat_Content` column
- Performed Exploratory Analysis to understand the statistics and correlation of each feature to the target
- Performed Explanatory Analysis to show the relationship between `Item_MRP` and `Item_Outlet_Sales`

### Results

#### Regplot of `Item_MRP` vs `Item_Outlet_Sales`

> ![reg_plot_1](https://user-images.githubusercontent.com/127703546/236113302-968bf5a3-ccfc-459b-8336-2424a5044a44.png)

There is a positive correlation between `Item_MRP` and `Item_Outlet_Sales`.

#### Outlet_Type Count Plot

> ![outlet_type](https://user-images.githubusercontent.com/127703546/236113472-7df7a044-4c7e-4189-9ec3-dfe2632a3bc1.png)
> 
Supermarket Type1 has the highest count.

### Model
#### 1. Decision Tree Model 

- Evaluation using Metrics: 
 > Decision Tree Test Scores
 > - Mean Average Error: 738.3556 
 > - Root Measn Squared Error: 1,057.4441 

- Analysis: 
    - Based on the metrics, the `Optimized Decision Tree Model` has the lower MAE of 738 and RMSE of 1057 compared to the `Linear Regression Model` which has higher MAE and RMSE. 
    - The difference between RMSE and MAE in the `Optimized Decision Tree Model` implies that the model is making some larger errors as well.
    - Since the average value of `Item_Outlet_Sales` column is **2181** and the Mean Average Error on the Test data is about **738** for the `Optimized Decision Tree model`, the model is off by about **33.8 %** on average.

#### 2. Random Forest Model

- Evaluation using Metrics: 
 > Random Forest Test Scores
 > - Mean Average Error: 728.2810 
 > - Root Measn Squared Error: 1,046.6086 

- Analysis: 
    - Based on the overall metrics of all 4 models that were compared, the `Optimized Random Forest Tree Model` (max_depth=5, n_estimators=150) has the lowest MAE of **728** and RMSE of **1047** on the test data. 
    - The difference between RMSE and MAE implies that the model is making some larger errors as well.
    - Since the average value of `Item_Outlet_Sales` column is **2181** and the Mean Average Error on the Test data is about **728** for the optimized Random Forest model, the model is off by about **33.4 %** on average.

### Recommendations: 

Based on the evaluation, `Decision Tree Model` or  `Random Forest Model` is recommended.


### Limitations & Next Steps

For this set of data, even the best model (Optimized Random Forest Model) is underfit and have high bias. This can be explained from the observation that the features do not correlate well with the target and some values were imputed.

### For further information
For any additional questions, please contact ekitano1@gmail.com
