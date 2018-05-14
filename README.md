# The Standard - Python & Data Science Training
## Agenda
### Section 1: Concepts
1. [10] Intros
2. [20] Question Set: Prediction
3. [15] Mechanics of Supervised Learning
4. [30] Brainstorm: Netflix Case
5. [15] Question Set: Models
6. [15] Intro to a model: Neural Network

### Section 2: Hands-on Data Engineering
1. [20] Read Nate Silver article.
2. [10] Data Science Process
3. [10] Python Data Science Tools
4. [10] Getting Acquainted with your Jupyter Notebook
5. [20] Python Warm Up 1: Functions
6. [20] Python Warm Up 2: Documentation
7. [40] Pandas mechanics

### Section 3: Hands-on Supervised Learning
0. [5] Regression vs Classification
1. [10] Question Set:  Lines...
2. [20] Linear Regression Theory
4. [30] Practice: Read in the data & visualize
5. [30] Practice: Predicting housing Prices
6. [30] Exercise: Build a Regression Model On Your Own

### Section 4: Q & A

### Meeting ID
https://zoom.us/j/3848842750

## Intros
1. Let's introduce ourselves
2. Objectives of the class
3. Methodology of the class
4. Software prerequisite: https://www.anaconda.com/download/

## Question Set: Prediction
1. What is a prediction?
2. What is it based on?
3. What makes it good?
4. How do you know it's good?

## Mechanics of Supervised Learning
1. The objective of supervised learning
2. Tagged data, features, target
3. Training set, validation set
4. Build a model and test it
5. Tune and repeat

## Brainstorm: Netflix Case
1. Hypothesize - what data would/could we have access to?
2. What could you predict with this data? 
3. What would be the features? What would be the target?
4. How would this predictor learn and get better?

## Question Set: Models
1. What is input and what is output? 
2. How do they relate to functions?
3. How do they relate to decisions?
4. How do they relate to predictions?
5. What inputs does a predictive function need to take? 
6. What is the output of a predictive function?

## Intro to a model: Neural Network
1. The data - feature and target
2. The perceptron model
3. Online learning

## Reading: Restaurant Grade Analysis
[How Data Made Me A Believer in NYC Restaurant Grades](https://fivethirtyeight.com/features/how-data-made-me-a-believer-in-new-york-citys-restaurant-grades/)

### Questions
1. What is the process?
2. Is this data science? Why or why not?
3. What is data science? When is something data science and when is it not?

## Data Science Process
1. Exploratory Data Analysis
2. Productionizing the data pipeline and model

## Python Data Science Tools
1. Jupyter Notebook
2. Pandas
3. Plotting libraries (plotly, matplotlib, seaborn, etc)
4. Scikit-learn - machine learning
5. Statsmodels - stats library

## Jupyter Notebook
1. Play with the notebook
2. I'll show you the basics of it
3. [Gallery of interesting notebooks](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks)

## Python Warm Up 1: Functions
1. Write a function that takes prints all the even numbers between 1 and 10,000.

## Python Warm Up 2: Documentation
1. Why is this skill set important?
2. Let's use the random library and play with `randint`
3. See the problem below.

```
Given a list of restaurants,
["Wagamama", Chipotle", "Tasty & Alder", "Yummi Cafe", "Shalom Y'all"]

Write a function that takes the list of restaurants, shuffles the list,
and one by one pops out a restaurant as a recommendation.
```

## Pandas Mechanics
[Here](https://s3.amazonaws.com/python-level-2/sales-funnel.csv) is our first data set. 

### Exercise: Investigate
0. Download and open the dataset
1. What is this dataset about?
2. What are some questions you might ask about the data?

### Basic Manipulation
- Let's read in the data.
- How do we see what columns are available?
- How do we look at just the head or tail of the dataset?
- How do we look at only a few rows?
- How do we only look at certain columns?
- How do we pull out a column and look at it as a series?
- How do we look at only those rows that have Status = won

## Exercise
1. How many accounts have a price greater than $12,000?
2. How do we get the maximum value of a certain column?
3. What is the minimum account price? The mean? The sum? The standard deviation?

## Modifying the data
1. What is the total dollar amount pending?

## Boolean masks
1. Demo

## What else can `pandas` do?
1. Operate quickly on big data sets 
2. Transform / clean the data
3. Work easily with time series, categorical or textual data

## (Optional) Exercise
0. Read in this dataset: https://s3.amazonaws.com/simple-fractal-workshops/movie_history_for_user.csv
1. What is the average vote count of movies released in 2014?
2. What is the total number of movies in this dataset that are comedies?
3. What percentage of sci-fi movies are also considered dramas?

## Question Set: Lines...
1. What is a line?
2. What is linear? 
3. What does "line of best fit" mean?

## The Theory of Linear Regression
0. Create plot
1. Hypothesis: linear equation
2. Which pattern fits it the best? Why?
3. Minimizing least squares error
4. R^2
5. Overfitting vs underfitting
6. What do the coefficients of the equation mean?

## Practice: Read in the data & visualize
### The Boston Housing Data Set
- [Here](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/Boston_Housing.csv) is our data set.
- [Here](https://archive.ics.uci.edu/ml/machine-learning-databases/housing/housing.names) is the description of the data.

### Exercise: Pre-Analysis
1. What is the data about?
2. What are columns? (What are the features?)
3. What are we trying to predict? (what is the target?

### Exercise: Prepping for Data Science (Solo)
0. Download and read in the data.
1. Use pandas's built-in descriptive statistics method to get a statistical summary of the data.

### Exercise: Together, we generate a plot
1. Plot CRIM against MEDV using pandas/matplotlib

### Exercise: Generate the rest of the plots
1. Generate the remaining 12 plots (ZN against MEDV, ..., LSTAT against MEV)
2. Which feature looks to be most predictive of MEDV(read: correlated to MEDV)?

## Practice: Predicting housing prices
### Process
0. Let's separate the data into feature and target.
1. Let's separate the feature and target into training and validation set.
2. Let's fit using just 3 feature columns to start with.
3. Let's measure the accuracy.
4. Let's see which columns were most predictive.

### Improvements
1. Let's use cross_val_predict and cross_val_score as shortcuts.

### Exercise 
0. Run the regression using all of the feature columns.
1. How do the results change?

## Practice On Your Own
[Here](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/health_data.csv) is a dataset with the following columns:

- Age
- Years spent receiving their education
- Income divided by 10,000
- Number of visits to the doctor in the previous year
