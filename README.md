# used cars
Machine learning project for predicting used car prices. The project includes data cleaning, handling missing values, feature engineering, categorical encoding, and training multiple regression models including Linear Regression, Decision Tree, Random Forest, and Gradient Boosting. The best model achieved an R² score of approximately 0.81.
Used Car Price Prediction

This project is about predicting the price of used cars using machine learning.

I started by loading the dataset and checking the columns, data types, and missing values.

The first thing I focused on was cleaning the data before training any model.

I checked for missing values and values that were stored in the wrong format.

The price column needed cleaning because some values contained symbols and commas.

After cleaning the price, I converted it into a numerical column.

I also checked the numerical and categorical features separately.

Some categorical features had to be converted into numbers before training.

I used encoding to make these features usable by machine learning models.

I also created useful features from the original data when possible.

After preparing the data, I separated the features from the target price.

Then I split the dataset into training and testing data.

I started with Linear Regression as a simple baseline model.

After that, I tested other models to see if I could improve the results.

The models included Decision Tree, Random Forest, Ridge, KNN, and Gradient Boosting.

I didn’t want to choose a model just because it was more complicated.

Instead, I compared the models using actual results.

For the regression evaluation, I used R², MAE, and RMSE.

R² helped me understand how well the model explained the target values.

MAE showed the average size of the prediction error.

RMSE helped me see the effect of larger prediction errors.

During the project, I changed the preprocessing and tested the models again.

This helped me understand how data preparation affects model performance.

The final model was selected based on its performance on unseen test data.

This project helped me practice the complete machine learning workflow.

I learned that cleaning and preparing the data can be just as important as choosing the model.

what i use

Python, Pandas, NumPy, Matplotlib, and Scikit-learn.

Future Improvements

I would like to add better feature engineering, hyperparameter tuning, cross-validation, and eventually deploy the model as a web application.
