# Tax-Free-Diamonds
 A project to develop a pricing model for diamonds based on their characteristics, exploring new investment opportunities following the VAT exemption.


## Overview
The **Tax-Free-Diamonds** project aims to develop a pricing model for diamonds using regression techniques. With the removal of VAT on diamonds starting October 1, diamonds are emerging as a new investment tool. This project explores their characteristics and price trends to create an effective predictive model.

---

## Project Objectives
1. **Data Cleaning**:
   - Deduplicate entries for diamonds listed multiple times.
   - Identify and handle anomalies in pricing and diamond characteristics.
   - Adjust prices for inflation within distinct groups.

2. **Regression Modeling**:
   - Develop baseline models using linear regression.
   - Evaluate performance using metrics like MSE or MAE.
   - Compare encoding techniques (LabelEncoder, OneHotEncoder, TargetEncoder).
   - Normalize data and handle missing values (e.g., for `fluor`).

3. **Model Comparison**:
   - Train and evaluate advanced models including KNN, Decision Trees, and Ensemble Methods (e.g., Random Forest).
   - Compare results to identify the best-performing model.

4. **Insights and Conclusion**:
   - Summarize findings and propose an optimal pricing strategy for diamonds.

---

## Dataset
The dataset `diamonds.csv` contains diamond characteristics and prices as of 2022-07-01 from the James Allen platform. Key features include:
- **Physical Attributes**: `carat`, `shape`, `color`, `clarity`, `cut`, `x`, `y`, `z`, `depth_perc`, `tablepercent`
- **Quality Metrics**: `symmetry`, `polish`, `fluor`
- **Grouping**: `size_group`, `big_size_group`, `quality_group`
- **Other Details**: `price`, `price_per_carat`, `platform`, `date`, `id`

---

## Steps

### **1. Data Preparation**
- Merge duplicate records by diamond `id`, keeping the latest price.
- Identify anomalies in pricing and characteristics.
- Adjust for inflation by calculating inflation coefficients across groups.

### **2. Model Building**
- Split data into training and validation sets.
- Build a baseline regression model using LabelEncoder.
- Experiment with advanced techniques:
  - OneHotEncoder and TargetEncoder for categorical variables.
  - Normalize features using StandardScaler.
- Train additional models: KNN, Decision Trees, and Random Forest.

### **3. Evaluation**
- Compare models using performance metrics (e.g., MSE/MAE).
- Analyze improvements from advanced preprocessing and encoding techniques.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/TaxFreeDiamonds.git
   ```
2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the dataset `diamonds.csv` and place it in the project directory.

---

## Usage
1. Run the Jupyter notebook `main.ipynb` to process the data and build models.
2. Adjust parameters in the code for experiments with different models or encoders.
3. Evaluate the model outputs and check the final pricing predictions.

---

## Results
The results include:
- A cleaned and inflation-adjusted dataset.
- Performance comparison across models:
  - Linear Regression (baseline)
  - KNN Regressor
  - Decision Trees
  - Random Forest
- Insights into key features influencing diamond prices.

---

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your improvements.
