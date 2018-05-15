# The Standard - Python & Data Science Training
### Meeting ID
https://zoom.us/j/3848842750

## Day 2 Agenda
### Section 1: kNN & Logistic
0. [5] Classification vs Regression
1. [30] kNN Theory
2. [15] kNN Application - build the model
3. [20] kNN Model Tuning
4. [20] Logistic Regression Theory
5. [15] Apply logistic regression
6. [10] Logistic regression: Play with the parameters
7. [15] Hypothesize & Discuss: kNN vs Logistic Regression

### Section 2: Trees
1. [30] Classification Trees
2. [15] Apply Tree Classifier to Data Set
3. [15] Play with the tree parameters
4. [15] Regression Trees
5. [15] Apply the regression tree to housing dataset
6. [30] Bagging Theory & Application
7. [40] Random Forest Theory & Application
8. [20] Classification Recap

### Section 3: Clustering & PCA
1. [30] Unsupervised Learning Concepts
2. [30] Clustering Theory - kMeans
3. [30] Clustering Applied
4. [15] PCA Concept
5. [15] PCA Applied

### Section 4: Lab

### Section 5: Q & A

## kNN Theory

### How It Works
Explain intuition behind kNN.

### Worksheet
- [kNN Worksheet 1](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/worksheet_1_kNN.pdf)
- [kNN Worksheet 2](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/worksheet_3_kNN.pdf)

### Reflection
1. What are the pros and cons of this model?
2. Where do you think it would be useful?
3. Where do you think it might fail?

Don't worry... you don't need to know these answers yet. Just want you to start becoming critical in this way.

## kNN Application
- [The data set](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/breast-cancer.csv)

### Data prep
1. Read it in
2. Get descriptive stats
3. Separate into feature and target
4. Separate into training and validation sets

### Together
1. Let's run the kNN model on it
2. Let's see an instance of a prediction.
3. Now let's use `cross_val_score` as a shortcut.

## kNN Model Tuning
1. Now try different values of k
2. Create a data frame of accuracy against K (you can do this with a dictionary)
3. Plot the accuracies
4. What did you find?

## Logistic Regression Theory
### Brainstorm for Distinctions
1. What are examples of situations where we want to predict a binary outcome?
2. What are situations where we want to know the **probability** of that outcome?
3. What are situations where we do not care about knowing that probability?

### The Setup of the Model
- linear separability
- features not highly correlated
- binary outcomes

## Logistic Regression Applied
Let's apply it to our breast cancer data set.

## Let's tune Logistic Regression
1. What are the parameters that we can tune?
2. Tune them and see what happens!

## Comparison: kNN vs Logistic
1. When do you think you'd use kNN over Logistic? 
2. When would you use Logistic over kNN?
3. What are the strengths of Logistic?
4. What are the strengths of kNN?

## Trees
### The Set Up
- Assumption of Non-Linearity
- Boolean Logic
- Binary Cuts

### Worksheet
- [Trees Worksheet 1](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Decision+Trees/DT_wksht_2.pdf)
- [Trees Worksheet 2](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Decision+Trees/DT_wksht_3.pdf)

## Apply Tree to Data Set

## Play with Tree Parameters
1. How stable is the model?

## Regression Trees
### The Set Up
- Non-linearity

### Worksheet
- [Regression Tree Cost](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Trees+Continued/trees_continued_wksht_1.pdf)
- [Measuring Variable Importance](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Trees+Continued/trees_continued_wksht_3.pdf)

## Apply Regression Tree
Let's apply it to the Boston Housing data set.

## Bagging
### The Why?
- Why are trees unstable?
- Addresses instability
- Is an ensemble method

### Worksheet
[Bagging](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Decision+Trees/DT_wksht_4.pdf)

### Application
Let's apply it to our breast cancer data set.

## Random Forest
### Question Set
1. What is bias?
2. What is variance?
3. What is flexibility? 

