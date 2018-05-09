---
layout: default
---

[Home](index.md)

## [](#header-1)Business Improvement Recommender System
[Link to Github Repo](https://github.com/jadhavhninad/Business_Improvement_Recommender_System).

### [](#header-3) Goals: 
*   In this project we provide a faster approach that combines different machine learning techniques to extract most frequently discussed negative topics/keywords that will provide business with insights regarding what they should be doing right based on what they are currently doing wrong. 
*   We use sentiment analysis to extract features from negative reviews to get higher business specific accuracy.

### [](#header-3) Implementation:
*   Using Neural Networks (LSTM, CNN) and SVM, a _Sentiment Analysis_ module was developed to separate positve and negative yelp reviews for a specific business
*   Topic modelling done on the negative reviews to extract latent topics using _Latent Dirichlet Allocation_
*   Extracted the most common keywords among the topics and re-iterated the topic modelling for those keyword specific texts in the negative reviews to filter out false positives.
*   Top 5 Final recommendations were given to business ordered by the most negative aspect that needs improvement 
*   The program was scaled up to handle multiple outlets for a specific business eg: _Starbucks_
*   All backend data handling tasks leverage MongoDB for storing intermediate and data.

!["Implementation Schema"]({{ site.url }}/assets/images/FlowDiagram.png)


### [](#header-3) Output:
*   A list of features/keywords that reflect the business aspects which need improvement.

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










