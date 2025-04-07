# Instagram Follow Prediction using Machine Learning

## Overview

This repository contains the code and documentation for a project investigating the development of machine learning models to predict Instagram follows based on various engagement and impression metrics. The project leverages a dataset with numerical features such as impressions, likes, comments, shares, saves, and profile visits, as well as text-based features like captions and hashtags. The aim is to identify the key factors that drive user follow behaviour on social media.

A **Random Forest regression model** was primarily employed for its robustness and ability to handle complex interactions within the dataset. Additionally, a **Support Vector Machine (SVM)** and a **Naive Bayes Classifier** were also utilised .

The Random Forest model achieved a high level of predictive accuracy with an **R-squared of 0.85, Mean Absolute Error (MAE) of 9.485, and Root Mean Square Error (RMSE) of 17.50**. The SVM model achieved an accuracy of **81%**, and the Naive Bayes model achieved an accuracy of approximately **75%**.

This project demonstrates the use of machine learning in social media analytics to uncover insights into which interactions contribute most significantly to user retention and follower growth, providing valuable guidance for optimising engagement strategies on social media platforms.

## Problem Statement

This project addresses the problem of **predicting Instagram follows** by leveraging a machine learning approach to analyse various engagement metrics. The goal is to determine how specific user interactions—such as likes, comments, shares, saves, impressions, and profile visits—contribute to follower growth and to build a model that can accurately predict follow counts based on these metrics.

## Objectives

The main objectives of this project were to:

*   Develop a **predictive machine learning model** that accurately forecasts Instagram follows based on engagement metrics like likes, comments, shares, and profile visits.
*   Identify which **engagement factors most influence follower growth** .
*   Provide **actionable insights** for optimising Instagram content strategies .
*   Evaluate **model performance** across several metrics to ensure reliability and offer practical recommendations.

## Significance

This project is significant because it provides a **data-driven approach** to understanding and optimising Instagram follower growth, a critical metric for influencers, marketers, and brands aiming to expand their reach. By identifying which engagement metrics most influence follows, the project offers actionable insights that can improve content strategies, ultimately leading to higher audience engagement and visibility. The predictive model equips users with a scalable tool for making informed decisions in the social media landscape.

## Dataset
follow the link - https://www.kaggle.com/datasets/amirmotefaker/instagram-data

## Methodology

### Approach

The project employed a machine learning approach to analyse user engagement patterns on Instagram to understand content effectiveness and audience interests. This analysis helps in categorising posts and users based on similar engagement patterns, forming the foundation for tailored content strategies. The machine learning models used were:

*   **Support Vector Machine (SVM):** Applied to find the optimal hyperplane that best separates engagement metrics for predicting follow counts, effective for high-dimensional data and non-linear relationships.
*   **Random Forest:** An ensemble learning method combining multiple decision trees to improve prediction accuracy and reduce overfitting, useful for identifying feature importance.
*   **Naive Bayes Classifier:** A probabilistic model used as a baseline to classify engagement behaviours by calculating the likelihood of follow counts based on individual engagement features.

### Data Pre-processing

The dataset underwent the following pre-processing steps:

*   **Handling Missing Data:** The dataset did not contain any missing values.
*   **Categorical Data Encoding:** Text-based features (Caption and Hashtags) were converted into numerical vectors using the **TF-IDF (Term Frequency-Inverse Document Frequency) encoding** technique.
*   **Normalization and Scaling:** Numerical attributes were scaled using **Z-score Normalization** to ensure features were on a similar scale, which improves the performance of many machine learning models.

### Model Training

The dataset was split into **70% for training and 30% for testing** to ensure the models could generalise to new, unseen data. The three machine learning models (SVM, Random Forest, and Naive Bayes Classifier) were trained to predict the number of "follows" based on the pre-processed Instagram engagement metrics.

## Results and Analysis

### Model Performance

*   **Support Vector Machine (SVM):** Achieved an accuracy of **81%**.
    *   Precision for Class 0 (low follows): **0.81**.
    *   Precision for Class 1 (high follows): **0.80**.
    *   Recall for Class 0: **0.85**.
    *   Recall for Class 1: **0.75**.
*   **Random Forest:** Achieved the highest accuracy of approximately **90%**.
    *   **Mean Absolute Error (MAE): 9.485**.
    *   **Root Mean Squared Error (RMSE): 17.51** .
    *   **R-squared (R²): 0.849**.
*   **Naive Bayes Classifier:** Achieved an accuracy of approximately **75%**, the lowest among the three models. It struggled with precision for the "high follows" class.

### Feature Importance

The **Random Forest model** identified **likes, shares, and profile visits** as the most influential predictors of follower growth. High impressions from hashtags and the explore page also indirectly increased follow counts.

### Engagement Patterns

Posts with higher **likes, shares, and comments** were more likely to attract follows.

## Conclusion

This project successfully demonstrated the application of machine learning models to predict Instagram follower growth based on engagement metrics. The **Random Forest model** showed the best performance with a high accuracy and R-squared value, indicating its suitability for this prediction task. The study highlights the significant influence of metrics like **likes and shares** on gaining followers.

