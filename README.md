# Diamonds Data Analysis Project

## Overview
This project focuses on analyzing and predicting diamond prices using various machine learning models. The primary objective is to preprocess the data, explore its features, and develop regression models to accurately predict the price of diamonds. The dataset used in this project is the **diamonds.csv**, which contains information about different diamond characteristics and their respective prices.

## Dataset
The **diamonds.csv** dataset includes the following key features:

- **carat**: Weight of the diamond.
- **cut**: Quality of the cut (e.g., Fair, Good, Very Good, Premium, Ideal).
- **color**: Diamond color, from J (worst) to D (best).
- **clarity**: Clarity of the diamond (e.g., I1, SI2, SI1, VS2, VS1, VVS2, VVS1, IF).
- **depth**: Total depth percentage = (z / mean(x, y)) * 100.
- **table**: Width of the top of the diamond relative to the widest point.
- **price**: Price of the diamond in US dollars.
- **x**: Length of the diamond in mm.
- **y**: Width of the diamond in mm.
- **z**: Depth of the diamond in mm.

## Key Steps

### 1. Data Preprocessing
- Handling missing values:
  - Categorical features (e.g., `cut`, `color`, `clarity`) were filled with their mode.
  - Continuous features (e.g., `carat`, `depth`, `table`) were filled with their median values.
- Encoding categorical features using **One-Hot Encoding**.
- Normalizing numerical features using **StandardScaler** after splitting the data into training and validation sets to avoid data leakage.

### 2. Exploratory Data Analysis (EDA)
- Visualized the distribution of features such as `carat`, `cut`, and `price`.
- Investigated correlations between numerical features and the target variable (`price`).

### 3. Model Training and Evaluation
The following models were trained and evaluated using Mean Absolute Error (MAE):

#### Baseline Model
- Predicted the mean price for all diamonds as a simple baseline.
- **Baseline MAE:** 6663.96

#### Linear Regression
- Captures linear relationships between features and the target.
- **MAE:** 2968.92

#### K-Nearest Neighbors (KNN)
- Identifies local patterns by averaging the target values of the nearest neighbors.
- **MAE:** 1559.39

#### Decision Tree
- Splits data based on feature thresholds to minimize prediction error.
- **MAE:** 104.27

#### Random Forest
- Combines predictions of multiple decision trees for better generalization.
- **MAE:** 63.67 (best-performing model).

### 4. Results and Insights
- **Random Forest** achieved the lowest MAE, demonstrating its ability to handle the nonlinear relationships and feature interactions in the dataset.
- The preprocessing steps, particularly handling missing values and scaling numerical features, contributed significantly to improving model performance.

## Requirements
To run the project, you need the following Python libraries:

- `pandas`
- `numpy`
- `scikit-learn`

Install the required packages using pip:

```bash
pip install pandas numpy scikit-learn
```

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/mr1necs/Tax-Free-Diamonds.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Tax-Free-Diamonds
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook main.ipynb
   ```
4. Run the notebook cells to see the preprocessing steps, model training, and evaluation results.

## File Structure
- **diamonds.csv**: Dataset used in the project.
- **main.ipynb**: Jupyter Notebook containing all code for data preprocessing, analysis, and modeling.
- **README.md**: Project documentation.

