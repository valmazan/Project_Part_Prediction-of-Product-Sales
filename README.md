# Prediction of Product Sales

## Anaylizing the Properties and Outlets of Future Projections of Sales.

Victoria Almazan 

### Our goal is to help partners understand the different properties of products and outlets that may play a crucial role in predicting future sales. There are so many factors that play into understanding which factors are most sucessful in continuous high sales based on varations and visibility.

---

# Data Set

Sales Predictions data set- https://docs.google.com/spreadsheets/d/e/2PACX-1vQujSPVdp1EfFsngrLgWZZ_VT_I7nuzXs10BqUJV5ai8hFZoUDf3mpA68wj37UFVfS3yvj_QvvO6655/pub?gid=1913766112&single=true&output=csv
* There are 8523 rows and 12 columns

# Data Dictionary
![Dictionary](https://user-images.githubusercontent.com/126423326/236727311-483eb005-c637-4e8b-9290-13f6c15c8d59.PNG)


## For this Data, we cleaned and prepared the data using the following processing was performed:

### Exploratory Data Analysis
- While exploring this data, we have ensure that our data was visualized by the usage of histograms for the numerical datatype. 
- Also the usage of barplots are used to visualize categorical data. 
- This gives us a better representation of what our data is trying to portray. 

## Item Outlet Sales

![Item Outlet Sales(1)](https://user-images.githubusercontent.com/126423326/236731997-e5d79191-71b1-423d-9457-a3d1810117fb.png)

This histogram shows the most amount on sales were under $2000.

### Explanatory Data Analysis 

- To better understand our categorical data, we will use bargraphs that will show comparisons. 

## Explanatory Visiuals 

![display items by type](https://user-images.githubusercontent.com/126423326/236738245-5aaa033a-3861-40c8-b1bc-0e9c9d642865.png)

The histogram above shows the percentage of visibility per item type. 
- We can see that Seafood has the most percentage of visibilty. 
- Following that, Dairy and Breakfast foods were also high in visibility.

![average outlet sales based on items](https://user-images.githubusercontent.com/126423326/236739223-531d8e33-af46-4079-b429-ae8acd2b7883.png)

The Average Outlet Sales show the Total Item sales by Type of Item.
- We can see that based on the barplot, Starchy Foods have had higher sales over all at $2374.33
- At the bottom of the figures, Other products totaling $1926.14 

## Machine Learning Using the following Models:
- Linear Regression Model 
- Untuned Decision Tree Model 
- Tuned (Max Depth) Decision Tree Model
- Untuned Random Forest Model 

## Models Evaluated & Results 

Linear Regression Model(Test Set):
  - R^2 = 0.096
  - MAE = 1065.951
  - MSE = 2205576.275
  - RMSE = 1485.118
  
Untuned Decision Tree Model(Test Set):
  - R^2 = 0.534
  - MAE = 754.496
  - MSE = 1137929.685
  - RMSE = 1066.738
  
Tuned (Max Depth) Decision Tree Model(Test Set):
  - R^2 = 0.493
  - MAE = 788.057
  - MSE = 1237667.664
  - RMSE = 1112.505
  
---

 - The final model chosen is the Tuned (Max Depth) Decision Tree Model
   - For this testing set, 53% of the variance was explained between x & y.
   - The Mean Absolute Error was off by $7,544.96.
   - The Mean Squared Error was $1,137,929.68.
   - The Root Mean Squared Error had a calculation of $1,066.79.
 - By using this model we can see that we have a we have a higher mean squared error dispite r^2 desparity. The data still has a good amount of error variance but reports alot accuracy.

---

### Recommendations

Based on the models rendered above:
- We can see that `Seafood` , being most visibile does generate high sales including having the highest `Item_MRP`.
- Additionally, `Starchy Foods` were additionally higher in sales but were lower in visibilty in comparison. 
-Rotation of Items that have lower or moderate sales can be made more visible based on type can be effective in promoting future sales. For example, providing bundle sales for `Breakfast Items` and promote sales in store would increase in popularity. 


























