# Project: Machine Translation
In this notebook, any section with a header ending in '(IMPLEMENTATION)' says that the following code blocks will need additional functionality, which you are responsible for providing. Please read the instructions thoroughly!

### Introduction
In this notebook, you will develop a deep neural network that forms a key component of an end-to-end machine translation pipeline. This pipeline will input English text and output its French translation.

### Preprocessing
You will start by converting the text into a sequence of integers.

### Model Creation
You will build models that take these sequences of integers as input and produce a probability distribution over potential translations. After learning about the basic neural network architectures commonly used in machine translation, you can design your model.

### Dataset
We start by examining the dataset that will be used for training and evaluating your pipeline. While the WMT datasets are commonly used for machine translation tasks, they require extensive training time for a neural network. Instead, for this project, we will use a custom dataset with a smaller vocabulary. This will allow you to train your model within a reasonable timeframe.

### Prediction
Finally, you will run the model on English text to generate translations.

## Neural Network Architectures

In this section, you'll explore different neural network architectures, starting with four relatively straightforward models.

* **Model 1:** A basic RNN
* **Model 2:** An RNN with Embedding
* **Model 3:** A Bidirectional RNN
* **Model 4:** An optional Encoder-Decoder RNN
After working with these initial models, you'll move on to build a more complex architecture aimed at surpassing the performance of the previous four.

![RNN_Model](https://github.com/1Px-Vision/NLP_DL/blob/main/Project_2_Machine_Translation/Model_RNN.jpg)

## Included in this repository 

* The code utilized for developing the Machine Translation Project
* Machine_Translation.ipynb - notebook containing the challenge for this project
* Includes Machine_Translation.html, which is an HTML copy of the notebook showing the output from executing all cells
* The data can be found in the directories data/small_vocab_en and data/small_vocab_fr. The small_vocab_en file contains English sentences, while the 
   small_vocab_fr file holds their corresponding French translations. You can load the English and French data from these files by running the cell below.
* project_tests.py and helper.py  files
* This README.md file
