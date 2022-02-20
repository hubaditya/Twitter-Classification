# Twitter-Classification
 A sentiment analysis problem to identify the hate tweets by implementing Bag-of-words and TF-IDF algorithm on tokenized and stemmed tweets.
 
 ### Motivation
 There is a lot of social media buzz that happens in an instant. That buzz can be either for a positive change or could reflect the criticism that the public is supposed to feel. Nevertheless, any social post should not be a hate post or spread negative criticism. While this is not entirely in the hands of the people running the social media, there can be however ways in which such posts can be dealt.
 This project aims to identify such posts in a scalable manner such that necessary action can be taken by the business to curb the negative spread.
 
 ### Problem Statement
 Identify if a tweet is a hate tweet
 
 ### Dataset
 The data was downloaded from Twitter API and contains the following structure
 
| Column            | Description                | Data Type |
|:---               |:---                        |:----------|
| id               | row number                 | Integer   |
| label               | whether the tweet is a hate tweet or not  | Integer  |
| tweet       | the tweet that a user posted | String  | 

### Technical Details

#### Libraries
* pandas and numpy - for data wrangling and mathematical operations
* matplotlib and seaborn - for rich data visualizations
* string and re - for data cleaning
* nltk - for information extraction
* sklearn - for train-test split, count and tfidf vectorizers, logistic regression and evaluating performance metrics

#### Data Cleaning
* removing twitter handle, special characters, numbers, punctuations and short words
* tokenizing and stemming the tweets

#### Data Visualization
* creating a word cloud of the tokenized words to visualize the most common words
* visualized the top words used in hate tweets
* top hashtags used in positive and hate tweets

#### Modeling
* Bag-of-words
  * created a count vectorized matrix with a maximum of 1000 features
  * trained a logistic regression model on 70% of the data
* TF-IDF
  * created a tf-idf vectorized matrix with a maximum of 1000 features
  * trained a logistic regression model on 70% of the data
 
#### Evaluation
Since this was an imbalanced classification, F1 score was used as the evaluation metric
* Bag-of-words
  * F1 score of 53%
* TF-IDF
  * F1 score of 54%

#### Result
Output 1 if it is hate tweet or 0 otherwise based on the tweet as an input


