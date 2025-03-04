# California Housing Prices Prediction

## Project Objective
This project aims to develop various regression models using PySpark to predict housing prices in California. The dataset contains features such as location coordinates, age, number of rooms, population, and income of the properties in California. The goal is to predict the median house value based on these features.

## Technologies and Libraries Used
- **PySpark**: Used for big data processing and distributed computing.
- **Python**: The primary programming language used for the project.
- **Jupyter Notebook**: The interactive environment where the code is written and executed.
- **Matplotlib & Seaborn**: Utilized for necessary visualizations during the exploratory data analysis phase.

## Dataset
The dataset used in this project is the [California Housing Prices Kaggle](https://www.kaggle.com/datasets/camnugent/california-housing-prices) dataset. It includes the following features:
- **longitude**: The longitude coordinate of the property.
- **latitude**: The latitude coordinate of the property.
- **housing_median_age**: The median age of the houses.
- **total_rooms**: Total number of rooms.
- **total_bedrooms**: Total number of bedrooms.
- **population**: The population in the area.
- **households**: The number of households.
- **median_income**: The median income in the area.
- **median_house_value**: The target variable representing the median house value to be predicted.

## Project Steps

### 1. Data Loading and Preliminary Inspection
- The CSV file is read using PySpark.
- The `header` and `inferSchema` parameters are used to correctly assign column names and data types.
- Functions such as `df.show()`, `df.printSchema()`, and `df.describe()` are used to get an overview of the dataset.

### 2. Data Cleaning
- Missing values are checked and handled using appropriate methods (e.g., mean, median, or removal).
- Unnecessary columns are identified and removed.

### 3. Feature Selection and Transformation
- Independent variables for model training are selected.
- The chosen features are combined into a single `features` column using `VectorAssembler`.
- The target variable (`median_house_value`) is kept separate.

### 4. Splitting the Dataset into Training and Test Sets
- The dataset is split into 80% training and 20% test sets using the `randomSplit` function.
- This split is crucial for reliably evaluating the model's performance.

### 5. Model Training and Evaluation
Different regression models are trained, and their performances are compared:
- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**

For each model, predictions are made on the test set and evaluated using the metrics **RMSE (Root Mean Squared Error)** and **R² (R-squared)**.

### 6. Interpretation of the Results
Example results table:

| Model                | RMSE       | R² Score |
|----------------------|------------|----------|
| Linear Regression    | 71,796.88  | 0.6274   |
| Decision Tree        | 70,479.20  | 0.6410   |
| Random Forest        | 71,041.61  | 0.6352   |
| Gradient Boosting    | 57,447.06  | 0.7615   |

The Gradient Boosting model shows the best performance with the lowest RMSE and the highest R² score, indicating that it is the most effective model for predicting housing prices.

You can download the project, use it as you wish and modify it. If you want a better result or want to contribute, I would be happy.
