# Energy Consumption Prediction: Linear Regression Mini-Project

## 📌 Overview
This project applies data mining techniques to predict building electricity consumption based on features like square footage, occupancy, and temperature. The goal is to clean, explore, and model the data using Linear Regression.

## 🛠️ Project Steps

* **1. Data Loading & Inspection**
  * Loaded `energy_data.csv` using Pandas.
  * Checked data types and missing values to plan the cleaning process.

* **2. Data Cleaning & Formatting**
  * Removed text strings (like ' kWh' and 'm2') from numeric columns (`Energy_Consumption`, `SquareFootage`) and converted them to pure numbers.
  * Cleaned up the `Neighborhood` column by removing extra spaces and standardizing the text.
  * Standardized `Day_of_Week` entries (e.g., changing 'wed' to 'Wednesday').
  * Fixed date formats for `Last_Maintenance_Date`.

* **3. Handling Missing Values**
  * Filled missing `Governorate` names logically based on the `Neighborhood` (e.g., mapping "Dokki" to "Giza").
  * Estimated missing `Average_Temperature` values using the average temperature of the respective neighborhood.

* **4. Feature Engineering & Outliers**
  * Converted categorical data like `Building_Type` into numbers using one-hot encoding so the machine learning model can understand them.
  * Removed extreme outliers, which made the mathematical relationship between temperature and energy consumption much clearer and more accurate.

* **5. Data Exploration & Visualization**
  * Discovered that Residential buildings vary the most in consumption, while Industrial buildings use the most energy on average.
  * Created visual plots using Seaborn and Matplotlib to clearly show how building size affects energy use.

* **6. Machine Learning Model**
  * Split the data into training and testing sets to properly evaluate performance.
  * Built a **Linear Regression** model using scikit-learn to predict energy consumption.
  * Evaluated the model's accuracy using Root Mean Squared Error (RMSE).

## 🚀 Technologies Used
* **Data Processing:** Python, Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn
