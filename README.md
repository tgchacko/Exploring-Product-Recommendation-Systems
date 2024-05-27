# Exploring-Product-Recommendation-Systems

## Table of Contents

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Data Description](#data-description)

[Tools](#tools)

[EDA Steps](#eda-steps)

[Data Preprocessing Steps and Inspiration](#data-preprocessing-steps-and-inspiration)

[Graphs](#graphs)

[Recommendation Techniques](#recommendation-techniques)

[Assumptions](#assumptions)

[Evaluation Metrics](#model-evaluation-metrics)

[Results](#results)

[Recommendations](#recommendations)

[Limitations](#limitations)

[Future Possibilities of the Project](#future-possibilities-of-the-project)

[References](#references)

### Project Overview

This project focuses on developing and evaluating various product recommender systems. It aims to enhance user experience by suggesting relevant products and boost customer satisfaction and sales through personalized recommendations.

### Data Sources

The dataset used in this project contains Amazon Electronics product ratings and reviews. The data is sourced from a CSV file: ratings_Electronics.csv.

[Ratings Dataset](https://www.kaggle.com/datasets/saurav9786/amazon-product-reviews/data)

### Data Description

#### Attributes

- user_id: Unique identifier for each user.
- product_id: Unique identifier for each product.
- rating: Rating given by the user to the product.
- timestamp: Time of the rating.

![Data Description[(https://i.postimg.cc/xjgDMBQK/Screenshot-2024-05-27-at-13-01-23-Amazon-Reviews-Jupyter-Notebook.png)

#### Summary

- Total No of Users: 786,330
- No of users having given at least 50 ratings: 38
- Total No of products: 61,894
- No of products having given at least 50 ratings: 3,813

### Tools

- Python: Data Cleaning and Analysis

    [Download Python](https://www.python.org/downloads/)

- Jupyter Notebook: For interactive data analysis and visualization

    [Install Jupyter](https://jupyter.org/install)
 
**Libraries**

Below are the links for details and commands (if required) to install the necessary Python packages:

Below are the links for details and commands (if required) to install the necessary Python packages:
- **pandas**: Go to [Pandas Installation](https://pypi.org/project/pandas/) or use command: `pip install pandas`
- **numpy**: Go to [NumPy Installation](https://pypi.org/project/numpy/) or use command: `pip install numpy`
- **matplotlib**: Go to [Matplotlib Installation](https://pypi.org/project/matplotlib/) or use command: `pip install matplotlib`
- **seaborn**: Go to [Seaborn Installation](https://pypi.org/project/seaborn/) or use command: `pip install seaborn`
- **scikit-learn**: Go to [Scikit-Learn Installation](https://pypi.org/project/scikit-learn/) or use command: `pip install scikit-learn`
- **surprise**: Go to [Surprise Installation](https://pypi.org/project/scikit-surprise/) or use command: pip install scikit-surprise`

### EDA Steps

- Data loading and initial exploration
- Data cleaning and manipulation
- Checking for missing values and duplicates
- Analyzing the distribution of product ratings


### Data Preprocessing Steps and Inspiration

- **Handling Missing Values**: Checked for missing values and duplicates in the dataset.
- **Subset Selection**: Selected a subset of the dataset for analysis to optimize performance.


### Graphs

![Distribution_of_ratings](https://i.postimg.cc/fbx0F2Pz/Screenshot-2024-05-27-at-12-52-23-Amazon-Reviews-Jupyter-Notebook.png)

![ratings_per_product](https://i.postimg.cc/Vv86tnBK/Screenshot-2024-05-27-at-12-54-02-Amazon-Reviews-Jupyter-Notebook.png)

![Distribution_average_ratings](https://i.postimg.cc/7LPYqqPW/Screenshot-2024-05-27-at-12-55-21-Amazon-Reviews-Jupyter-Notebook.png)


### Recommendation Techniques

- **Popularity-Based Recommender**: Recommends products based on their popularity (number of ratings).

- **Collaborative Filtering**:

a. **User-Based Filtering**:

- **KNNBasic**: A basic K-nearest neighbors algorithm for collaborative filtering based on user similarities.
- **KNNWithMeans**: An enhanced K-nearest neighbors algorithm that takes into account the mean ratings of users for better predictions.

b. **Item-Based Filtering**:
- **KNNBasic**: A basic K-nearest neighbors algorithm for collaborative filtering based on item similarities.
- **KNNWithMeans**: An enhanced K-nearest neighbors algorithm that takes into account the mean ratings of items for better predictions.

c. **Matrix Factorization (SVD)**: Uses Singular Value Decomposition to predict user ratings for products based on past user ratings.
  
### Assumptions

- Ratings provided by users are reliable.
- User preferences are consistent over time.
- Products with higher ratings are preferred by users.

### Evaluation Metrics

**RMSE (Root Mean Square Error)** was used to evaluate the performance of different models.

### Results 

**Top 30 products as per popularity recommender**

![top30](https://i.postimg.cc/Fs4DKbTf/Screenshot-2024-05-27-at-12-37-39-Amazon-Reviews-Jupyter-Notebook.png)

![RMSE Models Performance](https://i.postimg.cc/FzYK0Jrw/Screenshot-2024-05-27-at-12-32-53-Chat-GPT.png)

SVD was the best model with the least RMSE of 0.898

**Top 5 products for a given user(an example) with SVD**

![TOP5](https://i.postimg.cc/FRv2x8jj/Screenshot-2024-05-27-at-12-41-51-Amazon-Reviews-Jupyter-Notebook.png)

**Top 5 products similar to a given product(an example) with SVD**

![TOP5](https://i.postimg.cc/tgbzYjdG/Screenshot-2024-05-27-at-12-43-16-Amazon-Reviews-Jupyter-Notebook.png)

### Recommendations

- Further data collection and feature engineering could improve recommendation accuracy.
- Regularly updating the model with new product data can help maintain recommendation relevance.
- Implementing user feedback mechanisms to continuously improve recommendations.

### Limitations

- The dataset may contain biases that could affect the recommendations.
- The recommendation performance is limited by the quality and quantity of the available data.

### Future Possibilities of the Project

- Exploring additional recommendation algorithms and ensemble methods.
- Implementing deep learning models for better performance.
- Developing real-time recommendation systems based on user interactions.

### References

- [Scikit-learn documentation](https://scikit-learn.org/stable/)
- [Surprise documentation](https://pypi.org/project/scikit-surprise/)
- [Recommender Systems by Charu C. Aggarwal](http://pzs.dstu.dp.ua/DataMining/recom/bibl/1aggarwal_c_c_recommender_systems_the_textbook.pdf)


