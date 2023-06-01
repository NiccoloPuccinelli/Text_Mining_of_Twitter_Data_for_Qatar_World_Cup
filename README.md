# Text Mining of Twitter Data for Qatar World Cup

Together with my colleagues **Lorenzo Bruni** and **Simone Farallo**, we applied various text mining techniques to thousands of Tweets collected during the World Cup in Qatar in December 2022.

First of all, we acquired the tweets by scraping, and then carried out in-depth pre-processing based on the different techniques used.

We therefore explored the different views about the event by applying different text clustering and text summarization methodologies.

In particular, these two tasks were performed on 3 different embeddings, obtained through **TF-IDF**, **Doc2Vec** and **BERTweet**. For text clustering we compared **K-Means** and **hierarchical clustering**, while for summarization we conducted an analysis based on abstractive (**T5** and **BART**) and extractive (**LexRank** and **TextRank**) approaches. 

The combinations of embeddings and models were finally evaluated according to specific metrics.

The dataset is contained in `Tweets.zip`, where you can find the raw tweets, the pre-processed tweets and a list of the most popular hashtags. 

**Python** language.

## How-to guidelines

* The project is composed by 5 .ipynb files (each of which containing the code for, respectively, acquisition, exploration, preprocessing, clustering and summarization) and 3 .csv files (tweets.csv for the raw data, preprocessed.csv for the preprocessed data and hashtags.csv contains the ordered list of the most popular hashtags).

* The project was entirely developed with Google Colab Pro, except for the acquisition part (Acquisition.ipynb), which has been developed locally.

* Each model computation contains, within its output, the output obtained and the computation time expressed in seconds.

* The files (such as the dataset) were accessed through drives mounted on the Colab environment. Therefore, it may be necessary to configure the paths.

* Each .ipynb file contains the code related to the installation of packages and libraries for the execution on Colab.

* We provided, for each .ipynb file, several comments in order to improve the readability of the code and the results.


**1. Acquisition.ipynb**

The code cell containing the scraping must be run locally (we used Spyder), as the snscrape.modules.twitter scraping library is not supported by Colab.


**2. Preprocessing.ipynb**

This code can be run entirely sequentially, paying attention to the last subsection that overwrites the file "preprocessed.csv", which contains the preprocessed tweets.


**3. Exploration.ipynb**

This code can be run entirely sequentially.


**4. Clustering.ipynb**

Due to RAM limitations, the code was executed 3 times (one for each embedding methodology), each restarting the runtime. The hyperparameter search part for Doc2Vec can be omitted from the computation, as it is very time-consuming and the outputs are visible.

**5. Summarization.ipynb**

The abstractive part can be executed sequentially while, as for the extractive part, we ran the code 4 times (one for each approach) due to RAM limitations, each restarting the runtime.
