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
 - By using this model we can see that the Root Mean Squared Error out performs the other models and has the least amount of errors which is the same as the target unit, dispite r^2 desparity. The data still has a good amount of error variance but reports alot accurately.

---

### Recommendations

Based on the models rendered above:
- We can see that `Seafood` , being most visibile does generate high sales including having the highest `Item_MRP`.
- Additionally, `Starchy Foods` were additionally higher in sales but were lower in visibilty in comparison. 
- Rotation of Items that have lower or moderate sales can be made more visible based on type can be effective in promoting future sales. For example, providing bundle sales for `Breakfast Items` and promote sales in store would increase in popularity. 


---
---

## Project 1 Revisited: Importances and Coefficients



#### Linear Regression Coefficients


![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/cd37c1e4-b050-4182-bcdf-a3fe0e8b5012)


- We can tell based on the top Linear Coefficients that we have positive and negative coefficients with Item Visibility being in the negative coefficients. On the opposite hand we have a positive coefficients that being Item Type Breakfast.


#### Top 10 Most Important Features

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/913c2358-99fc-4a5a-a830-f8c5b68632e5)

## Part 2: Global Explanation

- We have narrowed down our Important Values to the top 10. Based on the figure above, we can see that Item_MRP is the most important feature. In simpler terms, for every increase we have in an item's 'Maximum retail price' the model predicts an increase in item sales thus driving the correlation between the two.

### Random Forest Dot Plot

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/7aa70ff7-fd15-4ed8-9c2f-395145fbfac2)

 - We will compare Random Forest Model to our top 10 features summary model, we can see that Item MRP is a consistent feature between the two models. To help better understand each dot represents the feature value on the model prediction, the color represents the feature value. We also can see here that Item_MRP swaying to the right of 0 signifies a higher prices item while swaying to the left signifies a decrease in price. 
 - Another feature of note is Outlet_type_grocery_store, this ohe feature represents the red meaning yes grocery store vs blue which is other type of grocery type.
 - I would also point out Item_Visibility, as this feature will differ depending on a visible variable, as we can see in our model that  sales are dependent on item visibility and display in store contributes to the higher and lower sales. 

### Random Forest SHAP Summary 

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/ded96b6d-f70e-4eb6-9ae1-71cb7cb11444)

 - We can see that our random forest bar plot has similar features to our top 10 important features. Item_MRP and Outlet_type


## Part 3 : Local Explainations 

 - We will continue to working on our models but now to will proceed to isolating two example rows of item_MRP based on the highest prices item and the lowest priced item. We will also continue to test between Linear Regression and Random Tree Forest.

## Example 1: 
### Shap Force Plot

#### Random Forest Force Plot

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/f5e2f916-a0b6-4c62-a79d-64fc4cc3f43f)

- In the sample, we isolated the base value of 2,155. Our highest final item value of 264.70 rupees. We can also see that this item is sold in a small grocery store. Also the establishments year of 2009.

#### Linear Regression Force Plot

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/af8c9297-7cd9-4dbe-9866-d3cc9c6bafd0)

- With running a secondary Linear Regression model we also see out Item_MRP at 264.70 rupess, we can also note that out final f(x) of 4,138.71 which is higher than the random forest model. We also see a change in outlet size to me medium of size.

We will continue with model by trying a LIME model.

## LIME 

We will be conducting a LIME model with you first Example which is the higher item_MRP using a regression mode.

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/304dc978-2323-401f-9996-a8a0ef1b9225)

- For our Lime Model, Our predicted value for this row is 3493.27 accurate out of 57.52-7059 which means that we have a good prediction for this model. We also can see that other values indicate that this establishment is a small grocery store as its value is 0 out of 4.

## Example 2:

### Shap Force Plot 

We will continue our modeling with example 2 for the minimum Item_MRP. We will also conduct a Random forest and linear regression model.

#### Random Forest Force Plot

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/099b2eb1-7d27-46b7-bb3c-998fcae04c56)

- For our value minimum Item_Mrp we can see 32.36 rupees. Our final f(x) value is 299.46. We also have a value for establishment year being 1987.

  #### Linear Regression

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/7e8e7de9-2fd1-4fab-9905-ecfb65b87e01)

- For this linear regression model we can see that the Item_MRP is similar to 32.35. We do see a change in increase of f(x) value of 824.18 rupees. We can also note that the outlet type changed to 1 meaning this item is located at a larger location and can attribute to the higher f(x) value.

- We will continue onto out LIME model with our secondardy exmaple row. 

## LIME

We will now proceed with conducting a LIME model for our second example and we will be using the random forest regression.

![image](https://github.com/valmazan/Project_Part_Prediction-of-Product-Sales/assets/126423326/3d646b1e-bf95-4421-9df0-024fe92a6284)

- Based on our predicted value of our second example, we showing 299.46. Our minimum predicted value ranges from 61.65- 6880.97, so we have a very low prediction value. We can also deduce that this is a small grocery store, we can also see the establishment year of 1987.
 
 








   












