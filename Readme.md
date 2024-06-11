### Project Overview
The company has been instrumental in helping students secure admissions to top colleges worldwide by optimizing their preparation for exams like GMAT, GRE, and SAT. They have recently introduced a feature that allows students to estimate their chances of getting into Ivy League colleges from an Indian perspective. This project involves analyzing the factors that influence graduate admissions and predicting the probability of a student's admission based on various parameters.

### Problem Statement
- Understand the factors important for graduate admissions.
- Analyze the interrelationships among these factors.
- Predict the chances of admission given the relevant variables.

### Data Dictionary
- **Serial No.**: Unique row ID
- **GRE Score**: GRE scores out of 340
- **TOEFL Score**: TOEFL scores out of 120
- **University Rating**: Rating of the university (1-5)
- **SOP**: Strength of Statement of Purpose (1-5)
- **LOR**: Strength of Letter of Recommendation (1-5)
- **CGPA**: Undergraduate GPA (out of 10)
- **Research**: Research experience (0 or 1)
- **Chance of Admit**: Probability of admission (0 to 1)

### Setup
Ensure you have the following libraries installed:
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn
- statsmodels

### Steps

1. **Import Libraries and Dataset**
   - Load the necessary libraries and the dataset.

2. **Data Preprocessing**
   - Drop unnecessary columns (e.g., `Serial No.`).
   - Rename columns for consistency.
   - Check for null values and duplicates.
   - Ensure proper data types for each column.

3. **Exploratory Data Analysis**
   - Analyze distributions and relationships between variables.
   - Perform Chi-square tests to determine dependency between categorical variables.
   - Create pair plots and regression plots for continuous variables to understand correlations.

4. **Model Training**
   - Standardize the dataset to ensure all features have the same scale.
   - Split the data into training and test sets.
   - Train various regression models (Linear Regression, Lasso Regression, Ridge Regression).
   - Evaluate model performance using metrics such as Mean Squared Error (MSE), Mean Absolute Error (MAE), R-squared, and Adjusted R-squared.

5. **Model Evaluation**
   - Check assumptions of linear regression:
     - **Normality of Residuals**: Ensure residuals are normally distributed.
     - **Homoscedasticity**: Ensure residuals have constant variance.
     - **Multicollinearity**: Ensure predictors are not highly correlated.

### Insights
- **University Rating and Research**: Higher-rated universities have more candidates with research experience.
- **LOR and SOP Relationship**: Higher SOP ratings correspond with higher LOR ratings.
- **GRE and TOEFL Scores**: Higher TOEFL scores are correlated with higher GRE scores.
- **Impact of Research**: Candidates with research experience have a higher chance of admission.

### Conclusion
The project successfully identifies key factors influencing graduate admissions and provides a predictive model for estimating the chances of admission based on these factors. The linear regression model, after removing non-significant predictors, performs well with an adjusted R-squared of 80.4%.
