### Project Overview: Predicting Health Insurance Costs Using Machine Learning

#### Objective
The objective of this project is to predict health insurance costs based on various factors such as age, sex, BMI, number of children, smoking habits, and region. This involves performing exploratory data analysis (EDA) and building predictive models to determine the contributing factors and evaluate their performance.

### Data Description
The dataset used for this project is obtained from Kaggle and includes the following features:

- **age**: Age of the primary beneficiary.
- **sex**: Insurance contractor gender (female, male).
- **bmi**: Body Mass Index (BMI), an objective index of body weight (kg/m^2).
- **children**: Number of children covered by health insurance / Number of dependents.
- **smoker**: Smoking status (yes/no).
- **region**: Beneficiary's residential area in the US (northeast, southeast, southwest, northwest).
- **charges**: Individual medical costs billed by health insurance.

### Exploratory Data Analysis (EDA)
EDA is crucial for understanding the dataset and identifying key insights:

- **Feature Balance**: The features 'sex' and 'region' are almost balanced, while most people are non-smokers and obese.
- **Correlation with Charges**:
  - Individuals who smoke and have a BMI above 30 tend to have higher medical costs.
  - Older people who smoke have more expensive charges.
  - People who smoke and are obese have the highest average charges.

### Data Processing and Feature Transformation
1. **Missing and Duplicate Values**:
   - Check for missing values: None found.
   - Check for duplicate values: One duplicate found, which will be removed.
2. **Feature Engineering**:
   - Create a new column 'weight_status' based on the BMI score.
3. **Feature Transformation**:
   - Encode categorical attributes ('sex', 'region', 'weight_status').
   - Ordinal encoding for 'smoker' attribute.

### Modeling
1. **Data Split**:
   - Separate the target variable ('charges') from the features.
   - Split the data into training and testing sets.
2. **Model Selection**:
   - Train models using Linear Regression, Decision Tree, Random Forest, Ridge, and Lasso algorithms.
3. **Hyperparameter Tuning**:
   - Perform hyperparameter tuning to find the best parameters for each model.

### Model Evaluation
The performance of each model is evaluated using various metrics:

- **R2 Score**: Measures the goodness of fit.
- **Training and Testing Accuracy**: Evaluates the model's performance on the training and testing datasets.
- **Mean Absolute Error (MAE)**: Measures the average magnitude of the errors.
- **Root Mean Squared Error (RMSE)**: Measures the square root of the average of the squared errors.

Here is a summary of the model performances:

| Score          | LinearRegression | DecisionTree | RandomForest | Ridge       |
|---------------|------------------|--------------|--------------|-------------|
| R2            | 0.77             | 0.78         | 0.78         | 0.86        |
| Train Accuracy| 0.74             | 1.0          | 0.97         | 0.74        |
| MAE           | 4305.20          | 2798.83      | 2608.55      | 4311.10     |
| Test Accuracy | 0.77             | 0.78         | 0.86         | 0.77        |
| RMSE          | 6209.88          | 6067.50      | 4841.88      | 6238.13     |

### Conclusion
Based on the evaluation metrics, the best model can vary depending on the criteria. However, in this case:

- **Linear Regression** was found to have the best overall score in terms of MAE, RMSE, and R2 score, making it the best-fitted model based on the training and testing accuracy.

### Additional Insights and Models
Other studies and projects have also explored similar datasets and models:
- **XGBoost and Gradient Boosting**: These models have also shown high performance in predicting health insurance premiums, with high accuracy and good performance metrics such as R2 score and RMSE.
- **Artificial Neural Networks (ANNs)**: ANNs have been used to achieve an accuracy of 92.72% in predicting health insurance premiums, evaluating the model using metrics like RMSE, MSE, MAE, and R2.

By comparing different models and tuning their hyperparameters, you can identify the most accurate and efficient model for predicting health insurance costs.
