# Project: Memory Management Chatbot

The objective of this project was to analyze and enhance a ChatBot program capable of discussing C++-related topics based on a predefined knowledge base. The program was optimized with a focus on memory management, implementing the following improvements:

* Utilization of smart pointers
* Implementation of move semantics
* Ensuring exclusive ownership and proper memory allocation
* Expansion of the knowledge base to include flow control topics
* Enhancement of artwork

![chatbot](https://github.com/1Px-Vision/NLP_DL/blob/main/Project%3A%20Memory%20Management%20Chatbot/CuriosityDemo.gif)

The ChatBot program facilitates a dialogue where users can ask questions about various aspects of memory management in C++. Upon loading its knowledge base from a text file, the chatbot constructs a knowledge graph representation in computer memory. In this graph, chatbot responses serve as nodes, while user queries act as edges. When a user submits a query, the Levenshtein distance algorithm determines the most probable response. The existing implementation is fully functional but relies on raw pointers for representing the knowledge graph and managing object interconnections. While the program executes as intended, it does not incorporate advanced memory management techniques discussed in this course. Specifically, it lacks smart pointers, move semantics, and a structured approach to ownership and memory allocation.
