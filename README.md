## Recommendation_system

# Motivation

1.Primary motivation for this project was to understand how recommendation systems work and are built.
2.It was also intended to derive some business insights from the data at hand (yelp dataset) and make use of visualization techniques for conveying   those insights.

# Problem at hand

Through this project,I am looking at making restaurant recommendations to users in the dataset. At present, I am making use of Neural Collaborative Filtering technique for this task.

I will be adding more algorithms for solving the same task.


# Approach

1. Reading the data, exploring data and preprocessing

Through the above step, I was able to understand the context of the problem. The data is from metropolitan areas centered on Montreal, Calgary, Toronto, Pittsburgh, Charlotte, Urbana-Champaign, Phoenix, Las Vegas, Madison, and Cleveland, are included in the dataset.

I could also find out about the missing values in the dataset. Understanding the context was important in filling null values.

Some unnecessary columns were also dropped which were essentially conveying the same information. For example, addresses of businesses were dropped because we had latitude and longitude information available.


2 Exploratory data analysis

This step gave some business insight as in the restaurants which are have the highest average rating, regions with most businesses, out of all businesses, which business was the most common.

Businesses could further analyze this information for making optimising resources.

3. Implementing Algorithms

  3.1 Neural Collaborative Filtering algorithm
  
  
  In this algorithm, I have created user_id and restaurant_id embeddings after label encoding them as the first step.
  
  Next step, we take the dot product of user embedding and restaurant embedding.
  
  We pass the output through sigmoid layer and then we normalize the rating values.
  
  We use Adam optimizer and mean_squared_error as our loss function.
  
  Here: point wise loss is calculated, we compare the actual rating in the training set and that calculated by our model and try to minimize the mse loss.
  
  
4. Recommendation:

We take the restaurant embeddings and normalize them.

For finding restaurants similar to a particular restaurant, we take dot product of this restaurant's normalised embeddings with other embeddings and find the values which are higher.

# Future work

I aim to add more algorithms for building recommendation system and will be trying to increase the complexity of NCF model.


# References

This attempt would not have been possible without the following articles and posts:

1. https://towardsdatascience.com/neural-collaborative-filtering-96cef1009401
2. https://www.kaggle.com/code/aryansakhala/recommend
3. https://towardsdatascience.com/paper-review-neural-collaborative-filtering-explanation-implementation-ea3e031b7f96 
  
  

  









