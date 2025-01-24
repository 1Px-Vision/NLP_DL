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

### Task 1 : Exclusive Ownership 1

In file ````chatgui.h / chatgui.cpp````, make _chatLogic an exclusive resource to class ChatbotPanelDialog using an appropriate smart pointer. Where required, make changes to the code such that data structures and function parameters reflect the new structure.

### Task 2 : The Rule Of Five

In file ````chatbot.h / chatbot.cpp````, make changes to the class ChatBot such that it complies with the Rule of Five. Make sure to properly allocate / deallocate memory resources on the heap and also copy member data where it makes sense to you. In each of the methods (e.g. the copy constructor), print a string of the type "ChatBot Copy Constructor" to the console so that you can see which method is called in later examples.

### Task 3 : Exclusive Ownership 2

In file ````chatlogic.h / chatlogic.cpp````, adapt the vector _nodes in a way that the instances of GraphNodes to which the vector elements refer are exclusively owned by the class ChatLogic. Use an appropriate type of smart pointer to achieve this. Where required, make changes to the code such that data structures and function parameters reflect the changes. When passing the GraphNode instances to functions, make sure to not transfer ownership and try to contain the changes to class ChatLogic where possible.

### Task 4 : Moving Smart Pointers

In files ````chatlogic.h / chatlogic.cpp```` and ````graphnode.h / graphnode.cpp```` change the ownership of all instances of ````GraphEdge```` in a way such that each instance of GraphNode exclusively owns the outgoing GraphEdges and holds non-owning references to incoming ````GraphEdges````. Use appropriate smart pointers and where required, make changes to the code such that data structures and function parameters reflect the changes. When transferring ownership from class ChatLogic, where all instances of GraphEdge are created, into instances of GraphNode, make sure to use move semantics.

### Task 5 : Moving the ChatBot

In file ````chatlogic.cpp````, create a local ChatBot instance on the stack at the bottom of the function ````LoadAnswerGraphFromFile````. Then, use move semantics to pass the ChatBot instance into the root node. Make sure that ChatLogic has no ownership relation to the ChatBot instance and thus is no longer responsible for memory allocation and deallocation. Note that the member _chatBot of ChatLogic remains so it can be used as a communication handle between GUI and ChatBot instance. Make all required changes in files ````chatlogic.h / chatlogic.cpp```` and ````graphnode.h / graphnode.cpp````. When the program is executed, messages on which part of the Rule of Five components of ChatBot is called should be printed to the console. When sending a query to the ChatBot, the output should look like the following:

````
ChatBot Constructor
ChatBot Move Constructor
ChatBot Move Assignment Operator
ChatBot Destructor
ChatBot Destructor 
````
