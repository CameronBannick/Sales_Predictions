# Sales Report
## Introduction
    As the grocery franchise approached its third decade of operation, it was decided to analyze the data collected over the years to find 
    insights that can aid in potential growth for the franchise.The goal of this report is exactly that.
## The data
Item_Identifier:           Unique identifier       
Item_Weight:               Items weight lbs        
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
 ### How much revenue does each item bring in?
![image](https://user-images.githubusercontent.com/109917853/210278775-4797fae2-ee4f-4fd6-9b50-8beb7c4f314a.png)
The histogram shows the distribution of how many items (Item Count) have an Item Outlet Sale of a certain amount (Item Outlet Sales ($)) It shows our minimum and maximum sales as well as the mean (average) and it shows us that most items bring in sales between $34 and $2200.
![image](https://user-images.githubusercontent.com/109917853/210279362-65a5b3c2-d2aa-47cc-bbdb-7ed153543de3.png)
The boxplot shows us similar information, with two more good pieces of information. The bulk of the items provided earn $1000 and $3500 dollars and everything about about $6300 is an outlier, meaning it is an exception to the norm of the sales. 
### Do certain Item Types on average bring in more revenue?
![image](https://user-images.githubusercontent.com/109917853/210279722-63178a88-ece5-452f-933a-3b2ba1f6a6bc.png)
The Bar Plot shows us the average outlet item sales by item type. While there are a few dips, each type of item brings in a roughly similar amount have no significant outliers to be seen.
## Model Results
Four models were created using two different types of model, one default and one with adjusted parameters. The reccomended model was labeled 'Model-1B', it did the best in understanding the variance in the data, understanding relationships, however the models error is about $1335.56.

# Conclusions
On average, it seems all item types bring in the same amount of revenue. Most revenue comes from items that bring in between $1000 and $3500 dollars with some outliers above and below this range.





