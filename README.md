# Rio de Janeiro Tourist Data Analysis and Prediction

This notebook analyzes tourist data for Rio de Janeiro from 2006 to 2019, focusing on predicting the number of tourists arriving by air.

## Dataset Description
The dataset contains information about tourists to Rio de Janeiro by country, including:
*   **Country**: Origin country of tourists.
*   **Total**: Total number of tourists arrived.
*   **Total_Arrived_by_air**: Number of tourists arrived by air.
*   **Total_Arrived_by_sea**: Number of tourists arrived by sea.
*   **Region**: Continent region.
*   **Continent**: Continent.
*   **Year**: Year.

## Project Steps
1.  **Data Loading and Preprocessing**: The raw data is loaded from a CSV file. Column names are standardized to English.
2.  **One-Hot Encoding**: Categorical features (Country, Region, Continent) are converted into numerical format using one-hot encoding.
3.  **Model Implementation and Evaluation**: Various regression models (Linear Regression, Lasso, Ridge, Decision Tree, Random Forest, Gradient Boosting, K-Nearest Neighbor) are implemented and evaluated using cross-validation to predict `Total_Arrived_by_air`.
4.  **Ensemble Methods**: Bagging Regressor, Stacking Regressor, and Voting Regressor are applied to explore improvements in prediction accuracy.
5.  **Log Transformation Analysis**: The effect of log transformation on skewed numerical features is investigated to see its impact on model accuracy.

## Key Findings
*   Initial model evaluation identified Random Forest Regressor and Gradient Boosting Regressor as strong performers with high accuracy scores.
*   Further testing with Gradient Boosting Regressor and Random Forest Regressor on different train-test splits showed consistent accuracy ranges.
*   Bagging Regressor with Gradient Boosting as the base estimator yielded a high cross-validation score of `0.9237`.
*   Log transformation of skewed numerical features, while often beneficial, led to a decrease in accuracy for the Gradient Boosting Regressor in this specific case, suggesting the original scale was more effective for this dataset and model configuration.
