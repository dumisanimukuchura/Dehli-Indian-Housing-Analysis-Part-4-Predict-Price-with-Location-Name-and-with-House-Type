
# Dehli Indian Housing Part 4: Predict Price with Location Name and House Type

## Project Overview
This project explores the predictive capabilities of high-cardinality features, such as **location names**, and categorical features, such as **house types**, in determining housing rental prices in Delhi. Using **Linear Regression** and **Ridge Regression**, the analysis evaluates the performance of models built on these features, comparing their ability to predict rental prices (`price_approx_usd`).

## Contact Details
- Email: dumisanimukuchura@gmail.com
- LinkedIn: https://www.linkedin.com/in/dumisani-maxwell-mukuchura-4859b7170/

## Objectives
- Investigate the influence of `location` and `house_type` features on rental prices.
- Build and evaluate baseline and regression models for:
  - Location names (`location`).
  - House types (`house_type`).
- Use regularization techniques (Ridge Regression) to assess their impact on model performance.
- Visualize and communicate findings through graphs and equations.

---

## Dataset Description
The dataset contains housing rental details in Delhi, India. Below are the columns relevant to this analysis:

| Column              | Description                                |
|---------------------|--------------------------------------------|
| `location`          | Name of the location (categorical)         |
| `house_type`        | Type of house (e.g., villa, apartment)     |
| `price_approx_usd`  | Rental price in USD                       |
| `numBathrooms`      | Number of bathrooms                       |
| `numBedrooms`       | Number of bedrooms                        |
| `house_size_in_sqft`| Size of the house in square feet           |

---

## Key Steps

### **1. Data Preparation**
- Imported and cleaned the dataset.
- Verified that `location` and `house_type` had no null values.
- Encoded categorical variables (`location`, `house_type`) using one-hot encoding.
- Split the data into training and testing sets.

### **2. Exploratory Data Analysis (EDA)**
- Analyzed feature distributions and their impact on price.
- Visualized rental prices grouped by:
  - Locations (`location`).
  - House types (`house_type`).
- Identified that:
  - Certain locations contribute more significantly to higher rental prices.
  - House types have moderate variability in price.

### **3. Baseline Models**
- Predicted the mean rental price for all records as the baseline.
- Calculated the **Mean Absolute Error (MAE)** for both features:
  - Baseline MAE: `$2076.93` for both location and house type models.

### **4. Regression Models**
- **Location-Based Model**:
  - Features: One-hot encoded `location`.
  - MAE:
    - Training: `$1217.60`
    - Test: `$1299.97`
- **House Type-Based Model**:
  - Features: One-hot encoded `house_type`.
  - MAE:
    - Training: `$1628.89`
    - Test: `$1718.23`

### **5. Ridge Regression Models**
- Applied Ridge regression with regularization to reduce overfitting.
- Ridge regression showed slightly higher MAE than standard linear regression models.

### **6. Communication of Results**
- Developed mathematical models:
  - Location Model: `rental price = 2943.78 + (346.36 * location_Saket) + ...`
  - House Type Model: `rental price = 3984.09 + (-577.41 * house_type_Independent Floor) + ...`
- Visualized results:
  - Bar charts showing feature importance.
  - Scatter plots overlaying regression predictions.

---

## Tools and Libraries Used
- **Python**
- **Pandas** and **NumPy**: Data manipulation and preprocessing.
- **Matplotlib** and **Seaborn**: Data visualization.
- **Scikit-learn**: Model training and evaluation.

---

## How to Run the Project
1. **Set Up the Environment**:
   - Install required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.
   - Ensure the dataset (`Dehli-Indian-Housing-Clean-Data.csv`) is in the `data` directory.
2. **Run the Jupyter Notebook**:
   - Execute cells sequentially to preprocess data, train models, and evaluate performance.
3. **Analyze Results**:
   - Compare metrics and visualizations to understand model effectiveness.

---

## Folder Structure
Dehli-Indian-Housing-Analysis-Part4/ 
├── data/ 
│ └── Dehli-Indian-Housing-Clean-Data.csv # Cleaned dataset 
├── notebook/ 
│ └── Dehli_Indian_Housing_MLR_Part4.ipynb # Jupyter Notebook 
├── visualizations/ 
│ └── plots/ # Saved plots (optional) 
├── README.md # Project documentation

## Project Outcome
- Models based on **Location Names** had better predictive performance than those based on **House Types**.
- Linear regression models outperformed Ridge regression in terms of test MAE.
- Visualizations highlighted the significance of specific locations and house types in price prediction.

---

## Future Work
- Include additional features like `numBathrooms` and `house_size_in_sqft` to improve accuracy.
- Explore embedding techniques for high-cardinality categorical variables.
- Test advanced algorithms such as Random Forest, Gradient Boosting, or Neural Networks.

---

## References
- **Dataset**: [Kaggle](https://www.kaggle.com/datasets/bhavyadhingra00020/india-rental-house-price)