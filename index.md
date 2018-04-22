---
layout: default
---

Details about my recent projects and repositories that I am currently working on.

## [](#header-2)Semi Supervised Learning Using Sparse Autoencoder
[Link to Github Repo](https://github.com/jadhavhninad/Sparse_autoencoder).

### [](#header-3) Goals:
*   To implement a sparse autoencoder for MNIST dataset. Plot a mosaic of the first 100 rows for the weight matrices W1 for different sparsities p = [0.01, 0.1, 0.5, 0.8] . 
*   Using the same architecutre, train a model for sparsity = 0.1 using 1000 images from MNIST dataset - 100 for each digit. Retrain the encoder output representation of the data with a softmax layer for the 1000 labeled points. Plug original data, encoding and softmax layers together and fine-tune the model. 
*   Compare performance with a generic neural network of same layers where the weights are initialized randomly for the remaining dataset which is considered to be unlabelled.


### [](#header-3) Implementation:
*   The the architecture and cost function is as follows

!["Implementation Schema"]({{ site.url }}/assets/images/sparseautoencoder_architecture.png)


*   The model is developed using TensorFlow. The weight matrix mosiac for a given sparsity value is as follows

!["Implementation Schema"]({{ site.url }}/assets/images/W1_0.1.png)

*   For semi supervised learning the same tensorflow model was used for initial training. Subsequent implementation of generiac neural network model and training of encoder-softmax & fine-tuning of input-encoder-softmax model was done using keras.

*   Since the already generated weights were requried to be reused during fine-tuning, an custom initializer class was implemented to pass them to the keras neural network layers.

### [](#header-3) Output:
*   Weight matrix and regenerated input mosiacs for different sparsity values 
*   Performance comparison between generic neural network and the fine-tuned model obtained using encoder

<br><br>

## [](#header-2)Formation Control of UAVs with a Fourth-Order Flight Dynamics and Model Predictive Control
[Link to Github Repo](https://github.com/jadhavhninad/Consensus_Based_Flight_Formation).

### [](#header-3) Goals:
To analyze & simulate consensus and leader-follower based formation control for a multi-UAV system with Fourth-Order flight dynamics. Also to Verify the robustness of the proposed algorithm in the paper : **Y. Kuriki and T. Namerikawa: Formation control of UAVs with a fourth-order flight dynamics, SICE Journal of Control, Mea- surement, and System Integration, Vol. 7, No. 2, pp. 74–81, 2014** by modifying different parameter like sampling time, UAV connection structure and weights to state parameters like velocity, position. A more robust approach of using MPC for formation flight was also implemented based on the paper **Y. Kuriki and T. Namerikawa, Formation Control with Collision Avoidance for a Multi-UAV System Using Decentralized MPC and Consensus-Based Control**

### [](#header-3) Implementation:
*   The control law and MPC proposed in the papers were implemented in Matlab. A custom Cost function was developed for MPC using the Matlab MPC toolbox.
*   Effectiveness and Robustness of the alogrithm for different connections among UAVs was tested and an imporvement to the algorithm was proposed and implemented to handle some failure scenarios.
*   UAV Convergence was tested for different sampling time and Beta (weights) values and the results were published in the final report
*   The software implementation was enhanced to scale up the simulation for more UAVs by dynamically generating new positions and desired locations for each UAV added. This simple framework has been opensourced.

!["MPC based formation control"]({{ site.url }}/assets/images/mpc_image.gif)

### [](#header-3) Output:
*   Control law algorithm enhancement
*   Results that depict the robustness of the algorithm
*   Software implementation framework.

<br><br>


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

!["Implementation Schema"]({{ site.url }}/assets/images/kprobes.png)


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










