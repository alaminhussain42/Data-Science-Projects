# California Housing Dataset - Linear Regression (PySpark)

## Introduction
This project focuses on predicting the `median_house_value` from the California Housing Dataset using linear regression with PySpark's machine learning library. The dataset includes various features related to housing and demographics, which are utilized to build a predictive model.

## Dataset Description
The dataset comprises the following features:
- **longitude**: Longitude of the location (double)
- **latitude**: Latitude of the location (double)
- **housing_median_age**: Median age of the houses (double)
- **total_rooms**: Total number of rooms (double)
- **total_bedrooms**: Total number of bedrooms (double)
- **population**: Population of the area (double)
- **households**: Number of households (double)
- **median_income**: Median income of the area (double)
- **median_house_value**: Median value of houses (double) - Target variable
- **ocean_proximity**: Proximity to the ocean (string) - Categorical feature

## Objective
The goal of this project is to build a linear regression model using PySpark to predict the `median_house_value` based on the other features in the dataset. This will help in understanding how various factors influence housing prices in California.

## Approach
### 1. **Data Preprocessing**
   - **Handling Categorical Data**: Convert the categorical feature `ocean_proximity` into numerical format using encoding techniques.
   - **Feature Scaling**: Normalize or standardize features if necessary to improve model performance.

### 2. **Model Building**
   - **Data Splitting**: Divide the dataset into training and testing sets.
   - **Linear Regression**: Use PySpark's MLlib to build a linear regression model. The model will be trained to predict `median_house_value` based on the provided features.

### 3. **Model Evaluation**
   - **Metrics**: Evaluate the model performance using appropriate metrics such as R², Mean Absolute Error (MAE), and Mean Squared Error (MSE).
   - **Cross-Validation**: Optionally, perform cross-validation to ensure the model's robustness and generalizability.

## Results
The project will provide insights into the performance of the linear regression model, including:
- Model accuracy and performance metrics.
- Key features influencing the `median_house_value`.

## Conclusion
This project demonstrates the use of PySpark for building and evaluating a linear regression model on the California Housing Dataset. It provides practical experience in handling large-scale datasets and applying machine learning techniques using PySpark.

## Technologies Used
- **PySpark**: Apache Spark's Python API for big data processing and machine learning.
- **Python Libraries**: Pandas, NumPy

## Future Work
- **Feature Engineering**: Explore additional features or interactions between features to improve model performance.
- **Advanced Models**: Experiment with more complex models such as Gradient Boosting or Random Forests for potentially better predictions.
- **Hyperparameter Tuning**: Optimize model hyperparameters to enhance accuracy.
