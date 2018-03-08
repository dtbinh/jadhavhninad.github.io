---
layout: default
---

Details about my recent projects and repositories that I am currently working on.

## [](#header-2)Neural Network Classifier for MNIST DataSet
[Link to Github Repo](https://github.com/jadhavhninad/Neural-Network-Classifier-for-MNIST-DataSet).

### [](#header-3) Goals:
To implement a two layer neural network for a binary classifier and a multi layer neural network for a multiclass classifier. Compare performance with K-Nearest Neighbour approach for same dataset size.

### [](#header-3) Implementation:
*   The two layer network has 1 hidden layer dimension=500, for binary classification. The multilayer neural network program is able to create and train a multilayer network based on command line arguments. 
*   Two approaches for K-Nearest Neighbour have been tried - using the default python package and building the algorithm from scratch. 
*   Since the MNIST dataset has 60,000 images which is too large for batch gradient descent. Therefore, training is done with 6000 samples and test with 1000 samples.

### [](#header-3) Output:
*   The training and testing accuracies. 
*   Plot of train error vs iterations
*   Plot of K-value vs Error (for kNN)

<br><br>
## [](#header-2)Latent Semantics Based Movie Recommender System
[Link to Github Repo](https://github.com/jadhavhninad/Latent-Semantics-Based-Movie-Recommender-System).

### [](#header-3) Goals:
A movie recommender system that takes user feedback to improve the recommendation. The system is developed using SVD matrix factorization and optimized using ALS method 

### [](#header-3) Implementation:
*   A program which, given all the information available about movies a given user has watched, recommends the user 5 more movies to watch, using SVD.

*   The order in which the movies are watched and the recency is taken into account.

*   The result interface allows the user to provide positive and/or negative feedback for the ranked results returned by the system to enable Task  Relevance feedback.

*   Relevance feedback loop is implemented to improve the accuracy of recommendation. 


### [](#header-3) Output:
*   The system outputs the revisions it suggests.
*   User feedback is taken into account (either by revising the query or by re-ordering the results as appropriate) and a new set of ranked results are returned.

<br><br>
## [](#header-2)Linux Barrier Mechanism for multi threaded program
[Link to Github Repo](https://github.com/jadhavhninad/Linux-Barrier-Mechanism-for-multi-threaded-program).

### [](#header-3) Goals:
To Develop a barrier synchronization mechanism in Linux kernel which can be invoked by user processes via system call interface. The mechanism consists of 3 Linux kernel system calls which are resemble to the pthread barrier i.e barrier-init, barrier-wait, barrier_destroy

### [](#header-3) Implementation:
A barrier synchronization synchronization mechanism was developed in Linux kernel which can be invoked by user processes via system call interface. The mechanism consists of 3 Linux kernel system calls which are resemble to the pthread barrier:

*   barrier_init(unsigned int count, unsigned int *barrier_id, signed int timeout) – to initiate a barrier in the caller’s address space. 

*   barrier_wait(unsigned int barrier_id) – to wait for a barrier synchronization.

*   barrier_destroy(unsigned int barrier_id) – to destroyed the barrier of the id barrier_id.

Since Linux system calls are statically defined and compiled into the kernel, the kernel was rebuilt with new system calls. To demonstrate your barrier implementation, a testing program was developed. The testing program forks two child processes. In each child process, there are 5 threads to exercise the 1 st barrier and additional 20 threads use the 2nd barrier. Each thread sleeps a random amount of time.

### [](#header-3) Output:
*   New Kernal image.

<br><br>
## [](#header-2)Dynamic Instrumentation In Kernel Modules
[Link to Github Repo](https://github.com/jadhavhninad/Kprobes-on-RB-tree-kernel-data-structure).

### [](#header-3) Goals:
Linux has static and dynamic tracing facilities with which callback functions can be invoked when trace points (or probes) are hit. A kernel module was developed that uses kprobe API to add and remove dynamic probes in any kernel programs. With the module’s device file interface, a user program can place a kprobe on a specific line of kernel code, access kernel information and variables.

### [](#header-3) Implementation:

![alt text](https://github.com/jadhavhninad/Kprobes-on-RB-tree-kernel-data-structure/blob/master/kprobes.png "Implementation Schema")


### [](#header-3) Output:
Trace data items to be collected by kprobe handler
*   the address of the kprobe, the pid of the running process that hits the probe, 
*   time stamp (x86 TSC), 
*   rb_object objects traversed in the RB tree while performing the corresponding functions

<br><br>
## [](#header-2)Machine Learning Repository for Different Datasets
[Link to Github Repo](https://github.com/jadhavhninad/ML-for-Different-Datasets).

### [](#header-3) Goals:
To try different Machine Learning algorithms on datasets to get better understanding of their implementation and insights in performance

### [](#header-3) Implementation:
Each Dataset has its own directory which states the different algorithms used and their comparisons.

### [](#header-3) Output:
*   Error plots
*   Behavior for different parameter values

<br><br>

---










