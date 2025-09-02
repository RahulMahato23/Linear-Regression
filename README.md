# California Housing Data Analysis and Linear Regression Model

This project performs an exploratory data analysis on the California Housing dataset, cleans the data, and builds linear regression models to predict median house values.

## Dataset

The California Housing dataset contains information about housing in California based on the 1990 census. It includes the following features:

- **longitude**: Longitudinal coordinate
- **latitude**: Latitudinal coordinate
- **housing_median_age**: Median age of houses
- **total_rooms**: Total number of rooms
- **total_bedrooms**: Total number of bedrooms
- **population**: Population in the area
- **households**: Number of households
- **median_income**: Median income of households
- **median_house_value**: Median house value (target variable)
- **ocean_proximity**: Categorical feature indicating proximity to the ocean

## Analysis Steps

1. **Loading and Initial Exploration**: 
   - Load the dataset and examine its structure, columns, and data types
   - Understand the distribution of features and target variable

2. **Missing Data Analysis**:
   - Identify missing values in the dataset
   - Handle missing values by removing rows with incomplete data

3. **Outlier Detection and Removal**:
   - Identify outliers in 'median_house_value' and 'median_income'
   - Remove outliers using the Interquartile Range (IQR) method

4. **Correlation Analysis**:
   - Generate a correlation heatmap to visualize relationships between numerical features
   - Remove the 'total_bedrooms' column due to high correlation with 'total_rooms' and 'households'

5. **Categorical Feature Encoding**:
   - Convert the 'ocean_proximity' categorical feature into dummy variables using one-hot encoding
   - Drop one dummy variable ('ocean_proximity_ISLAND') to avoid multicollinearity

6. **Data Splitting**:
   - Split the data into training and testing sets for model evaluation

7. **Linear Regression Model (Statsmodels)**:
   - Train a linear regression model using the statsmodels library
   - Print model summary including coefficients, R-squared, and other statistical metrics

8. **Assumption Checking**:
   - Check OLS model assumptions (linearity, random sample, exogeneity, homoskedasticity)
   - Create scatter plots of observed vs predicted values and residuals vs fitted values
   - Analyze correlation of residuals with predictors

9. **Linear Regression Model (Scikit-learn)**:
   - Train a linear regression model using the sklearn library
   - Scale numerical features using StandardScaler to improve model performance

10. **Prediction and Evaluation**:
    - Make predictions on the scaled test data
    - Evaluate model performance using Root Mean Squared Error (RMSE)

## Libraries Used

- pandas
- numpy
- matplotlib.pyplot
- seaborn
- scipy.stats
- statsmodels.api
- sklearn.linear_model
- sklearn.model_selection
- sklearn.preprocessing
- sklearn.metrics

## How to Run

1. Upload the `housing.csv` file to your working directory
2. Run the Jupyter notebook sequentially
3. Alternatively, you can run the code in Google Colab by uploading the dataset

## Results

The analysis provides insights into the California Housing dataset, including:
- Distribution patterns of median house values
- Identification and treatment of outliers
- Correlation relationships between features

The linear regression models successfully predict median house values based on the available features, with RMSE providing an estimate of prediction accuracy.

The project demonstrates a complete data science workflow from data exploration and cleaning to model building and evaluation.
