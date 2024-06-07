# gold_price_prediction
Gold Price Prediction Using ML

# Gold Price Prediction using Machine Learning

## Overview
This project aims to predict the price of gold using various financial indicators. The dataset contains information about gold prices and other related financial data over a period.

## Dataset
The dataset used for this project contains 2290 rows with the following columns:

- `Date`: The date of the observation.
- `SPX`: S&P 500 index value.
- `GLD`: Gold price.
- `USO`: United States Oil Fund price.
- `SLV`: Silver price.
- `EUR/USD`: Euro to US Dollar exchange rate.

## Data Preprocessing
1. **Basic Analysis**: Checked for null values, dataset shape, and descriptive statistics using `df.info()` and `df.describe()`.
2. **Feature Extraction**:
   - Extracted `month`, `date`, and `year` from the `Date` column using lambda functions:
     ```python
     df["month"] = df['Date'].apply(lambda x: x.split("/")[0])
     df["date"] = df['Date'].apply(lambda x: x.split("/")[1])
     df["year"] = df['Date'].apply(lambda x: x.split("/")[2])
     ```
3. **Data Visualization**: 
   - Plotted scatter plots and heatmaps to study relationships between columns.

## Model Training
Performed train-test split and used two models for training:
1. **Linear Regression**
2. **Random Forest Regressor**

## Model Evaluation
Evaluated models using:
- **Mean Squared Error (MSE)**
- **R-squared (R²) Score**
- **Root Mean Squared Error (RMSE)**

### Results
- **Linear Regression**: R² Score = 0.9160
- **Random Forest Regressor**: R² Score = 0.9957

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/riitk/gold_price_prediction.git
   cd gold-price-prediction
