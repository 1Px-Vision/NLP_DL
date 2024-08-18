# Natural Language Processing (NLP) Projects
This repository contains a collection of Natural Language Processing (NLP) projects, each focusing on a different area of language processing and understanding. Below is an overview of the projects included:

## Projects Overview
### 1. Part of Speech Tagging
#### Description:
This project involves building a Part of Speech (POS) tagger, a fundamental tool in NLP that labels each word in a sentence with its corresponding part of speech (e.g., noun, verb, adjective). The POS tagger is implemented using a Hidden Markov Model (HMM) and trained on a labeled corpus. The model uses unigram and bigram probabilities to estimate the likelihood of tags given words and the sequence of tags in a sentence.

#### Key Features:

* Implementation of HMM for POS tagging
* Evaluation on tagged corpus
* Error analysis and model improvement techniques
* Technologies Used:
  * Python
  * Pomegranate
  * NLTK


### 2. Machine Translation
#### Description:
This project focuses on machine translation, the task of automatically translating text from one language to another. The project involves training a sequence-to-sequence model with attention mechanisms to translate sentences between languages (e.g., English to French). The model is designed to handle varying sentence lengths and capture the context of words in a sentence to improve translation accuracy.

#### Key Features:

* Sequence-to-sequence model with attention
* Handling of variable-length input and output sequences
* BLEU score evaluation for translation quality
* Technologies Used:
  *Python
  * PyTorch
  * NLTK
