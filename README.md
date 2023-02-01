# Sales Predictions Data Report
The goal is understand the relationship between characteristics of items and how much revenue they generate.
# Data Dictionary

-Item_Fat_Content:	Described as Low Fat or Regular

-Item_Visibility: A percentage quanifying how easily items were seen by customers

-Item_Type: Which food group the item in questioning 

-Item_MRP: How much the product is sold for

-Item_Outlet_Sales: How much money the item generated

# Questions adressed 
 ## How much revenue does each item bring in?
![image](https://user-images.githubusercontent.com/109917853/210278775-4797fae2-ee4f-4fd6-9b50-8beb7c4f314a.png)
The histogram shows the distribution of how many items (Item Count) have an Item Outlet Sale of a certain amount (Item Outlet Sales ($)) It shows our minimum and maximum sales as well as the mean (average) and it shows us that most items bring in sales between $34 and $2200.
![image](https://user-images.githubusercontent.com/109917853/210279362-65a5b3c2-d2aa-47cc-bbdb-7ed153543de3.png)
The boxplot shows us similar information, with two more good pieces of information. The bulk of the items provided earn $1000 and $3500 dollars and everything about about $6300 is an outlier, meaning it is an exception to the norm of the sales. 
### Do certain Item Types on average bring in more revenue?
![image](https://user-images.githubusercontent.com/109917853/210279722-63178a88-ece5-452f-933a-3b2ba1f6a6bc.png)
The Bar Plot shows us the average outlet item sales by item type. While there are a few dips, each type of item brings in a roughly similar amount have no significant outliers to be seen.
## Model Results
Four models were created using two different types of model, one default and one with adjusted parameters. The reccomended model was labeled 'Model-1B', it did the best in understanding the variance in the data, understanding relationships, however the models error is about $1335.56.







