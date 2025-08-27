# Bengaluru House Price Prediction 🏡

## Overview

This is an end-to-end data science project that builds a machine learning model to predict house prices in Bengaluru, India. Using a dataset from Kaggle, the model is trained to estimate property values based on key features like location, size in square feet, and the number of bedrooms and bathrooms.

The entire process, from raw data to a working prediction function, is documented in the `House_prediction(Bengaluru).ipynb` Jupyter Notebook.

---

## 🚀 Project Pipeline

The project follows a standard data science workflow:

1.  **Data Loading & Exploration:** The dataset is loaded using Pandas for an initial assessment of its structure, features, and data types.
2.  **Data Cleaning:** Handled missing values, standardized inconsistent text data (e.g., '2 BHK' vs. '2 Bedroom'), and cleaned complex features like `total_sqft` which contained ranges.
3.  **Feature Engineering:** Created the insightful `price_per_sqft` feature to aid in analysis and outlier detection.
4.  **Outlier Removal:** Implemented both business logic (e.g., minimum sqft per bedroom) and statistical methods (standard deviation) to remove anomalous data points and improve model reliability.
5.  **Exploratory Data Analysis (EDA):** Visualized the cleaned data using Matplotlib to understand distributions and relationships between features.
6.  **Modeling:** Built and evaluated a **Linear Regression** model using Scikit-learn to establish a performance baseline and make predictions.

---

## 🛠️ Technologies Used

* **Language:** Python
* **Libraries:**
    * Pandas (for data manipulation)
    * NumPy (for numerical operations)
    * Scikit-learn (for machine learning)
    * Matplotlib (for data visualization)
* **Environment:** Jupyter Notebook
* **Version Control:** Git & GitHub

---

## ⚙️ How to Use

To predict the price of a house, you can use the `predict_price` function defined in the notebook.

**Example Usage:**

```python
# First, run the notebook to train the lr_model

# Then, use the function to predict a price
# predict_price(location, sqft, bath, bhk)

price = predict_price('Whitefield', 1200, 2, 2)
print(f"Predicted Price: {price:.2f} Lakhs")
# Expected Output: Predicted Price: 105.45 Lakhs (your value may vary slightly)
