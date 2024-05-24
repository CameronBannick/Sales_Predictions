# Sales Report
## Introduction
    As the grocery franchise approached its third decade of operation, it was decided to analyze the data collected over the years to find 
insights that can aid in potential growth for the franchise. The goal of this report is exactly that.
## The data
Item_Identifier:           Unique identifier       
Item_Weight:               Items weight (lbs)        
Item_Fat_Content:          Low fat or regular fat  
Item_Visibility:           Metric for visibility   
Item_Type:                 Food group               
Item_MRP:                  Item price              
Outlet_Identifier:         Unique Identifier        
Outlet_Establishment_Year: Year opened       
Outlet_Size:               Store size       
Outlet_Location_Type:      Location type    
Outlet_Type:               Store type      
Item_Outlet_Sales:         Total item outlet sales   

## Exploratory data analysis
 ### Item information 
 #### Item outlet sales

![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/Item_sales_boxplot.png)

![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/Item_sales_histogram.png)

Most item sales occur between $834.25 and $3101.30 with the middle of all the data points being $1794.33. The average item outlet sales are $2181.29. Since our middle (median) and average are far away from each other, this implies there are a lot of outliers. The outliers can be seen as diamonds on the boxplot above.

#### Item outlet sales and item mrp.
![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/Item_mrp_outlet_sales.png)

The above scatterplot shows a correlation coefficient of 0.57 for item outlet sales and item mrp, which is a moderately strong correlation.

#### Item outlet sales and item visibility 
![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/item_visibility_item_sales.png)

This next scatterplot shows a correlation coefficient of -0.13 between item outlet sales and item visibility, which is a very weak relationship.

#### Item outlet sales and item visibility
![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/sales_over_weight.png)

Lastly, our last scatterplot shows a virtually non existent relationship between item outlet sales and item weight.

## Predictive models
Two different versions (a tuned and an untuned) of three different models were made for a total of six. The metrics used were Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE). MSE is scored by taking the distances from the predicted value from the actual value and multiplying it by itself, this is to penalize larger errors more. The closer the score is to 0 the better. The RMSE is similar except you don't multiply the number, this gives a feel for the overall error. Lastly, the MAE gives the average error regardless of if the error is positive or negative. Using all three together will give a clearer picture of what’s going on.

### Decision tree 
The Decision Tree algorithm works like being interviewed on a podcast. The host asks you a series of questions and by the end you get a prediction of what kind of person you are. This algorithm starts with one question that branches out with even more questions until it comes back with a prediction.

#### Untuned model
MAE: 0.00000000000000010671
MSE: 0.000000000000000000000000000024
RMSE: 0.00000000000000492586

The error in this model is virtually non-existent. If it's true then the model can predict item sales by less than half a penny. I would advise caution when considering this model.

#### Tuned model
MAE: 762.61
MSE: 1172122.77
RMSE: 1082.65

The MAE tells us that the average error in the model was 762.61, this could be in a positive or negative direction. The MSE is over a million, so there could have been a lot of large errors. Alternatively, this could be due to the outliers in the data. The RMSE tells us the model can predict sales within 1082.65.

### Random forest
Let's say you had a problem in your personal or professional life, chances are you would seek advice from many different people. Then, you would take all of those pieces of advice to inform your plan of action. In the case of the Random Forest Algorithm, each person you ask for advice is a decision tree creating a forest of opinions that help inform a prediction.

#### Untuned model
MAE: 296.98
MSE: 183498.95
RMSE: 428.37

The MAE tells us that the average error in the model was 296.98, this could be in a positive or negative direction. The MSE is 183498.95, so there could have been some large errors. Alternatively, this could be due to the outliers in the data. The RMSE tells us the model can predict sales within 428.37.

#### Tuned model
MAE: 724.74
MSE: 1057240.99
RMSE: 1028.22

The MAE tells us that the average error in the model was 724.74, this could be in a positive or negative direction. The MSE is over a million, so there could have been a lot of large errors. Alternatively, this could be due to the outliers in the data. The RMSE tells us the model can predict sales within 1028.22.

### XGBoost 
Imagine you're taking a quiz, except for this quiz you have access to a myriad of experts in different fields of study. You could consult each expert. In the case of the XGBoost algorithm, the experts are each decision trees that combine their expert opinions that even can learn from their mistakes giving us its best prediction. 

#### Untuned model
MAE: 457.76
MSE: 403082.89
RMSE: 634.89

The MAE tells us that the average error in the model was 457.76, this could be in a positive or negative direction. The MSE is 403082.89, so there could have been some of large errors. Alternatively, this could be due to the outliers in the data. The RMSE tells us the model can predict sales within 634.89.

**Feature Importance:**
item_weight: 0.0032266636844724417
item_fat_content: 0.0
item_visibility: 0.005109422840178013
item_type: 0.0039376430213451385
**item_mrp: 0.008135724812746048**
outlet_establishment_year: 0.0038489806465804577
**outlet_size: 0.006368603557348251**
outlet_location_type: 0.004086561966687441
**outlet_type: 0.005701855290681124**

#### Tuned model
MAE: 734.10
MSE: 1079569.68
RMSE: 1039.02

The MAE tells us that the average error in the model was 734.10, this could be in a positive or negative direction. The MSE is over a million, so there could have been a lot of large errors. Alternatively, this could be due to the outliers in the data. The RMSE tells us the model can predict sales within 1039.02.

**Feature Importance:**
item_weight: 0.0015420609852299094
item_fat_content: 0.0
item_visibility: 0.0
item_type: 0.00264928606338799
i**tem_mrp: 0.004750597290694714**
outlet_establishment_year: 0.002885641297325492
**outlet_size: 0.008301385678350925**
**outlet_location_type: 0.003716213395819068**
outlet_type: 0.010065117850899696

## Results and interpretations

![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/store_sales_sum_type.png)

The statistical analysis showed a significant difference in sales between outlet types, more than half of sales come from Supermarket Type 1.

![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/store_sum_sales.png)

It also showed a significant difference in sales by outlet size. Most item sales come from medium sized stores.

![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/total_item_type_sales.png)

There is a significant difference in sales by item type. The highest selling products are Fruits/Vegetables, Snack Foods, and household products.

There was no relationship found between sales and item visibility/item visibility as shown previously. A moderate relationship was found between Item MRP and outlet sales as shown previously


## Limitations
The information regarding each item was very limiting, for example no brands were given to the items, 

## Recomendations
If you wish to proceed deploying a model, I recommend the untuned random Forrest model, however the features in the dataset were very limiting in some regards. For example, there was no information regarding the brand or the actual item itself aside from the unique indicator. 

## Conclusion
While insights were made into what features in the dataset related most to item outlet sales, they were made with very limited information regarding the items.

## Next Steps
I believe we should test these findings against some more brand and name specific data points. While we found some food types might be the highest selling, know the top brands of each type. I believe there are some similar insights we will find in regards to outlet size and types. I am also fairly confident we could created a more accurate model.








