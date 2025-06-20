# OIBSIP Data Science Task 3 – Car Price Prediction

## Objective
The goal of this project is to predict the **selling price of used cars** using regression techniques. The model considers various features such as the current price, age, fuel type, transmission, and kilometers driven. The objective is to help both buyers and sellers make informed decisions using data-driven insights.

## Dataset Details

The dataset contains the following columns:

| Column Name       | Description                                      |
|-------------------|--------------------------------------------------|
| Car_Name          | Name of the car                                  |
| Year              | Year of purchase                                 |
| Selling_Price     | Price at which the car is being sold             |
| Present_Price     | Price of the car when bought                     |
| Kms_Driven        | Kilometers driven                                |
| Fuel_Type         | Fuel type of the car (Petrol, Diesel, CNG)       |
| Seller_Type       | Dealer or Individual                             |
| Transmission      | Manual or Automatic                              |
| Owner             | Number of previous owners                        |

Target variable: `Selling_Price`

Dataset file: `car data.csv`

## Steps Performed

### 1. Data Loading and Inspection
- Loaded the dataset using pandas
- Checked for null values, duplicates, and data types

### 2. Data Preprocessing
- Created a new feature: `Car_Age = 2020 - Year`
- Removed redundant columns like `Car_Name` and `Year`
- Applied one-hot encoding to categorical features
- Split the dataset into training and testing sets

### 3. Model Building
- Trained multiple regression models:
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor
- Performed hyperparameter tuning using `GridSearchCV`

### 4. Model Evaluation
- Used metrics like R² score, MAE, and RMSE
- Visualized prediction vs actual results

### 5. Feature Importance
- Used Random Forest to rank the importance of features
- Found that `Present_Price`, `Car_Age`, and `Kms_Driven` had the most impact

## Tools and Libraries Used

- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- Jupyter Notebook

## Key Insights

- The price of a car is most influenced by:
  - Current market price (`Present_Price`)
  - Age of the car (`Car_Age`)
  - Distance driven (`Kms_Driven`)
- Manual transmission cars and dealer-sold cars often show different pricing trends
- Random Forest outperformed other models in accuracy and stability



