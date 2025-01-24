# Project: Memory Management Chatbot

The objective of this project was to analyze and enhance a ChatBot program capable of discussing C++-related topics based on a predefined knowledge base. The program was optimized with a focus on memory management, implementing the following improvements:

* Utilization of smart pointers
* Implementation of move semantics
* Ensuring exclusive ownership and proper memory allocation
* Expansion of the knowledge base to include flow control topics
* Enhancement of artwork

![chatbot](https://github.com/1Px-Vision/NLP_DL/blob/main/Project%3A%20Memory%20Management%20Chatbot/CuriosityDemo.gif)

The ChatBot program facilitates a dialogue where users can ask questions about various aspects of memory management in C++. Upon loading its knowledge base from a text file, the chatbot constructs a knowledge graph representation in computer memory. In this graph, chatbot responses serve as nodes, while user queries act as edges. When a user submits a query, the Levenshtein distance algorithm determines the most probable response. The existing implementation is fully functional but relies on raw pointers for representing the knowledge graph and managing object interconnections. While the program executes as intended, it does not incorporate advanced memory management techniques discussed in this course. Specifically, it lacks smart pointers, move semantics, and a structured approach to ownership and memory allocation.

## Project Task Details
Currently, the program crashes when you close the window. There is a small bug hidden somewhere, which has something to do with improper memory management. So your first warm-up task will be to find this bug and remove it. This should familiarize you with the code and set you up for the rest of the upcoming tasks. Have fun debugging!

Aside from the bug mentioned above, there are five additional major student tasks in the Memory Management chatbot project, which are:

