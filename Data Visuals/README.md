# Sales Report
## Introduction
    As the grocery franchise approached its third decade of operation, it was decided to analyze the data collected over the years to find 
    insights that can aid in potential growth for the franchise.The goal of this report is exactly that.
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

The majority of item sales occur between $834.25 and $3101.30 with the middle of all the data points being $1794.33. The average item outlet sales is $2181.29. Since our middle (median) and average are far away from each other, this implies there are a lot of outliers. The outliers can be seen as diamonds on the boxplot above. 

#### Item outlet sales and item mrp.
![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/Item_mrp_outlet_sales.png)

The above scatterplot shows a correlation coeficient of 0.57 for item outlet sales and item mrp, which is a moderate strong correlation.

#### Item outlet sales and item visibility 
![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/item_visibility_item_sales.png)

This next scatterplot shows a correlation coeficient of -0.13 between item outlet sales and item visibility, which is a very weak relationship.

####
![image](https://github.com/CameronBannick/Sales_Predictions/blob/main/Data%20Visuals/sales_over_weight.png)

Lastly, our last scatterplot shows a virtually non existent relationship between item outlet sales and item weight.

## Predictive models
Two different versions (a tuned and an untuned) of three different models were made for a total of six.

### Decision tree



# Conclusions
On average, it seems all item types bring in the same amount of revenue. Most revenue comes from items that bring in between $1000 and $3500 dollars with some outliers above and below this range.





