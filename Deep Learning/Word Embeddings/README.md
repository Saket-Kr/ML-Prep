Wikipedia defines word embedding as the collective name for a set of language modeling and feature learning techniques in natural language processing (NLP) where words or phrases from the vocabulary are mapped to vectors of real numbers. 

Word embeddings are a way to transform words in text to numerical vectors so that they can be analyzed by standard machine learning algorithms that require vectors as numerical input.

Two specific forms of word-embeddings:
  - GloVe
  - word2vec  
  
**Word2Vec** - The two architectures for word2vec are as follows:
  - Continuous Bag Of Words (CBOW) - model predicts the current word given a window of surrounding words. In addition, the order of the context words does not influence the prediction (that is, the bag of words assumption).
  - Skip-gram - model predicts the surrounding words given the center word.  
  
CBOW is faster but skip-gram does a better job at predicting infrequent words.
