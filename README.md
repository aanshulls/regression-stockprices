# regression-stockprices

This project focuses on predicting stock closing prices using a Linear Regression model. The dataset used contains 5 years of historical stock data for various companies, including features like opening price, high price, low price, volume, and date. The goal is to build a model that can accurately predict the closing price of a stock based on these features.

Dataset
The dataset (all_stocks_5yr.csv) contains the following columns:

Date: The date of the stock data.
Open: The opening price of the stock.
High: The highest price of the stock during the day.
Low: The lowest price of the stock during the day.
Close: The closing price of the stock (target variable).
Volume: The number of shares traded during the day.
Name: The name of the company (stock ticker symbol).

Data Preprocessing:
Handling Missing Values: Missing values in the open, high, and low columns were filled with their respective medians.

Feature Engineering:
The date column was converted into a numerical feature (days_since_first) representing the number of days since the first date in the dataset.

The Name column (categorical) was dropped as it was not relevant for regression.

Data Type Conversion: Columns like open, high, and low were converted from object type to numeric type for analysis.

Correlation Analysis: A heatmap was used to visualize the correlation between features, showing strong relationships between the target (close) and features like open, high, and low.

Model Building
Algorithm Used: Linear Regression.

Train-Test Split: The data was split into training and testing sets (75% training, 25% testing).

Evaluation Metric: The model was evaluated using the R² score, which measures the proportion of variance in the target variable that is predictable from the features.

Results:
The model achieved an R² score of 0.9998, indicating an extremely high level of accuracy in predicting stock closing prices. This suggests that the features used (open, high, low, volume, and days_since_first) are highly predictive of the closing price.

Libraries Used:
Pandas: For data manipulation and analysis.
NumPy: For numerical computations.
Seaborn and Matplotlib: For data visualization.
Scikit-learn: For model building and evaluation.
