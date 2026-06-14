Project Overview
This project focuses on applying data mining techniques to predict building-level electricity consumption based on contextual attributes such as square footage, occupancy levels, and average temperatures. The core objective was to clean, preprocess, explore, and model the data using Linear Regression.

Steps Undertaken
Data Loading & Initial Inspection: * Loaded the dataset using Pandas and evaluated the general info, data types, and non-null value counts to determine the cleaning strategy.

Identified the most relevant features influencing building electricity consumption.

Data Cleaning & Formatting:

Extracted numeric values from string columns by removing ' kWh' from Energy_Consumption and 'm2' from SquareFootage, converting both to numeric types.

Standardized the Neighborhood column using regex to extract and strip whitespace.

Normalized the Day_of_Week column by correcting mixed-case strings into standard day names (e.g., matching 'wed' to 'Wednesday').

Converted the Last_Maintenance_Date to a standard datetime format.

Handling Missing Values:

Intelligently imputed missing Governorate values by mapping them to their corresponding Neighborhood (e.g., mapping "Dokki" to "Giza" and "Smouha" to "Alexandria").

Evaluated missing Average_Temperature values by analyzing the mean and standard deviation grouped by neighborhood.

Feature Engineering & Outlier Handling:

Applied one-hot encoding to categorical features like Building_Type (Commercial, Industrial, Residential) to prepare them for mathematical operations.

Removed outliers to significantly raise the correlation between average temperature and energy consumption.

Exploratory Data Analysis (EDA) & Visualization:

Analyzed consumption distributions, discovering that Residential buildings had the widest distribution and Industrial buildings had the highest average consumption.

Visualized the relationship between building size (SquareFootage) and energy consumption using scatter plots and Seaborn regression plots.

Computed the mathematical correlation between specific features and the target variable.

Model Preparation:

Utilized scikit-learn to prepare the data for training using train_test_split.

Set up a LinearRegression model to predict consumption, utilizing Root Mean Squared Error (RMSE) as the primary evaluation metric.

Technologies Used
Python: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-Learn
