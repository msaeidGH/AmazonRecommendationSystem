# AmazonRecommendationSystem

# Context:

Today, information is growing exponentially with volume, velocity and variety throughout the globe. This has lead to information overload, and too many choices for the consumer of any business. It represents a real dilemma for these consumers and they often turn to denial. Recommender Systems are one of the best tools that help recommending products to consumers while they are browsing online. Providing personalized recommendations which is most relevant for the user is what's most likely to keep them engaged and help business.

E-commerce websites like Amazon, Walmart, Target and Etsy use different recommendation models to provide personalized suggestions to different users. These companies spend millions of dollars to come up with algorithmic techniques that can provide personalized recommendations to their users.

Amazon, for example, is well-known for its accurate selection of recommendations in its online site. Amazon's recommendation system is capable of intelligently analyzing and predicting customers' shopping preferences in order to offer them a list of recommended products. Amazon's recommendation algorithm is therefore a key element in using AI to improve the personalization of its website. For example, one of the baseline recommendation models that Amazon uses is item-to-item collaborative filtering, which scales to massive data sets and produces high-quality recommendations in real-time.

# Objective:

We want to build a recommendation system to recommend products to customers based on their previous ratings for other products. You have a collection of labeled data of Amazon reviews of products. The goal is to extract meaningful insights from the data and build a recommendation system that helps in recommending products to online consumers.

# Dataset:

The Amazon dataset contains the following attributes:

- userId: Every user identified with a unique id
- productId: Every product identified with a unique id
- Rating: The rating of the corresponding product by the corresponding user
- timestamp: Time of the rating. We will not use this column to solve the current problem



# Conclusion and Recommendations

- In this case study, we built recommendation systems using four different algorithms. They are as follows:
  - Rank-based using averages
  - User-user similarity-based collaborative filtering
  - Item-item similarity-based collaborative filtering
  - Model-based (matrix factorization) collaborative filtering

- To demonstrate "user-user similarity-based collaborative filtering", "item-item similarity-based collaborative filtering", and "model-based (matrix factorization) collaborative filtering", surprise library has been used. For these algorithms, grid search cross-validation is used to find the optimal hyperparameters for the data, and improve the performance of the model**.
- For performance evaluation of these models, precision@k and recall@k are used. Using these two metrics, the F_1 score is calculated for each working model.

- Collaborative Filtering searches for neighbors based on similarity of items (example) preferences and recommend items that those neighbors rate while Matrix factorization works by decomposing the user-item matrix into the product of two lower dimensionality rectangular matrices.

  - User-User Similarity-based Algorithm:
      - RMSE: 1.0250
      - Precision: 0.86
      - Recall: 0.783
      - F1 score: 0.82
    
  - Optimized User-User Similarity-based Algorithm:
      - RMSE: 0.9633
      - Precision: 0.857
      - Recall: 0.806
      - F1 score: 0.831

  - Item-Item Similarity-based Algorithm:
      - RMSE: 1.0232
      - Precision: 0.835
      - Recall: 0.758
      - F1 score: 0.795

  - Optimized Item-Item Similarity-based Algorithm:
      - RMSE: 0.9681
      - Precision: 0.836
      - Recall: 0.8
      - F1 score: 0.818

  - Matrix Factorization model-based Algorithm:
      - RMSE: 0.8989
      - Precision: 0.86
      - Recall: 0.797
      - F1 score: 0.827

  - Optimized Matrix Factorization model-based Algorithm:
      - RMSE: 0.8908
      - Precision: 0.862
      - Recall: 0.801
      - F1 score: 0.83

- RMSE (Root Mean Square Error): Lower is better, indicating better accuracy.

- The Optimized Matrix Factorization model-based Algorithm has the lowest RMSE, indicating the best accuracy among the models.

- Precision, Recall, and F1 Score:

 -  The Optimized Matrix Factorization model-based Algorithm and the Optimized User-User Similarity-based Algorithm generally perform the best across all three metrics. They strike a good balance between precision and recall, as reflected in their higher F1 scores.

 -  Optimized Matrix Factorization model-based Algorithm slightly outperforms the other models in terms of accuracy and balance between precision and recall.

 -  Tuning hyperparameters significantly improved the performance of both User-User and Item-Item KNN algorithms, particularly in recall, RMSE and F1 score metrics.


# Recommendation:

  - Based on the results and analysis, I recommend using the Optimized Matrix Factorization model-based Algorithm for the recommendation system. It offers the best balance between accuracy (low RMSE) and effectiveness in predicting user preferences (high precision, recall, and F1 score).

  - Based on F1 score alone, the Optimized Matrix Factorization model-based Algorithm comes out on top, followed closely by the Optimized User-User Similarity-based Algorithm. These two algorithms exhibit the best balance between precision and recall, making them strong choices for recommendation systems where both accuracy and relevance of recommendations are crucial.

  - We can try to further improve the performance of these models using hyperparameter tuning.

  - We can also try to combine different recommendation techniques to build a more complex model like hybrid recommendation systems.

  - It's recommended to consider predictions with a larger 'actual_k' value, as they indicate a more comprehensive analysis and are likely to be more accurate in predicting user preferences.

  - Continuously refining the recommendation system's algorithms and data analysis techniques to increase the neighborhood size and improve prediction accuracy could lead to better user experiences and recommendations.

  - It is also recommended to continue exploring hyperparameter tuning and possibly experimenting with different algorithms or ensemble methods to further enhance the recommendation system's performance. Additionally, conducting A/B testing with real users to validate the improvements and gather feedback would be beneficial in fine-tuning the system for optimal user satisfaction.

    It's recommended to continue monitoring and refining the tuned algorithm to ensure its effectiveness in making accurate predictions and improving user satisfaction.

