Different operations for cleaning and operating on textual features:
https://www.analyticsvidhya.com/blog/2018/02/the-different-methods-deal-text-data-predictive-python/


Any input sentence for a classification task will go through the following steps before being fed into the BERT model.

1) Tokenization: breaking down of the sentence into tokens
2) Adding the [CLS] token at the beginning of the sentence
3) Adding the [SEP] token at the end of the sentence
4) Padding the sentence with [PAD] tokens so that the total length equals to the maximum length (All Sentences are of fixed
   length)
5) Converting each token into their corresponding IDs in the model (out-of-vocabulary (OOV) tokens not appearing in the 
   original vocabulary are replaced with special token [UNK])
   BERT makes use of a WordPiece algorithm that breaks a word into several subwords, such that commonly seen subwords can 
   also be represented by the model. 
