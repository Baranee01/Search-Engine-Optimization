# Search Engine Optimization

Language Used : Python 3.8

Packages Used : numpy, pandas, seaborn, matplotlib, sklearn, statsmodels

##
### ABOUT THE DATASET
The dataset used for analysis is the keywords selection data from the SEO keywords repository called E-Grow. In that dataset there are 500 keywords related to shoes. They include 21 attributes, 19 are numeric and “keyword” attribute alone is a string. This also includes a class attribute.

Source : EGrow Keywords Repository

Link : https://in.egrow.io/member/keyword-niche-tool

##
### SAMPLE DATASET
![image](https://user-images.githubusercontent.com/80042740/117948020-5fad6a00-b32e-11eb-9017-00afd89d8ed7.png)

##
### FLOW OF THE PROJECT
• Data Preprocessing.

• Exploratory Data Analysis.

• Splitting training and test data.

• Builidng models.

• Results and Analysis.

##
### DATA PREPROCESSING
All the null values '?' are converted to Nan.

### CORRELATION HEATMAP OF UNPROCESSED DATA
![image](https://user-images.githubusercontent.com/80042740/117949684-03e3e080-b330-11eb-8b7b-cb72250a3ed3.png)

There are too many unwanted attributes present here. All the unwanted attributes will be dropped.

##
### CORRELATION HEATMAP OF PROCESSED DATA
![image](https://user-images.githubusercontent.com/80042740/117949849-2d047100-b330-11eb-91b0-6a559ffb8a75.png)

##
### COUNT OF YES AND NO
The values of class attribute 'use' are converted into NO : 0 and YES : 1 by label encoding.

![image](https://user-images.githubusercontent.com/80042740/117950255-a00de780-b330-11eb-9d56-a007135127fa.png)

Here we can find that there are more keyword acceptance (357) than keyword rejections (143). The dataset shows the interest of the person to include as many keywords as possible which has a decent opportunity.

##
### EXPLORATORY DATA ANALYSIS

### RELATIONSHIP BETWEEN BSR_AVG AND OPPURTUNITY_SCORE
![image](https://user-images.githubusercontent.com/80042740/117950481-d9deee00-b330-11eb-9d58-4f12efe7fa91.png)

Here, we can find that the probability of rejection increases when the BSR is large and the Opportunity Score is less than 3. We can also find that the graph suggests that most of the keywords has its Average BSR within 100000. We also found the correlation coefficient between these two attributes to be -0.44. This highly suggests a negative correlation between the two variables.

##
### RELATIONSHIP BETWEEN REVENUE_AVG AND PRICE_AVG
![image](https://user-images.githubusercontent.com/80042740/117951338-b4061900-b331-11eb-978f-d1fca358569e.png)

Here, we can find that there is only one outlier on the top right of the graph. When we consider the rest of the data, we can find the Average price of shoes roughly comes between 200-10000. The Price corresponds to the Revenue as well. Through the heatmap, we find that there lies a strong positive correlation between them with correlation coefficient as 0.96.

##
### RELATIONSHIP BETWEEN SALES_AVG AND BSR_AVG
![image](https://user-images.githubusercontent.com/80042740/117951545-e57ee480-b331-11eb-90dd-5367f0a8ec1a.png)

We can find a datapoint in the top left corner of the graph. Here, we can find the Average sales of shoes roughly comes between 0-300. The Price corresponds to the BSR as well. Through the heatmap, we find that there lies a negative correlation between them with correlation coefficient as -0.37.

##
### RELATIONSHIP BETWEEN SALES_AVG AND OPPURTUNITY_SCORE
![image](https://user-images.githubusercontent.com/80042740/117951674-05160d00-b332-11eb-97b1-a4e5bbf7f115.png)

Here, by considering the scattered datapoints, we can find the Average Sales of shoes roughly comes between 0-300. The Price corresponds to the Revenue as well. Through the heatmap, we find that there lies a positive correlation between them with correlation coefficient as 0.65.

##
### MODELS
We have implemented 6 models which are:

• K – Nearest Neighbour (KNN)

• Logistic Regression

• Naive Bayes Classifier

• Decision Tree Classifier

• Random Forest Classifier

• Support Vector Machines Classifier

##
### KNN
![image](https://user-images.githubusercontent.com/80042740/117953021-5c68ad00-b333-11eb-97ef-fe7c4f51296e.png)

KNN model has classified the keywords with an accuracy of 89%.

### LOGISTIC REGRESSION
![image](https://user-images.githubusercontent.com/80042740/117953613-d0a35080-b333-11eb-947a-4f895829b74f.png)

Logistic Regression model has classified the keywords with an accuracy of 82%.

### NAIVE BAYES
![image](https://user-images.githubusercontent.com/80042740/117953732-f0d30f80-b333-11eb-8be1-2861f7e2fe82.png)

Naive Bayes model has classified the keywords with an accuracy of 86%.

### DECISION TREE
![image](https://user-images.githubusercontent.com/80042740/117953929-2841bc00-b334-11eb-8422-986dfc546030.png)

Decision Tree model has classified the keywords with an accuracy of 87%.

### RANDOM FOREST
![image](https://user-images.githubusercontent.com/80042740/117954106-50c9b600-b334-11eb-8ecc-9f8e74bf43c5.png)

Random Forest model has classified the keywords with an accuracy of 92%.

### SUPPORT VECTOR MACHINES
![image](https://user-images.githubusercontent.com/80042740/117954240-75be2900-b334-11eb-9075-597cca43c313.png)

Support Vector Machines model has classified the keywords with an accuracy of 90%.

##
### RESULTS AND ANALYSIS
![image](https://user-images.githubusercontent.com/80042740/117954591-cc2b6780-b334-11eb-9d1b-620e7143e4ac.png)

By comparing all the models, Random Forest Classifier has performed well with an accuracy of 92%. 

The results of these predictions can be added to the domain of SEO and can be used for providing suggestions in the domain by making it easy for professionals in identifying the best keywords to use for Campaign.
