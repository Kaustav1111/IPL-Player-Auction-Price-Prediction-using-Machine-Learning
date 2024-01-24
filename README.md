# Project Description:

This project revolves around predicting the auction price of IPL 2023 players by employing ML (Random Forest Regression) techniques. The process involves comprehensive data preprocessing, exploratory data analysis (EDA), feature engineering, and model training. The ultimate aim is to enhance the accuracy of predictions and assess the model's performance.
This project showcases the application of machine learning techniques to predict IPL player auction prices, demonstrating the authors knowledge of specific ML concepts.

# Actions Taken:

## Dataset Import:
Loaded the IPL player dataset from the 'Player_Data.csv' file using the pandas library.
## Column Processing:
1) Dropped irrelevant columns, such as 'Sl.no' and 'Cost in Dollars.'
2) Treated null values in the 'Team2021' column, replacing them with 'Unsold.'
3) Transformed the 'Base Price' column to a continuous format, converting values like 'Lakh' and 'Cr' to numeric format.
4) Created a new 'Player Tier' column based on the difference between 'Cost in Cr' and 'Base Price.'
5) Imputed missing values in 'Cost in Cr' based on 'Base Price.'
6) Rearranged columns for better readability.
## Exploratory Data Analysis (EDA):
1) Explored the distribution of player tiers, player types, base prices, and team distributions for 2021 and 2022.
Feature Engineering:
2) Created dummy variables for categorical variables excluding 'Player Tier.'
3) Applied label encoding to 'Player Tier' since tiers are ordinal.
4) Checked correlation between variables.
## Train-Test Data Splitting:
Split the dataset into training and testing sets using the train_test_split function from sklearn.model_selection.
## VIF Analysis:
Checked variance inflation factor (VIF) to assess multicollinearity.
## Feature Scaling:
Performed standardization on the training and testing sets using StandardScaler from sklearn.preprocessing.
## Model Training:
Employed a Random Forest Regressor with 
1) 300 estimators,
2) A random state of 1 for reproducibility, and
3) A maximum depth of 5 for predicting auction prices.
## Model Performance Evaluation:
Evaluated model performance using metrics like 
1) Mean Absolute Error (MAE),
2) Mean Absolute Percentage Error (APE),
3) accuracy for both training and testing sets.
## Model Performance:
Mean Absolute Error: 4,455,447
Mean Absolute Percentage Error: 18.77%
Model accuracy for X_test: 81.23%
Model accuracy for X_train: 87.46%
