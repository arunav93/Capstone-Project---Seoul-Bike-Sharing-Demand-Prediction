# Capstone-Project---Seoul-Bike-Sharing-Demand-Prediction!
![image](https://user-images.githubusercontent.com/20932848/167474611-cd165721-25b0-4294-bd5f-71c4e1fa6cf4.png)

# **Problem Statement**    

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

# **Introduction** 
Pubic rental bike sharing is becoming popular because of its increased comfortableness and environmental sustainability. Bicycle system provides user to rent a bike from one docking station, where user can ride and then return in another docking station. Weather conditions heavily impact the supply of bikes for which the people have to face problems.
Our objective is to  predict the number of bikes rented each hour so as to make an approximate estimation of the number of bikes to be made available to the public given a particular hour of the day.

# **Overview of the data**

We have the following variables in the dataset:
* Date : year-month-day
* Rented Bike count - Count of bikes rented at each hour
* Hour - Hour of the day
* Temperature-Temperature in Celsius
* Humidity - %
* Wind Speed - m/s
* Visibility - 10m
* Dew point temperature - Celsius
* Solar radiation - MJ/m2
* Rainfall - mm
* Snowfall - cm
* Seasons - Winter, Spring, Summer, Autumn
* Holiday - Holiday/No holiday
* Functional Day - No(Non Functional Hours), Yes(Functional hours)

# **Steps involved**

* Installing libraies and getting the dataset.
* Pre-processing the dataset - Checking for Missing values, Duplicate values
* Conduct Exploratory Data Analysis - Analysing the dependent variable, categorical and numerical variables individually.
* Feature Engineering and Feature Selection: - Creation of new features according to our need, handling of outliers, Standardization and normalization of features,       dropping of unnecessary features by checking correlation, VIF and OLS method
* Training different models  - Linear regression, Decision Tress, Random Forest, Gradient Boosting
* Evaluating metrics of all the models - Mean Squared Error, Root Mean Squared Error, Mean Absolute Error, R2 and Adjusted R2
* Hypertuning and Explaining the best model with SHAP.

# **Conclusion**

* We checked Adjusted R2 score to understand which model fit our data better, and we found that that Random Forest Model gave the highest train Adjusted R2 score of 99.05 % and test R2 score of 91.52 %. So we took Random forest for hyperparameter tuning.
For hyperparameter tuning, we first used RandomizedSearchCV on Random Forest model to find random set of best parameters and then we applied GridSearch CV method to narrow down the range to find the perfect hyperparameters.
* We found the evaluation scores for Random Forest model by applying the best hyperparameters.
* We applied SHAP model explainer and we found that Hour and Temperature are the most important features that contributed to prediction.
