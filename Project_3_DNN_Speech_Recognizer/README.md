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
