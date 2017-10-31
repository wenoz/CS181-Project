# CS181-Project

# Methods
* The review dataset need to be joined with the business dataset on business_id. The reviews will be grouped by the categories of the given business_id to obtain the labeled dataset for each category existed in the dataset.  30% of dataset are training data, and 70% are testing data.
* The raw data collected from Yelp are the text of the reviews posted by the users, so Term frequency–inverse document frequency will be used to convert the textual information into numerical values to reflect the importance of a term to a document in the corpus. We will use the spark built-in TF/IDF library to compute the word frequency of the reviews. In order to reduce the dimensionality, we need to find an ideal threshold to truncate the words/features with lower frequency, which could require manually examining the features. We might utilize the Stanford CoreNLP software to extract entities from the reviews before the feature vectorization.  
* After modifying our selections of features, several classification machine learning techniques will be applied on our data and results will be compared based on the performance on the testing dataset. The initial model we will try is the Naive Bayes Classifier, as the most popular algorithm used in text-mining. We might try the K-Nearest Neighbor or Decision Tree, depending on the amount of time left after the pre-processing step. 
* A pipeline will be constructed to return possible categories associated with the input review(s).
