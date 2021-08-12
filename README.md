# Sentiment-analysis
*Implementing sentiment analysis from scratch without any external libraries and self-trained word vectors*

This project was completed in partial requirement of the course SEL TOPICS FROM COMP SC (CS F441) offered during First Semester 2021-21 at BITS Pilani, Pilani Campus.

The aim of this project is to understand word embeddings and sentiment analysis which form the basis of many standard NLP downstream tasks. The condition was that no external library was to be used except for generating visualizations.

The project was divided into 2 stages.

### Stage 1
This stage was concerned with extracting embeddings for the task of sentiment analysis. We were asked to choose a dataset of our choice and extract word embeddings from the same. For the sake of this project, I chose the publicly available Reuters Corpus from nltk. Only a subset of the corpus was used for training the emebeddings owing to time and computational constraints. 
This was followed by data preprocessing which consisted of the the following tasks in order:
1. Alphabetization
2. Tokenization
3. Lower casing
4. Stop words removal, and
5. Lemmatization

3 popular word embedding algorithms were implemented using Python and Numpy only to extract the embeddings and their performance was subjectively compared in stage 1. The implementations include:

- Continuous Bag of Words Model (CBOW)
- Skip-Gram Model (SG)
- Skip-Gram with Negative Sampling (SGNS)

A simple neural network was used for each implementation. In CBOW and Skip-gram, the activation function used was softmax whereas in Skip-gram with Negative Sampling, the activation function used was sigmoid.

Syntactic and semantic analogies were also computed for select word examples.

Please refer to the [report](https://github.com/Vitthal98/Sentiment-analysis/blob/master/stage%201/Vitthal_2017A7PS0136P_report.pdf) for a detailed, complete review of the methods, dataset, architecture, results and discussion.

### Stage 2
This stage was concerned with creating a sentiment analysis model on a Movies Review Dataset. The task was to predict the sentiment on a scale of 1 to 5 for each provided movie review.

Data preprocessing was employed just as in stage 1. Each movie review phrase was truncated, tokenized and fed to a simple neural network.The dataset was handled for skewness. Cross entropy loss was used along with softmax activation.

Based on performance from stage 1, CBOW vectors were chosen and their accuracy was measured against much better performing GLoVe vectors. Overfitting was overcome by applying L2 regularization to the model. 

The validation accuracy for sentiment analysis can be further improved by:
- training word vectors on a larger corpus
- implementing an RNN/GRU/LSTM instead of a regular neural network.
- exploring other regularization techniques

Kindly refer to the [report](https://github.com/Vitthal98/Sentiment-analysis/blob/master/stage%202/Vitthal_Bhandari_2017A7PS0136P_report.pdf) of stage 2 for a much more comprehensive review.
