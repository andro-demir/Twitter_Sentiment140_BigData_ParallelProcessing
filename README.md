# Opinion Mining and Sentiment Analysis Classification using Twitter Sentiment140 Dataset 

We implement two classiﬁers based on a logistic regression model to decide whether the sentiment in a tweet is positive or negative. The methods applied in this paper constitute of (i) converting the textual data to a numeric form using Term Frequency (TF) hashing to generate feature vectors and Inverse Document Frequency (IDF) to scale the feature vector to reduce the weights of words that appear often in tweets and not affect the sentiment classiﬁcation (ii) tokenizing the textual data into consecutive sequences of words, called n-grams, and then ﬁtting the features (extracted and scaled the same way as described in (i) and then assembled together) from the unigrams, bigrams and trigrams into a logistic regression model. We compare the computational performance and accuracy on validation and test sets for each method.

We worked with Spark’s Dataframe as data structure in this project and used PySpark MLlib’s Pipeline which is an abstraction speciﬁed as a sequence of stages. These stages are run in order and the input DataFrame is transformed as it passes through each stage: tokenizing, extracting feature vectors by HashingTF, and scaling feature vectors by the TFIDF scores. For classsification of the tweet sentiment, we fit the scaled features in a logistic regression model at the end.
