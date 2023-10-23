# sales_predictions
sales prediction for food items sold at various stores

**Author:** 
Namutebi Winnie Susan

**Business problem:**

The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.

**Data:**

The data provided includes information as follows: 'Item_Identifier', 'Item_Weight', 'Item_Fat_Content', 'Item_Visibility','Item_Type', 'Item_MRP', 'Outlet_Identifier','Outlet_Establishment_Year', 'Outlet_Size', 'Outlet_Location_Type','Outlet_Type', 'Item_Outlet_Sales'
The data was provided by Coding Dojo as part of teh Data Science program.

**Methods**

I replaced the ordinal data with numbers for the Outlet size.

I used the simple imputer mean strategy to fill in missing values in the numerical columns

I used the frequency strategy of the simple imputer fill in missing values in the data.

I then scaled the data and used the One Hot Enconder to get data ready for preprocessing. ie making all the values numeric

I then used the column transformer anf instantiated the Linear regression model.

The linear regression model didn't perform well on the test data, and was overfitting on the training set.

I therefore dropped it and used the random forest regressor to complete the prediction. and it gave me better R2 results. 59% on the test data. This can be used on new data and the RMSE is not so big and can be taken into account once the model is in use.

**RESULTS**

![Screenshot 2023-03-12 204924](https://user-images.githubusercontent.com/122565105/224562965-367ecc6e-f106-4e30-9d18-9c187a279d8f.png)

![Screenshot 2023-03-12 204955](https://user-images.githubusercontent.com/122565105/224562997-b3e585a6-e844-41c0-9b11-cd8a7c032982.png)

**MODEL**

The final model after preprocessing used the Random Forest Regressor to predict sales. It is giving an RMSE of 1113.

**RECOMMENDATION**

**LIMITATIONS AND NEXT STEPS**

Ibelieve there is still room for improvement on this model. after removing some features that are redundant and also removing features that could cause leakage, the model didn't improve. I need to invest more time to tune parameters and improve the mae.
For further information: winnsusanne@gmail.com
