# Project: Machine Translation
In this notebook, any section with a header ending in '(IMPLEMENTATION)' says that the following code blocks will need additional functionality, which you are responsible for providing. Please read the instructions thoroughly!

### Introduction
In this notebook, you will develop a deep neural network that forms a key component of an end-to-end machine translation pipeline. This pipeline will input English text and output its French translation.

### Preprocessing
You will start by converting the text into a sequence of integers.

### Model Creation
You will build models that take these sequences of integers as input and produce a probability distribution over potential translations. After learning about the basic neural network architectures commonly used in machine translation, you can design your own model.

### Prediction
Finally, you will run the model on English text to generate translations.

## Neural Network Architectures

In this section, you'll explore different neural network architectures, starting with four relatively straightforward models.

* **Model 1:** A basic RNN
* **Model 2:** An RNN with Embedding
* **Model 3:** A Bidirectional RNN
* **Model 4:** An optional Encoder-Decoder RNN
After working with these initial models, you'll move on to build a more complex architecture aimed at surpassing the performance of the previous four.
