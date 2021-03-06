# Amazon Recommendation System

**Author: Li Yuan and Matthew Flaherty**

**Date: 2022/4/30**

# Visit our fine-tuned Hugging Face Model Card: 

https://huggingface.co/LiYuan/amazon-review-sentiment-analysis

# Introduction

Online shopping has become one of the main sources of shopping and Amazon has led this push of e-commerce. Individuals can go to their website and search for any product and Amazon will give pages of products that are similar to the item searched. Ideally, the product that the individual searched will be at the top of the results. If not, then something similar ought to be near the top. What if there was a way to make this process more efficient? A way in which the individual did not have to get on the website and search. What if they got an email from Amazon recommending products based on previous searches. In this project, we aim to build a recommendation system to make the process more efficient. Our main goal it build a recommendation system to recommend three products for each individual in our dataset. Along the way, we will also explore the data and look at the most purchased product categories as well as the most reviews left by a customer.

# Download Data

Our data comes from a [Kaggle competition](https://www.kaggle.com/datasets/cynthiarempel/amazon-us-customer-reviews-dataset?select=amazon_reviews_us_Baby_v1_00.tsv). We are given features about the individual's feelings about the product as well as the products such as product rating, category, review body, etc. While there are a plethora of product categories, we chose to use a subset of 12 categories. This data covers 20 years of purchases.

# Upload the data into Google Cloud and Google Drive

1. The first step is to upload the 12 dataset (21.78 GB) to Google Cloud drive as following:
![](img/1.png)
2. The second step is transfer all the dataset to Hadoop file system on the Cloud by typing the following code into your cloud terminal
```
hadoop fs -moveFromLocal /home/g593697882/archive hdfs://cluster-bigdata1-m/user/root/archive
```

**Upload all 12 dataset to your Google drive.**

# Run the code on two the platforms

## On Google Cloud

For `01-EDA.ipynb`, `02-recommender-system.ipynb`, `03-cluster-product-title.ipynb`, `04-lsh-product-info.ipynb`, these four python jyputer notebooks should be ran on the **Google Gloud** seperately. In the Google Cloud, we used Pyspark which is installed by the Cloud, we don't need to install any packages by ourselves.

***

## On Google Colab
`05-sentiment-analysis.ipynb` and `06-fine-tune-BERT-on-our-dataset.ipynb` should be ran on the google colab. All the needed packages will be installed once you ran each cell from the beginning because installing codes are included in the beginning.
