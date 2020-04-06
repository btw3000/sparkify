# Sparkify Big Data Project
This is a blog post describing some aspects of big data analysis using Pyspark and AWS. This is the code block to replicate the findings. Read the blog here: 

The auxiliary data can be accessed through the S3 storage link given inside the notebook. The main dataset is a 12 GB dataset containing entries of users visiting music pages in Sparkify, a fictional music app.

# Packages required
1. pyspark
2. pandas
3. matplotlib
4. collections
5. string
6. numpy

# Motivation
The idea behind this project is to understand how to conduct more Big Data analysis, understand how AWS works, use Pyspark and conduct data visualization and machine learning. The idea is to do it with a hands-on approach.

# Repository files
1. Small Dataset: If you want, you can try to use the dataset, and see how the code can be replicated on a small scale
2. pysparkify.ipynb: This is the main notebook. It contains all the exploratory analysis, data wrangling and machine learning analysis.

# CRISP-DM Process
The CRISP-DM process has been utilized in this analysis. The questions are gauged to see how the states differ when it comes to some key factors.

# Business Understanding
The major questions I gained to seek an understanding about were:

1) Which are the most important factors in deciding the churn rate?
2) What is the click-through rate for the individual pages of ?
3) Can we develop a model which predicts users who will leave the app soon, so that we can provide them promotional offers to get them to stay? 

# Data Understanding
The dataset has around 4.6 million records, after cleaning null records. There are 18 attributes in every record. 

 |-- artist: string (nullable = true) - name of the artist, if a music page is visited
 |-- auth: string (nullable = true) - whether the user is logged in or not
 |-- firstName: string (nullable = true) - first name of the user
 |-- gender: string (nullable = true) - gender of the user
 |-- itemInSession: long (nullable = true) - item number
 |-- lastName: string (nullable = true) - last name of the user
 |-- length: double (nullable = true) - length of the songs in seconds
 |-- level: string (nullable = true) - paid or free subscription
 |-- location: string (nullable = true) - city and state where the song was heard
 |-- method: string (nullable = true) - HTML data (PUT, GET etc.)
 |-- page: string (nullable = true) - which page is being visited by the user
 |-- registration: long (nullable = true) - unique id for each user
 |-- sessionId: long (nullable = true) - unique id for each session
 |-- song: string (nullable = true) - song name being played (if on song page)
 |-- status: long (nullable = true) - unique codes for status of each user
 |-- ts: long (nullable = true) - timestamp of visiting page
 |-- userAgent: string (nullable = true) - data for the device and OS being used

# Data Preparation
First of all the null accounts were removed. There is no other data cleaning required.

## Question 1


#### Missing values: There were only 4 missing values, present for the climate zone values. However, these values were reported in the climate zone description values. So, they were co-opted from the description values.

## Question 2


#### Missing values: There were no missing values in this case except household median income. There were only 703 (<1%) empty values out of 72,760 values, which were equally distributed amongst all the states. They were neglected.

## Question 3


#### Missing values: The total energy dataset did not have any missing value. The solar energy dataset had missing values for small-scale solar. However, in many cases, those states had utility-scale solar energy to be very low. It is safe to assume the small-scale residential solar generation would be negligible, especially as a fraction of the total electricity generated. It was considered to be zero.

# Data Modeling

## Question 1

## Question 2

## Question 3

# Results Evaluation
The major results of the analysis are:


# Acknowledgements
I thank Udacity for the datasets, and Alazar Kessela, for his mentoring on this project.
