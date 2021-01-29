# Sparkify Churn Project

### Table of Contents

1. <a href="#Overview">Overview</a>
2. <a href="#Getting-Started">Getting Started</a>    
    1. <a href="#Prerequisites">Prerequisites </a>
    2. <a href="#Data">Data </a>
3. <a href="#Insights">Insights</a>
5. <a href="#Results">Results </a>
6. <a href="#Author--Acknowledgement"> Author & Acknowledgement</a>

# Overview
Sparkify is a Music platform like <a href="https://fizy.com/">Fizy</a>. Sparkify's most important problem is Churn. Churn defines cancellation of the subscription.

In this case we are going to predict potential churner subscribers. If Sparkify detects the subscriber who will be churner, they can take actions to labeled subscribers like discount, no ads and so on.

The data provided from Sparkify Company has customer logs in the platform. Also the dataset has variables like age, gender, location. First of all we analyzed the dataset and created some features about subscribers. After Feature engineering steps we went to modelling steps and tried some ML alogrithms for predict the potential churner subscribers correctly. In the evaluation step we used F1 Score because the dataset is imbalanced. Accuracy is not a good metric for this problem.

Finally We achieved 0.82 F1 Score with Crossvalidated Random Forest Classifier. Also We prepared an <a href="https://abduygur.medium.com/churn-prediction-using-pyspark-a1f4ef0439b3"> article in the medium </a> about this project

# Getting Started

You can run the codes in the notebook on local computer also you can run the codes on a cluster. I decided IBM Cloud

## Prerequisites
````
- python 3.x
- pyspark
- pandas
- pyspark.ml
- httpagentparser
- matplotlib
- seaborn
````

## Data
The data provided by Udacity. In the course we have 3 types of dataset. Medium size dataset used in this project

# Insights
There are many insights about data in the notebook. 

<img src='./img/Churn Proportion.JPG'>

Nearly 20% churn rate in the sparkify dataset.

<img src='./img/General Data Distiribution.JPG'>

Most of the input data skewed in this case i preferred RandomForest and GBTClassifier. Because they are robust to skewed data. Also no need for scale the data.


# Results

I have evaluate the models with F1 Score. After modeling I chose RandomForeset because F1 Score is higher than the GBTClassifier. AFter hyperparameter tuning steps I achieved 0.79 F1 Score

# Author & Acknowledgement

Thanks the Udacity team for providing this project. I have gained a lot of  knowledge about Big data environments and Spark.

The all codes are written by <a href='https://www.linkedin.com/in/abduygur/'>A. Uygur Yiğit </a>
