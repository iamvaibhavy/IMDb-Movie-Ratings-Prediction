# IMDb-Movie-Ratings-Prediction


## 📌 Project Overview:-
This project aims to predict IMDb movie ratings using a Random Forest Regressor based on various movie attributes such as Genre, Director, Actors, Year, Duration, and Votes. The goal is to build a machine learning model that accurately predicts ratings and optimize its performance using hyperparameter tuning.


## 🛠 Approach:-
The project follows these key steps:
## Data Collection & Loading
1. The dataset used is IMDb Movies India.csv.
2. It is loaded using pandas.read_csv(), handling encoding issues (latin1 encoding).
## Data Preprocessing
A. Handling Missing Values
1. Categorical columns are filled with "Unknown".
2. Numeric columns are filled with the median value.

B. Feature Transformation
1. Extract numeric year from the "Year" column.
2. Convert "Duration" from string format ('120 min') to float.
3. Convert "Votes" to numeric.

C. Feature Engineering
1. Director Success Rate: Average IMDb rating of the director's previous movies.
2. Genre Average Rating: Average IMDb rating of movies in the same genre.

D. Encoding Categorical Data
1. Label Encoding is used for categorical features (Genre, Director, Actor 1, etc.).

E. Model Selection & Training
1. A RandomForestRegressor is used as the base model.
2. The dataset is split into training (80%) and testing (20%) using train_test_split().
3. The model is trained on the processed dataset.

F. Hyperparameter Tuning
1. GridSearchCV is applied to optimize hyperparameters:
n_estimators: Number of trees in the forest.
max_depth: Maximum depth of each tree.
min_samples_split: Minimum samples to split a node.
min_samples_leaf: Minimum samples per leaf.
2. The best parameters are used to retrain the model.

G. Evaluation Metrics
1. Mean Absolute Error (MAE)
2. Root Mean Squared Error (RMSE)
3. R² Score (Coefficient of Determination)



## 🔄 Preprocessing Summary:-
### A. Handling Missing Data	                                     
1. Categorical values → "Unknown"
2. Numeric values → Filled with median
### B. Feature Transformation
1. Extracted numeric Year
2. Converted Duration to float
3. Converted Votes to numeric
### C. Feature Engineering
1. Added Director Success Rate
2. Added Genre Average Rating
### D. Encoding
1. Label Encoding categorical features



## 📊 Performance Evaluation:-	  
### Initial Model:-
MAE - 32.9%	           
RMSE - 60.3%            
R² Score - 62.6%   
### Tuned Model:-
MAE - 32.5%	           
RMSE - 60.0%	            
R² Score - 63.0% 



## Key Observations:-
1. The tuned model performs better, reducing error and improving accuracy.
2. Feature engineering (e.g., Director Success Rate) improved predictions.
3. Further improvements can be made by experimenting with one-hot encoding instead of label encoding.



## 🚀Future Improvements:-
1. Use One-Hot Encoding instead of Label Encoding for categorical variables.
2. Try other models like Gradient Boosting or XGBoost.
3. Perform Feature Selection to reduce unnecessary attributes.
4. Use Time-Based Splitting instead of random train-test split for more realistic evaluations.



## 📌 Conclusion:-
This project successfully builds an IMDb rating prediction model using Random Forest Regression with optimized hyperparameters. The approach ensures proper data cleaning, feature engineering, and model evaluation, achieving a well-performing model for movie rating prediction.







