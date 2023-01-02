# Sales Predictions Data Report
Cameron Bannick
# Issue Adressed
This project consisted of two main sections, out exploratory data analysis with data visualizations and two models with the goal of gaining insight and predicting an items total outlet sales.
# Data Provided
## The Data provided originally had the features of: 
Item_Identifier,	Item_Weight,	Item_Fat_Content,	Item_Visibility,	Item_Type,	Item_MRP,	Outlet_Identifier	Outlet_Establishment_Year	Outlet_Size	Outlet_Location_Type	Outlet_Type	Item_Outlet_Sales 
## However, all visualizations and models were created using only:
Item_Fat_Content,	Item_Visibility,	Item_Type	Item_MRP,	Item_Outlet_Sales,
### This was because these were the only features that had to do with the individual items themselves.
# Results 
## Data Visualizations 
### Visual A
![image](https://user-images.githubusercontent.com/109917853/210278775-4797fae2-ee4f-4fd6-9b50-8beb7c4f314a.png)
Visual A shows the distribution of how many items (Item Count) have an Item Outlet Sale of a certain amount (Item Outlet Sales ($)) It shows our minimum and maximum sales as well as the mean (average) and it shows us that most items bring in sales between $34 and $2200.
### Visual B
![image](https://user-images.githubusercontent.com/109917853/210279362-65a5b3c2-d2aa-47cc-bbdb-7ed153543de3.png)
The next visual shows us similar information, with two more good pieces of information. The bulk of the items provided earn $1000 and $3500 dollars and everything about about $6300 is an outlier, meaning it is an exception to the norm of the sales. 
### Visual C 
![image](https://user-images.githubusercontent.com/109917853/210279722-63178a88-ece5-452f-933a-3b2ba1f6a6bc.png)
Our last visual shows us the average outlet item sales by item type. While there are a few dips, each type of item brings in a roughly similar amount have no significant outliers to be seen.
## Model Results
Four models were created using two different types of model, one default and one with adjusted parameters. The reccomended model was labeled 'Model-1B', it did the best in understanding the variance in the data, understanding relationships, however the models error is about $1335.56.







