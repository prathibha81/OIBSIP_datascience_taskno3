#  Car Price Prediction using Machine Learning

##  Overview

This project builds a machine learning model to predict the selling price of cars based on key features such as mileage, age, fuel type, and transmission. It demonstrates the end-to-end workflow of a regression problem, from data preprocessing to model evaluation.



##  Problem Statement

To develop a predictive model that accurately estimates car prices using historical data and relevant features.



##  Objectives

* Perform data analysis and preprocessing
* Build and compare multiple regression models
* Optimize model performance
* Evaluate using appropriate metrics
* Generate predictions for unseen data


##  Dataset Description

The dataset includes the following features:

* Car_Name
* Year
* Selling_Price (Target)
* Present_Price
* Driven_kms
* Fuel_Type
* Selling_type
* Transmission
* Owner



##  Exploratory Data Analysis (EDA)

* Checked data distribution and correlations
* Identified important features affecting price
* Visualized relationships using heatmaps and pairplots



##  Data Preprocessing

* Created new feature: **Car_Age**
* Removed irrelevant columns (Car_Name, Year)
* Converted categorical variables using One-Hot Encoding
* Prepared dataset for model training



##  Train-Test Split

The dataset was split into:

* Training Data: 80%
* Testing Data: 20%
  
This ensures that the model is evaluated on unseen data, which helps measure its generalization ability.



##  Models Used

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor (Best Performing Model)

##  Random Forest Regressor – Detailed Explanation

###  Beginner Level Explanation

Random Forest is an ensemble machine learning algorithm that combines multiple decision trees to make better predictions.

Instead of relying on a single decision tree (which can overfit), Random Forest builds many trees using different subsets of the data and features. Each tree makes a prediction, and the final output is the average of all predictions.

####  How it Works:

1. Random subsets of training data are selected (Bootstrap Sampling)
2. Multiple decision trees are trained independently
3. Each tree makes a prediction
4. Final prediction = Average of all tree predictions

####  Why it Works Well:

* Reduces overfitting compared to a single decision tree
* Handles non-linear relationships effectively
* Works well with both numerical and categorical data
* Requires minimal preprocessing


###  Key Parameters

* **n_estimators** → Number of trees in the forest
* **max_depth** → Maximum depth of each tree
* **min_samples_split** → Minimum samples required to split a node
* **random_state** → Ensures reproducibility



###  Advanced Level Explanation

Random Forest is based on the concept of **Bagging (Bootstrap Aggregation)** and **feature randomness**, which improves model generalization.

####  Core Concepts:

**1. Bagging (Bootstrap Sampling)**
Each tree is trained on a different random subset of the dataset. This reduces variance and prevents overfitting.

**2. Feature Randomness**
At each split, only a random subset of features is considered. This ensures diversity among trees.

**3. Aggregation**
Final prediction is obtained by averaging outputs of all trees, which stabilizes predictions.


###  Advantages

* High accuracy for regression problems
* Handles large datasets efficiently
* Robust to noise and outliers
* Less prone to overfitting than decision trees



###  Limitations

* Slower compared to simple models
* Less interpretable
* Requires more computational resources



##  Model Comparison

| Model             | Type              | Pros                           | Cons                        | Performance  |
| ----------------- | ----------------- | ------------------------------ | --------------------------- | ------------ |
| Linear Regression | Simple            | Fast, interpretable            | Cannot handle non-linearity | Low–Moderate |
| Decision Tree     | Non-linear        | Easy to understand             | Overfitting                 | Moderate     |
| Random Forest     | Ensemble          | High accuracy, robust          | Less interpretable          | High         |
| Gradient Boosting | Ensemble          | Very high accuracy             | Sensitive to tuning         | Very High    |
| XGBoost           | Advanced Ensemble | Best performance in real-world | Complex, needs tuning       | Excellent    |



##  Why Random Forest is Best for This Project

* Captures complex relationships between car features and price
* Reduces overfitting through multiple trees
* Performs consistently well without heavy tuning
* Suitable for real-world datasets with mixed features


##  Model Evaluation

* Model_Score : 0.9554841970229158
* R² Score : 0.9564270702931321
* Mean Absolute Error (MAE) : 0.6590632916468783
* Root Mean Squared Error (RMSE) :  1.0018622186005521



##  Results

* Random Forest achieved the best performance
* High R² score with low prediction error
* Model generalizes well on test data
* Random Forest is a powerful and reliable regression algorithm that improves prediction accuracy by combining multiple decision trees. It is widely used in real-world machine learning applications due to its balance between performance and robustness.


##  Sample Prediction

The model can predict car prices based on user-provided input features.



##  Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn



##  Project Structure


car-price-prediction/
│

├── car_data.csv

├── car_price_prediction.ipynb

├── requirements.txt

└── README.md



##  How to Run

1. Clone the repository:

```
git clone https://github.com/your-username/OIBSIP_datascience_taskno3.git
```

2. Navigate to the project folder:

```
cd car-price-prediction
```

3. Install dependencies:

```
pip install -r requirements.txt
```

4. Run the notebook or prediction script

```
jupyter notebook car_price_prediction.ipynb
```

##  Future Improvements

* Deploy as a web application
* Use advanced models like XGBoost
* Add user interface for predictions



##  Author
Ummalla Prathibha Data Science Intern

Developed as part of a machine learning project to demonstrate regression modeling and real-world application.
