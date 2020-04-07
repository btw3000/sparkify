# Sparkify Big Data Project
This is a blog post describing some aspects of big data analysis using Pyspark and AWS. This is the code block to replicate the findings. Read the blog here: https://medium.com/@yashkumar_73975/my-first-big-data-project-using-aws-90cd51812d6b

The auxiliary data can be accessed through the S3 storage link given inside the notebook. The main dataset is a 12 GB dataset containing entries of users visiting music pages in Sparkify, a fictional music app.

# Packages required
1. pyspark
2. pandas
3. matplotlib
4. collections
5. string
6. numpy

# Motivation
The idea behind this project is to understand how to conduct more Big Data analysis, understand how AWS works, use Pyspark and conduct data visualization and machine learning. The idea is to do it with a hands-on approach. The major questions I gained to seek an understanding about were:

1) Which are the most important factors in deciding the churn rate?
2) What is the click-through rate for the individual pages of ?
3) Can we develop a model which predicts users who will leave the app soon, so that we can provide them promotional offers to get them to stay? 

# Repository files
1. Sparkify.ipynb: This is the smaller dataset. If you want, you can try to use the dataset, and see how the code can be replicated on a small scale
2. pyspark-sparkify.ipynb: This is the main notebook. It contains all the exploratory analysis, data wrangling and machine learning analysis.

# Dataset
The dataset has around 4.6 million records, after cleaning null records. There are 18 attributes in every record. 

1. artist: string (nullable = true) - name of the artist, if a music page is visited
2. auth: string (nullable = true) - whether the user is logged in or not
3. firstName: string (nullable = true) - first name of the user
4. gender: string (nullable = true) - gender of the user
5. itemInSession: long (nullable = true) - item number
6. lastName: string (nullable = true) - last name of the user
7. length: double (nullable = true) - length of the songs in seconds
8. level: string (nullable = true) - paid or free subscription
9. location: string (nullable = true) - city and state where the song was heard
10. method: string (nullable = true) - HTML data (PUT, GET etc.)
11. page: string (nullable = true) - which page is being visited by the user
12. registration: long (nullable = true) - unique id for each user
13. sessionId: long (nullable = true) - unique id for each session
14. song: string (nullable = true) - song name being played (if on song page)
15. status: long (nullable = true) - unique codes for status of each user
16. ts: long (nullable = true) - timestamp of visiting page
17. userAgent: string (nullable = true) - data for the device and OS being used


# Acknowledgements
I thank Udacity for the datasets, and Alazar Kessela, for his mentoring on this project. Any feedback on the project is greatly appreciated.
