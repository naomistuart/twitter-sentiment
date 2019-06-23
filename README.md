# twitter-sentiment
This project uses Naive Bayes classification to perform sentiment analysis on the 100 most recent tweets relating to a user-specified keyword.

## Training data set
[Twitter sentiment corpus](https://raw.githubusercontent.com/zfz/twitter_corpus/master/full-corpus.csv) (see also [https://github.com/karanluthra/twitter-sentiment-training])

This dataset, created by Sanders Analytics / Niek J. Sanders, consists of 5513 hand-classified tweets.

## Analysis steps
1. Set up Python wrapper for Twitter API
2. Process tweets in the training set
    - Remove URLs, usernames and hashtag symbols
    - Remove stopwords (e.g. pronouns) and punctuation
    - Tokenize tweets into list of individual words
3. Build model using Naive Bayes classification
    - Build the vocabulary (i.e. all words in training set)
    - Match training tweets against vocabulary and build features vector
    - Train the classifier
4. Test the model
    - Input a search term
    - Fetch most recent 100 tweets relating to the search term
    - Process tweets (as above for training set)
    - Classify sentiment of each tweet
    - Output overall sentiment relating to the topic

## Built with
- [Jupyter Notebook](https://jupyter.org/) to run python code and display results
- [python-twitter library](https://python-twitter.readthedocs.io/en/latest/index.html), a Python wrapper around the Twitter API
- [Python re library](https://docs.python.org/3/library/re.html) for regular expression matching
- [Python nltk library](https://www.nltk.org/), a set of text processing tools for classification and tokenization etc.

## References
- [Creating The Twitter Sentiment Analysis Program in Python with Naive Bayes Classification](https://towardsdatascience.com/creating-the-twitter-sentiment-analysis-program-in-python-with-naive-bayes-classification-672e5589a7ed), an article I followed along as a tutorial
-[Rate Limiting of Twitter API](https://developer.twitter.com/en/docs/basics/rate-limiting.html)
