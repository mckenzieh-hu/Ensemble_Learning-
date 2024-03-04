# Electricity Price Modelling for France and Germany

## Overview
This project aims to estimate daily price variations of short-term electricity futures contracts in France and Germany using weather, energy, and commercial data. The challenge focuses on understanding the impact of various factors, including local weather conditions, global phenomena, and geopolitical events on electricity prices.

## Data Description
We utilize three CSV datasets: `X_train` for training inputs, `Y_train` for training outputs, and `X_test` for test inputs, covering weather measurements, commodity price changes, energy production measures, and electricity usage metrics.

NB: The input data X_train and X_test represent the same explanatory variables but over two different time periods.
## Methodologies

### Data Pre-processing
- **Outlier Removal**: Applied Z-Score method to improve model performance by identifying and removing outliers.
- **Skewed Data Handling**: Log-transformation was used for features with skewness greater than 1 to normalize data distribution.
- **Missing Values Handling**: Explored mean, median, and KNN imputation methods, with the mean method showing slight superiority.

### Feature Engineering
- Developed interaction, polynomial, and lagged features to capture complex relationships and temporal trends in the data.

## Model Selection and Evaluation
- Evaluated models including Decision Tree, Random Forest, Extra Trees, Gradient Boost, AdaBoost, and XGBoost, with forest ensemble methods showing higher performance.
- Used Spearman correlation and Mean Squared Error (MSE) as evaluation metrics.

## Feature Importance
- Analyzed feature importance to understand the drivers behind electricity price variations, noting differences between France and Germany related to international factors and domestic production capabilities.

## Conclusions and Future Directions
- Forest ensemble methods outperformed boosting methods. Feature importance analysis revealed critical insights into price variation drivers.
- Future work could explore additional data sources, alternative modeling techniques, or improvements to the current approach.

## Usage
Please refer to the Jupyter notebook (`EL_modelling_to_work.ipynb`) for detailed code and analysis.

## Contributions
This project represents a collaborative effort among team members, with tasks distributed to leverage individual strengths and expertise.
