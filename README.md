# Twitter_Sentiment_Analysis

We did the twitter sentiment analysis, which is a well known problem that tries to predict the underlying sentiment of a statement (a tweet in our case).

There are many combinations of algorithms and tokenizers out there to solve this problem and we  
deided to test them all out and compare their training times and accuracies.

We tried the TF_IDF, Bag of words, Word2Vec, Doc2Vec and BERT tokenizers and applied the Logistic Regression, SVM and Random forrest classifiers.

Later we also create a BERT classifier using the bert vectorizing model, which gave the best accuracies when combined with the bert tokenizer.

We also tried running the algorithm for different scales of the input. (100 to 1M Tweets)

#### How to run the code:

We just have a single jupyter notebook file, Twitter_sentiment_analysis.ipynb. You can just run the notebook in order. Make sure you change the path to the input csv file which contains the tweets. Also, install the required libraries to run the code. (All the libraries are imported in the first cell).

We have used the Sentiment140 dataset, which consists of 1.6 M tweets. 
This is the link to the dataset: http://help.sentiment140.com/for-students

#### Code Structure:

First we preprocess the data, by removing unnecssary columns, and then clean the tweets by removing twitter handles, punctuations, numbers and short words. Then we apply the porter stemmer, which removes the morphological endings of english words.

Then we create a classifier function, which defines the different classifiers. When we pass data into the function, the models get trained and we get the accuracies and times.

Later we tokenize the input by selecting each tokenizer and then apply the classifier function to report the accuracy metrics. 

Finally, we define a bert classifier, that takes bert tokens as inputs and we train the model, and later use for predicting tweet sentiment.


## Results:

### Trainig times,accuracies,f1_scores for different ML algorithms and Tokenizers
![plot](https://github.com/prakyath-04/Twitter_Sentiment_Analysis/blob/main/Result3.png)

###  Trainig times,accuracies,f1_scores for Bert classifier at different input scales
![plot](https://github.com/prakyath-04/Twitter_Sentiment_Analysis/blob/main/Result2.png)

###  Tokenizing times for different tokenizers at different input scales
![plot](https://github.com/prakyath-04/Twitter_Sentiment_Analysis/blob/main/Result1.png)
