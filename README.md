# Suicidal Ideation Detection Using Natural Languange Processing and Machine Learning - Deep Learning Models
This project aims to develop a system that can detect suicidal ideation using Natural Language Processing (NLP) and Machine Learning (ML) models, including Word Embedding Layers Model,Word Embedding + Global Average Pooling Models, Word Embedding + Convolutional Neural Networks (CNN), Word Embedding + Bidirectional Long Short-Term Memory (Bi-LSTM). This project aims to identify individuals who may be at risk of suicide and contribute to suicide prevention efforts.

# Dataset:
I've used the kaggle dataset from this [link](https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch). The dataset is a collection of posts from "SuicideWatch" and "depression" subreddits of the Reddit platform. The posts are collected using Pushshift API. All posts that were made to "SuicideWatch" from Dec 16, 2008(creation) till Jan 2, 2021, were collected while "depression" posts were collected from Jan 1, 2009, to Jan 2, 2021.

# Data Preprocessing
At the preprocessing stage, the lower case process is carried out, filtering text by removing symbols, emoji, numbers, special characters, and any objects other than the alphabet. Then the stopword removal process is carried out using the NLTK library (Natural Language Toolkit). Then stemming is done to change word classes into basic words using NLTK Stemmer.

# Feature Extraction:
Before entering the feature extraction stage the dataset is split into 80% data train and 20% data validation. At the feature extraction stage, the tokenizer process is carried out using Tokenizer() on tensorflow. Furthermore, padding is done to equalize the length of the sequence of each line.

# Deep Learning Models:
Word Embedding Layers Model,Word Embedding + Global Average Pooling Models, Word Embedding + Convolutional Neural Networks (CNN), Word Embedding + Bidirectional Long Short-Term Memory (Bi-LSTM)

# Logs Results

<center>
  
  | No |                              Models                             | Total Params | Trainable Params | Duration per Epoch (Second) | Accuracy (Validation) |                File Name                |
|:--:|:---------------------------------------------------------------:|:------------:|:----------------:|:---------------------------:|:---------------------:|:---------------------------------------:|
|  1 |                Word Embedding Layers (Base Model)               |  20,673,281  |    20,673,281    |            46-51            |   94.09888982772827%  |     Basic Model Embeding Layers.h5      |
|  2 |             Word Embedding + Global Average Pooling             |    195,329   |      195,329     |            31-38            |   93.53872537612915%  | Model Basic + Global Average Pooling.h5 |
|  3 |       Word Embedding + Convolutional Neural Networks (CNN)      |    220,033   |      220,033     |           170-174           |   94.52332258224487%  |       Model Embedding + Conv1D.h5       |
|  4 | Word Embedding + Bidirectional Long Short-Term Memory (Bi-LSTM) |    107,137   |      107,137     |            93-124           |   92.56921410560608%  |      Bidirectional-LSTM-1-Layers.h5     |

  </center>
