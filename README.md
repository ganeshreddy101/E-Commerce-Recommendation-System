# E-Commerce-Recommendation-System
A Machine Learning-based recommendation engine developed for an e-commerce platform. The system suggests relevant products to users based on their purchase history and behavioral data, aiming to enhance user experience and increase sales conversions.

Dataset Overview:

~ Records: 7.8 million user-product interactions

~ Users: 4.2 million

~ Products: 476,000

~ Sparsity: 100% (very few users rate very few products)

~ Due to high sparsity, the dataset was filtered to retain only active users and frequently rated products, reducing computation and improving model effectiveness.

Workflow Summary:

1.Data Cleaning

No missing or duplicate values.

Ratings analyzed: Majority are 5-star ratings.

2.User & Product Analysis

Identified most active users and most rated products.

Strategy: Recommend top-rated products to active users for higher conversion.

3.Sparse Matrix Handling

Constructed a User-Product Interaction Matrix.

Filtered users/products with very few ratings to improve matrix quality.

4. Model Evaluation & Accuracy

To predict product ratings and generate personalized recommendations, five regression models were tested and evaluated using Root Mean Squared Error (RMSE):

Model	RMSE

~ LightGBM Regressor: 0.960

~ XGBoost Regressor: 0.968

~ Random Forest Regressor: 0.999

~ Ridge Regression: 0.971

~ Support Vector Regression: 1.132


Best Model: LightGBM with the lowest RMSE, selected for final recommendations.

These models help predict how likely a user is to rate a product highly. The predicted ratings are then used to recommend the Top-N most relevant products to each user.