### Bias-Variance
[Short Article](https://elitedatascience.com/bias-variance-tradeoff)

### The Set Up
- Bagging & randomized pruning
- [Intuitive example](https://www.quora.com/How-does-randomization-in-a-random-forest-work/answer/Edwin-Chen-1?share=1&srid=h5QG)
- How do we interpret the random forest model?

### (Optional) Question Set
1. How does Random Forest reduce variance?
2. How does Random Forest reduce bias?
3. Is there always a trade off?

### Let's Apply It
- Let's apply it to our data set.
- classification report

## Classification Recap
1. kNN
2. Logistic
3. Trees
4. Bagging
5. Random Forest

### Intuition Exercise...
Let's split up into groups, each take a model and come up with an intuitive explanation of it, with examples/possible use cases, and pros and cons and share.

### (Optional) Lab
Work with [this dataset](https://s3-us-west-2.amazonaws.com/simplefractal-teaching/cc_default.csv) and build different classifiers, tune them as best you can, and compare the performance.

## Unsupervised Learning Concepts

## Clustering Theory - kMeans
Simplest approach to clustering:
- We are given some data D, consisting of x<sup>(i)</sup>, each of which is a p-dimensional vector.
- Our task is to group the data into K groups. We specify K beforehand.

## An Application
Suppose we have census data and want to do *market segmentation* - subgroup the people from the census in such a way that we can better target advertisements.

## Intuition
Here's the intuition behind K-means clustering:
- There are certain points which are the centers of the clusters
- The points in that cluster are nearer to the center of that cluster than they are to the center of a different cluster.

## Procedure
### Draw the K-means clustering procedure step-by-step on the board.
Assume K clusters, with *unknown* centers c<sub>1</sub>, ..., c<sub>k</sub>, each of which is a p-dimensional vector.

A good measure of how good a cluster is is the sum of squared distances of the points to the center of that cluster. Then we'll sum that over all the clusters to see how good our choice of centers were.

We want to minimize the sum over all the clusters of the sum of square distances of points to the center of the cluster they belong to.

It's difficult to minimize this analytically, so we'll need an algorithm to help us do this.

### The math behind the procedure on the board.
K-means do this iteratively by the following:

1. Initialize the centers c<sub>1</sub>, ..., c<sub>k</sub> to be arbitrary, distinct points from the dataset.
2. Choose the optimal assignment of points to clusters given by the centers above. Call this assignment of points to centers A. We do this by assigning each point to the center nearest to it.
3. Now that the assignment is fixed, choose the optimal centers for that assignment A.
4. Repeat 2 and 3 until convergence, a.k.a. the assignments don't change on subsequent iterations.

### Resources
- [Finding the K in K Means](https://datasciencelab.wordpress.com/2013/12/27/finding-the-k-in-k-means-clustering/)

## Clustering Applied
- Scaling of the data matters
- Let's cluster our breast cancer data feature set

## PCA - Conceptual Intro & Motivation
### The Setup
- PCA is a technique to reduce the dimensionality of our dataset.
- It transforms our feature data matrix into a matrix with fewer columns, keeping as much of the variance as possible.
- Often used for machine vision and NLP, given the high dimensionality and sometimes high correlation between background pixels (machine vision) or ngrams (NLP) for example.
- [Visual Demo](http://setosa.io/ev/principal-component-analysis/)

### Worksheet
- [Math Walkthrough](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/PCA/PCA_worksheet_1.pdf)

## PCA & Clustering Applied - Walk Through
- [The Code](http://nbviewer.jupyter.org/gist/suneel0101/2649ee8bdecbf0c42da5)
- [Another Example](http://nbviewer.jupyter.org/gist/suneel0101/a09857db18eab5c476b9)

## Q & A & Wrap Up

## Resources
- https://elitedatascience.com/machine-learning-algorithms
- http://scott.fortmann-roe.com/docs/BiasVariance.html