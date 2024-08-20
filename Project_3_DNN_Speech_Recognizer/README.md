# Project: Deep Neural Network (DNN) Speech Recognizer

In this notebook, you'll develop a deep neural network to serve as a key component in an end-to-end automatic speech recognition (ASR) pipeline. We’ll start by exploring the LibriSpeech dataset, which will be used to train and evaluate your models. Your Algorithm will initially convert raw audio into feature representations commonly employed in ASR. Next, you'll build neural networks capable of mapping these audio features to transcribed text. After understanding the foundational layers frequently used in deep learning approaches to ASR, you'll experiment with creating and testing your state-of-the-art models. Throughout the notebook, you'll find recommended research papers for further reading and links to GitHub repositories with notable implementations.

## Introduction

In this notebook, you'll develop a deep neural network designed to operate within an end-to-end automatic speech recognition (ASR) pipeline. Upon completion, your pipeline will take raw audio as input and generate a predicted transcription of the spoken language. The overall structure of the pipeline is illustrated in the figure below.

![Figure_P](https://github.com/1Px-Vision/NLP_DL/blob/main/Project_3_DNN_Speech_Recognizer/DDN_Speech.jpg)

* **STEP 1** involves pre-processing, where raw audio is converted into one of two commonly used feature representations for automatic speech recognition (ASR).
* **STEP 2** introduces an acoustic model that takes these audio features as input and outputs a probability distribution across all possible transcriptions. After exploring the fundamental types of neural networks frequently used in acoustic modeling, you will have the opportunity to conduct your experiments and design a custom acoustic model!
* **STEP 3** processes the output from the acoustic model to generate a predicted transcription.

You can use the following links to navigate through the notebook:

* The Data
* **STEP 1:** Acoustic Features for Speech Recognition
* **STEP 2:** Deep Neural Networks for Acoustic Modeling
* **Model 0:** RNN
* **Model 1:** RNN + TimeDistributed Dense
* **Model 2:** CNN + RNN + TimeDistributed Dense
* **Model 3:** Deeper RNN + TimeDistributed Dense
* **Model 4:** Bidirectional RNN + TimeDistributed Dense
* **Models 5+**
* Compare the Models
* Final Model
* **STEP 3:** Obtain Predictions

## The Data

We start by examining the dataset that will be utilized to train and evaluate your pipeline. [LibriSpeech](https://www.danielpovey.com/files/2015_icassp_librispeech.pdf) is an extensive corpus of English-read speech, specifically created for training and assessing models for Automatic Speech Recognition (ASR). The dataset comprises 1,000 hours of speech derived from audiobooks. For this project, we'll work with a smaller subset, as training on the full dataset would require considerable time. However, once you have completed this project, you are encouraged to explore the larger dataset available online if you wish to delve deeper.

## Neural Network Architectures
In this section, you'll explore different neural network architectures

### Model 0: RNN
The first acoustic model you'll be using is an RNN, known for its ability to effectively model sequential data. As illustrated in the figure below, the RNN provided will process the time sequence of audio features as its input.

![Model_0_RNN](https://github.com/1Px-Vision/NLP_DL/blob/main/Project_3_DNN_Speech_Recognizer/Model_0_RNN.jpg)

At each time step, the speaker articulates one of 28 possible characters, which includes the 26 letters of the English alphabet, a space character (" "), and an apostrophe ('). The RNN's output at each time step is a probability vector with 29 entries. Each entry in the vector corresponds to the likelihood of a specific character being spoken at that time. The 29th entry is reserved for an empty "character" used to pad training examples within batches of varying lengths. If you're curious about how characters are mapped to indices in the probability vector, you can check the char_map.py file in the repository. The figure below presents a rolled depiction of the RNN, highlighting the output layer in more detail.

### Model 1: RNN + TimeDistributed Dense

Explore the Keras documentation to understand the TimeDistributed wrapper and the BatchNormalization layer. In this architecture, batch normalization will be incorporated into the recurrent layer to accelerate training. The TimeDistributed layer will be utilized to capture more intricate patterns in the dataset. An unrolled view of the architecture is shown below.

![Model_1_RNN](https://github.com/1Px-Vision/NLP_DL/blob/main/Project_3_DNN_Speech_Recognizer/Model_1_RNN.jpg)

## Included in this repository 

* The code utilized for developing the DDN Speech Recognizer Project
* vui_notebook.ipynb - notebook containing the challenge for this project
* This README.md file
