# Text Mining of Twitter Data for Qatar World Cup

Together with my colleagues **Lorenzo Bruni** and **Simone Farallo**, we applied various text mining techniques to thousands of Tweets collected during the World Cup in Qatar in December 2022.

First of all, we acquired the tweets by scraping, and then carried out in-depth pre-processing based on the different techniques used.

We therefore explored the different views about the event by applying different text clustering and text summarisation methodologies.

In particular, these two tasks were performed on 3 different embeddings, obtained through **TF-IDF**, **Doc2Vec** and **BERTweet**. For text clustering we compared **K-Means** and **hierarchical clustering**, while for summarization we conducted an analysis based on abstractive (**T5** and **BART**) and extractive (**LexRank** and **TextRank**) approaches. 

The combinations of embeddings and models were finally evaluated according to specific metrics.

The dataset is contained in `Tweets.zip`, where you can find the raw tweets, the pre-processed tweets and a list of the most popular hashtags.
