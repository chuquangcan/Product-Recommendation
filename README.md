# README: Product Purchase Prediction using Machine Learning

## Overview
This project applies machine learning models to predict the products that customers are likely to purchase. By leveraging customer behavior and financial data, the system aims to provide personalized product recommendations to improve customer experience and engagement.

## Installation & Setup
To run the project, follow these steps:
1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Preprocess the dataset:
   - Run `Clean.ipynb` to clean and prepare the dataset.
3. Perform data visualization:
   - Run `Visualize.ipynb` to explore and analyze the dataset.
4. Train machine learning models:
   - Execute `Model_KNN.ipynb` and `Ensemble_model.ipynb` to train and evaluate models.

---
## I. Problem Statement
A retail and personal finance bank aims to enhance its product recommendation system. The current approach results in imbalanced exposure, where a subset of customers receives multiple suggestions while others receive none. This discrepancy impacts customer satisfaction and engagement.

To address this, the goal is to develop a smarter, data-driven recommendation system that utilizes customer financial behavior and product usage trends to generate more relevant and balanced product suggestions.

## II. Objectives
- Develop an effective predictive model to understand customer needs and recommend suitable products.
- Improve customer satisfaction by ensuring balanced product exposure.
- Enhance cross-selling and upselling strategies to drive revenue growth and competitive advantage.

## III. Key Requirements
### 1. Data Discovery & Cleaning
- Use visualization tools to explore data insights regarding customers, products, and business trends.
- Handle missing values, outliers, and inconsistencies for accurate analysis.

### 2. Feature Engineering
- Create meaningful derived features to enhance model performance.
- Select the most impactful features for prediction.

### 3. Model Training
- Experiment with various techniques, including:
  - Probabilistic models
  - Regression models
  - Collaborative filtering
  - Deep learning
  - Ensemble learning
- Evaluate model performance using **Mean Average Precision (MAP)**.

### 4. Prediction Generation
- Generate personalized product recommendations for each customer at the prediction time.

### 5. Code Optimization
- Enhance computational efficiency to handle large-scale data.
- Implement performance improvements through code optimization techniques.

### 6. Presentation & Insights
- Visualize data findings and model outcomes through charts, tables, and storytelling techniques.
- Provide actionable insights based on analysis and model predictions.

## IV. Data Description
- The dataset includes **1.5 years of customer behavior data** from a banking institution.
- Data spans from **January 28, 2015, to May 28, 2016**, with monthly records of product ownership.
- The goal is to predict additional products a customer may purchase in **May 2016**, excluding those they already owned in **April 2016**.
- Relevant product indicators are stored in columns `ind_(xyz)_ult1`, spanning columns **25 to 48** in the training dataset.

Dataset source: [Kaggle - DataFlow 2025 Product Recommendation](https://www.kaggle.com/datasets/grizmo/dataflow2025-product-recommendation)

