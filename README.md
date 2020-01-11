# Predicting-Yelp-User-Rating-using-Spark-ML-library-
We have to write a spark program to predict Yelp user rating based on their review Text. You can download the data files from here: https://uofi.box.com/s/b3hwy8rax1eipmiz2r78csxp06jnodci . Unzip the folder and find review.json and user.json . You can read the description of each file and their attributes here:  https://www.yelp.com/dataset/documentation/main

What you need to do:

1- Data Exploration:
• load the review.json file  and extract “text” and “stars” attributes
• find the distribution of “stars” attributes; that is, find the number of reviews for each star value. 

2- Feature Engineering:
• The star ratings 1,2,and 3 typically indicate dissatisfactionand the star rating 4,5 shows satisfaction. Create a new column “rating” with values 0 (if the star rating is 1,2, or 3) and 2 (if the star rating is 4 or 5).  This will be the target variable you want to predict.  
• Find the distribution of the “rating” column; that is, find the count of reviews for each rating value. Is the rating attribute balanced? If not, you should down sample your data. That means, keep the rating value with the lowest count but take a sample of the reviews for each of the other two rating values in order to have a balanced distribution among all categories. This is called stratified sampling.
• Multiply all fractions by 0.1 to get a sample of only 10% of reviews in each rating category after down-sampling. 
• Extract TFIDF vectors from the review Text

3- Building Machine Learning pipelines.
• Use three different classification models (Logistic Regression, Random Forest and Gradient Boosted classification Trees  to predict the ratings based on the TFIDF vector of the review text.  Use CrossValidation  with three folds to evaluate and tune each model’s hyper-parameter.
• Create a separate pipeline for each ML model. 

4- Adding more Features  
• find the correlation between average_stars and rating columns. You can use stat.corr(col1,col2) 



The solution is provided in the Spark Notebook with the extension ipynb.
