# HealthIntelligence

## Culinary Health Intelligence: Predicting Dish Healthiness with Machine Learning

### Overview
HealthIntelligence is a machine learning project aimed at predicting the healthiness of various dishes based on their ingredients, cuisine type, preparation method, and additional features. By leveraging machine learning, this project provides insights to promote healthier food choices and can support applications in dietary recommendation systems.

### Table of Contents
- [Project Motivation](#project-motivation)
- [Dataset](#dataset)
- [Pipeline Stages](#pipeline-stages)
- [Models and Results](#models-and-results)
- [Visualizations](#visualizations)
- [Conclusions](#conclusions)

### Project Motivation
With a rising interest in healthy eating, there's a growing need for systems that can objectively assess the healthiness of food based on its characteristics. This project addresses this need by using machine learning to estimate a healthiness rating for various dishes, informed by ingredients, cuisine, and preparation setting.

### Dataset
The project uses the **MLEnd Yummy Dataset**, containing labeled data of various dishes along with information such as ingredients, cuisine, and healthiness ratings. This dataset enables the prediction of healthiness ratings by training models to understand patterns within the culinary data.

### Pipeline Stages
The machine learning pipeline developed in this project involves the following stages:

1. **Data Collection and Preprocessing**: Data is cleaned, missing values are handled, and categorical variables are encoded.
2. **Feature Engineering**:
   - Tokenization and vectorization of ingredients.
   - One-hot encoding of categorical features like `Cuisine` and `Diet`.
3. **Feature Scaling**: Standardization of numerical features.
4. **Model Training**: Several models are trained and tuned, including Lasso Regression, Random Forest, and SVR.
5. **Evaluation and Interpretation**: Models are evaluated based on Mean Squared Error (MSE) and R-squared metrics, with feature importance analyzed for interpretability.

### Models and Results
Several models were trained and evaluated. The key results are as follows:

| Model                     | Mean Squared Error (MSE) | R-squared (R²) |
|---------------------------|--------------------------|----------------|
| **Lasso Regression**      | 0.7183                   | 0.3615         |
| Random Forest             | 0.7641                   | 0.3208         |
| Support Vector Regressor  | 0.7730                   | 0.3129         |
| XGBoost                   | 0.7789                   | 0.3077         |
| k-Nearest Neighbors       | 0.8909                   | 0.2081         |

- **Lasso Regression** was the best performing model, with an MSE of 0.7183 and an R-squared of 0.3615, making it a strong candidate for real-world applications requiring interpretability and feature selection.

### Visualizations
The project includes several visualizations:
- **Distribution of Healthiness Ratings**: A histogram and box plot of the healthiness ratings in the dataset.
- **Top Ingredients**: A bar chart of the most frequent ingredients, providing insight into common components across dishes.
- **Model Comparison**: Bar charts comparing the MSE and R-squared values of the different models.

### Conclusions
This project demonstrates the potential of machine learning to predict healthiness ratings based on a dish's ingredients and other features. Lasso Regression outperformed other models, showcasing the utility of regularization in high-dimensional spaces.

**Key Insights**:
- Ingredient-related features such as the presence of `salt`, `sugar`, and `oil` are significant predictors of healthiness.
- Lasso Regression's interpretability and feature selection make it ideal for this type of analysis, and it could support applications in dietary recommendation systems.
