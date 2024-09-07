# Medical Insurance Premium Cost Prediction

## Overview

This project aims to predict medical insurance premiums using machine learning models. We utilized a dataset containing demographic information such as age, sex, BMI, children, smoking habits, region, and insurance charges. By leveraging a neural network built in TensorFlow, the model achieved a high level of accuracy, explaining over 85% of the variance in the target variable.

### Key Highlights:
- **Model Used:** Neural Network (TensorFlow, Keras)
- **Performance Metrics:** R² = 0.8563, Adjusted R² = 0.8519
- **Techniques Applied:** Feature Encoding, Data Scaling, Neural Network Hyperparameter Tuning

## Dataset

The dataset contains 1,338 entries with 7 features:

| Column    | Data Type | Description                                   |
|-----------|-----------|-----------------------------------------------|
| `age`     | int       | Age of the individual                         |
| `sex`     | object    | Gender (encoded as male/female)               |
| `bmi`     | float     | Body Mass Index                               |
| `children`| int       | Number of children                            |
| `smoker`  | object    | Whether the individual smokes (yes/no)        |
| `region`  | object    | Residential region                           |
| `charges` | float     | Annual medical insurance premium              |

### Preprocessing
- **Label Encoding** was applied to the `sex` and `smoker` columns.
- **One-Hot Encoding** was applied to the `region` column.
- **Feature Scaling** was conducted using StandardScaler for continuous variables.

## Model Development

We used TensorFlow and Keras to build a neural network for predicting insurance charges. The network was optimized using techniques like dropout and batch normalization, and tuned with the Keras Tuner library.

### Key Libraries:
- `tensorflow`, `keras_tuner`, `scikit-learn`

### Neural Network Structure:
- **Input Layer:** Accepts all feature columns.
- **Hidden Layers:** Dense layers with batch normalization and dropout to prevent overfitting.
- **Output Layer:** A single neuron predicting the insurance premium.

## Results

The model demonstrated strong predictive performance:
- **R²:** 0.8563
- **Adjusted R²:** 0.8519

These metrics suggest that the model is well-suited for predicting insurance costs, explaining around 85% of the variance in the target variable.

## Conclusion

Our neural network model significantly improved over the baseline, making it a viable option for predicting medical insurance premiums. The robust fit demonstrated by the R² values implies that the model generalizes well to unseen data and is ready for real-world applications.

## Future Improvements
- Incorporating additional features like medical history or family background.
- Experimenting with other advanced models such as Gradient Boosting or Random Forest.
