# ClassifyingAmazonReviews
Capstone Project for US AI Academy - 2nd Semester
![dispositivos-Amazon-1000x600](https://user-images.githubusercontent.com/115184790/230679282-a9425c5d-b25e-4ed9-ba10-263e788d3d25.jpg)

This data set has been downloaded from the Amazon ficial web site at: https://www.kaggle.com/datasets/sid321axn/amazon-alexa-reviews , enter the link and click on "Download". Make shure to add the rute of the folder where you have saved the data. 

# Summary
- Project Proposal
- File to extract data: amazon_alexa.tsv
- Project file: Index.ipynb

## Buisness Understanding
Our main objective is create a true smart home experience by identifying the needs and requirements of our users.
Users opinion are very valuable to us as it allows us to improve the quality of the response of our devices.
Therefore, when analysing reviews, we will find the user's favorite skills as well as the most common problems in certain 
versions or models.
At the same time, we are interested in creating an automatic learning model that allows us to classify whether a review is positive or negative based on its content and keywords, that way we can give immediate attention to those users who are dissatisfied with your product.

## Data Understanding
The data set we used for our research is made up of more than 3,000 user reviews of aleza devices like Echo, Echo Dot, Fire 
Sticks, etc.

## Data Preparation
Before analysing of the data, it's necessary to clean it, this will eliminate information that is not useful, and structure it so that all values of the same type have the same format, either numerical or text, depending on the case.

1) Data Extraction
2) Changing needed date types
3) Analysing numeric data
4) Cleaning and Preprocessing text data
5) Normalizing Words
6) Creating N-Grams

## Modeling
To create the model we must consider: 
    
 - What's the best feature from our data frame? The split is based on the best feature.
 - Which is the best algorithm to start deciding, entropy or ginni index?
 - Best sizes for training and test sets.
 - Best encoder. One hot encoder, vector count, binary count, TF-IDF?
 - Max depth, how many levels will our tree have? 
 - Pruning in case it's necesary
 - Accuracy, scores and interpretation of Confusion Matrix. 

Reviews are choosen as the input feature in the model becuase its content will determine the parameters to predict if a new comment is positive or negative 

I decided to create different modeles each one with different paramaters in order to compare their accuracy and precision to predict if an input is a positive or negative review. 

## Evaluation
Comparing the accuracy of the different models to predict whether a comment is negative or positive is *Model 3*, based on its results on F1 Score, accurracy an recall. 

## Conclusion
Although the model is not very good, it is not the worst. Apparently we have gotten good results in predicting if a review is bad, however it is highly unlikely that this will happen since most of the reviews in this dataset are positive, it would make more sense for the model to identify more accurately a positive comment because it has more samples to learn from them.

This is possible because both positive and negative feedback can include the same words and as they enter the model by themselves, without knowing the context of the sentence it is difficult for the model to identify its sense.

A good way to attack this problem would be introducing to the model sets of words, specifically bi-grams and tri-grams that can give more information to the model.

Surely, by doing it this way you will be able to appreciate a greater difference between positive and negative comments and it would increase the precision with which it predicts a positive comment.

This work will continue on improving this model by changing the model's input from a single word to sets of words. In the same way, these "n-grams" will be used subsequently to create a cluster that can determine the issues most addressed by clients and their favorite skills.
