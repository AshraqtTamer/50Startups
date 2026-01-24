

# 50 Startups Profit Prediction & Backward Elimination

This project performs exploratory data analysis (EDA) and builds a regression model to predict the profit of 50 startups based on various expenditure and location data. It specifically explores the technique of **Backward Elimination** to optimize the multiple linear regression model.

## Dataset

The project uses the `50_Startups.csv` dataset, which contains the following features for 50 companies:

* **R&D Spend**: Amount spent on Research and Development.
* **Administration**: Amount spent on administrative expenses.
* **Marketing Spend**: Amount spent on marketing efforts.
* **State**: The state where the startup is located (New York, California, Florida).
* **Profit**: The target variable representing the startup's profit.

## Project Workflow

1. **Data Loading & Cleaning**: Importing data and checking for null values (the dataset contains no missing values).
2. **Exploratory Data Analysis (EDA)**:
* Statistical summary of the numerical features.
* Correlation analysis (e.g., R&D Spend shows a very high correlation with Profit at ~0.97).
* Visualizations using Seaborn and Matplotlib (Pair plots, Heatmaps).


3. **Data Preprocessing**:
* Handling categorical variables (State) using One-Hot Encoding.
* Splitting the data into Training and Test sets.
* Feature Scaling (Normalization).


4. **Modeling**:
* Implementing **Multiple Linear Regression**.
* Applying **Backward Elimination** using the `statsmodels` library to remove statistically insignificant variables (features with high P-values) to improve model efficiency.



## Technologies Used

* **Python 3.x**
* **Pandas**: Data manipulation and analysis.
* **NumPy**: Numerical computing.
* **Matplotlib / Seaborn**: Data visualization.
* **Scikit-Learn**: Machine learning and preprocessing.
* **Statsmodels**: Statistical modeling and P-value analysis.

## Key Findings

* **R&D Spend** is the most significant predictor of a startup's profit.
* **Backward Elimination** helps in simplifying the model by removing features like 'State' or 'Administration' if they do not contribute significantly to the prediction accuracy.
