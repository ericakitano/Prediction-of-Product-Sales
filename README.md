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
  - filled in missing values with "Unknown' for the categorical column: `Outlet_Size`
  - fixed inconsistent values in `Item_Fat_Content` column
- Performed Exploratory Analysis to understand the statistics and correlation of each feature to the target
- Performed Explanatory Analysis to show the relationship between `Item_MRP` and `Item_Outlet_Sales`

### Results

(plots)

### Model
- Decision Tree Model (TBD)

- Evaluation using Metrics

- Analysis: 
    -  Based on the metrics, the Optimized Decision Tree Model has the lowest MAE of 738 and RMSE of 1057. The difference between RMSE and MAE implies that the model is making some larger errors as well.
    - Since the average value of Item_Outlet_Sales column is 2181 and the Mean Average Error on the Test data is about 738 for the optimized Decision Tree Regression model, the model is off by about 33.8 % on average. (TBD)

### Recommendations:


### Limitations & Next Steps

### For further information
For any additional questions, please contact ekitano1@gmail.com
