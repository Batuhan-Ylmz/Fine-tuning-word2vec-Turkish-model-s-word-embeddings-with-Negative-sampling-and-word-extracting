# Fine-Tuning word2vec Turkish models' word embeddings with Negative sampling, word extracting and dimension reduction ( autoencoders )

A Turkish word2vec model proposed by Abdulllatif Koksal (https://github.com/akoksal) using the Gensim library is fine-tuned with negative sampling and word extracting algorithm.

# Downloading the Model

Gensim model proposed by Abdulaltif Koksal can be downloaded from his repository. (trmodel).

# Generating the Dataset and Creating the JSON file for storing the Embeddings of Original Model

Embeddings size of 400 are extracted from the model and saved to a ".json" file. 
".json" file contains the each word trained in the model and their corresponding vector with a size of 400.

# Dimension Reduction from 400 to 40 Using AutoEncoder

Indices of each word is extracted from the .json file and fed into the autoencoder which consists of an "encoder" and "decoder" layers.
Outcome of encoder layer (words embeddings with the size of 400) is used in order to fine-tune the word embeddings of 'trmodel'.

# Fine-tuning the model with negative sampling and word-extracting Algorithm

A new dataset is chosen from the dumps of wikipedia (https://dumps.wikimedia.org/mirrors.html).
Model architecture is created with negative sampling algorithm.
A subsampling algorithm that removes (based on frequency ratio of each word) the words that are considered as outliers is implemented as well. Due to the lack of qualified hardware and limited dataset, subsampling is NOT applied upon the text data. With a higher-level machine and a higher size of data can be chosen and a better performing Turkish word2vec model can be trained using the subsampling algorithm.
