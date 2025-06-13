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

4.Model Building

Used K-Nearest Neighbors (KNN) with cosine similarity.

Model recommends items based on similarity between users and items.

5.Evaluation

Used precision-based inspection for relevance of top-N recommendations.

Insights into model limitations due to cold-start problems and sparse interactions.

