# Car-Price-Prediction

Car Price Prediction Report
Aim
The primary objective of this project was to build a machine learning model to predict car prices accurately based on various car attributes. The goal was to identify the most influential features impacting car prices and evaluate the performance of different models to select the best-performing one.

Methodology
1. Data Preprocessing
Dataset Exploration: Loaded the dataset and explored its structure using statistical summaries and data types.

Handling Missing Values: Removed rows with missing data to maintain data integrity.

Feature Engineering:

Extracted 'CarBrand' and 'CarModel' from the 'CarName' column.

Dropped irrelevant columns that did not contribute significantly to car price predictions, including:

car_ID (unique identifier)

CarName (replaced by 'CarBrand' and 'CarModel')

drivewheel (low relevance)

curbweight, carwidth (high correlation with enginesize)

highwaympg (correlated with citympg)

symboling, stroke, compressionratio (weak correlation with price)

Encoding Categorical Variables: Applied Label Encoding to transform categorical data into numerical form.

2. Model Development
Train-Test Split: Split the dataset into 80% training and 20% testing data.

Feature Scaling: Standardized the features using StandardScaler to improve model performance.

Model Selection: Implemented and evaluated the following models:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

Gradient Boosting Regressor

Support Vector Regressor (SVR)

3. Model Evaluation
Metrics Used:

Mean Squared Error (MSE)

R² Score (Coefficient of Determination)

Results:

Random Forest Regressor performed the best with:

R² = 0.829 (Strong fit)

Mean Absolute Error (MAE) = 2520

Root Mean Squared Error (RMSE) = 3844

Linear Regression, Ridge, and Lasso had moderate performance (R² ≈ 0.78).

Support Vector Regressor performed the worst (R² = -0.09).

4. Hyperparameter Tuning
Applied hyperparameter tuning to optimize the Random Forest model.

Improvements Post-Tuning:

MAE decreased by 98.37 units

MSE decreased by 1,102,113 units

RMSE decreased by 144.74 units

R² increased from 0.8264 to 0.8399

Feature Importance
The most influential features affecting car prices were:

enginesize (Most significant)

horsepower

citympg

carlength

wheelbase

Other features like fuel type, car body, and engine type had minimal impact on price prediction.

Final Prediction
Using the optimized Random Forest model, a sample prediction yielded an estimated car price of $12,693.11.

Conclusion
Random Forest Regressor emerged as the most accurate model for predicting car prices due to its superior R² score and lower error metrics.

Feature importance analysis revealed that engine size and horsepower are the most critical factors influencing car prices.

Hyperparameter tuning significantly enhanced model accuracy and precision, making the tuned Random Forest model the best choice for future predictions.

The project successfully developed an accurate and robust car price prediction model, offering valuable insights into the key attributes affecting car valuations.
