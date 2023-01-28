# Clustering_Customers_Segmentation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Customer segmentation is used to segmented customer therefore we can classify the customer based on their behaviour, this customer segmentation usually used to help store to know how to treat their customers and know better about their customers, In this project I used machine learning which is clustering model to classify the customers.

# Dataset
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The dataset I downloaded from [Kaggle -  Customer Clustering](https://www.kaggle.com/datasets/dev0914sharma/customer-clustering). The dataset contains 8 columns which are:
1. ID - for customers ID
2. Sex - for customers gender {0: male, 1: female}
3. Marital Status - {0: single, 1: non-single(divorces / seperated / married / widowed)}
4. Age - Age of each customers
5. Education -  To determine education of each customers {0: other/unknown, 1: high school, 2: university, 3: graduate school}
6. Income - Income of each customers (annual in USD)

![image](https://user-images.githubusercontent.com/91602612/215123474-7e26f715-4464-4acd-b42d-ec1fb324ee6e.png)

# Exploratory Data Analysis

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this step I will explore the dataset to get insight from the dataset. I used following steps to explore my dataset:
1. Used .info() to see all the information of the dataset such as **2000 rows and 8 columns, the data type of all columns are int64**
2. I also used describe to see information of the dataset in statistical way such as mean, max, standard deviation and so on.
3. Then I used ```data.isnull().sum()``` to see if there is a missing values in the dataset, because it will very important to handle the missing value before build a machine learning model because it can impact to our model peformance, and fortunately there are no missing values in the dataset.
4. I also check for duplicated data in dataset.
5. I drop the unnecessary data column in this case I drop ID 
6. Then I am used univariate plot method to analyze the distribution for each existing column

# Data Preprocessing & Modeling

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this step I will start to preprocessing the dataset therefore the dataset can be used to build the machine learning model.I used the following steps to preprocessing my model and to modeling my dataset:
1. Convert the dataset into array therefore model can processed them
2. I used elbow method to see what is the best cluster number to choose
3. I used K-Means model with 4 cluster because 4 cluster is the best cluster number based on elbow method that we already plot
4. I used PCA to reduce the dimensionality into just 2 because I want to plot the result later. I fit and transform PCA into x variable therefore x now will only has 2 dimensionality
5. I fit and predict dataset that already reduced the dimensionality with K-Means model
6. I print the label to see the label distribution
7. I used unique label and scatter plot to plot the result

![image](https://user-images.githubusercontent.com/91602612/215239731-03d20a2a-923b-404d-9b52-887ab07ea508.png)


