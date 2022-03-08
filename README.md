# Bank-customer-churn-prediction
We will test different models and machine learning techniques to determine which one is the most accurate for bank customer churn prediction.

### Introduction

In phase 1, we had decided to conduct this project on Environmental Impact of Food Production. However, during the conduction of CRISP-DM
methodology we encounter our first issue: the lack of useful datasets on this regard. Therefore, we decided to change our Project Domain to Financial
and as a result also the Research Questions.
In order to develop this project, we have decided to follow CRISP-DM model. Cross Industry Standard Process for Data Mining is a model which
describes the life cycle of data science. It works as a guide in order to plan, organize and implement machine learning. This process is divided into six
phases such as Business Understanding, Data Understanding, Data Preparation, Modelling, Evaluation and Deployment (CRISP-DM - Data Science Process Alliance, 2021).
One of the biggest benefits of CRISP-DM is to identify issues in the process or even avoid them in the early stages of the project (Manasson, 2019).

### 1. Business Understanding

First step of CRISP-DM is Business Understanding. Most important in this step is to define the problem and the objectives of the project by assessing
the situation.
Nowadays companies have to face a large number of competitors and in
Financial Sector it is not different. With the high number of options customers have available it has become more and more important to the 
companies to retain their customers. Keep an existing customer is easier than to attract new ones, just as it is easier to prevent them from leaving
the company than to convince customers to return. Also, the costs to attract new customers are often higher than the costs to retain existing customers.
Therefore, it is important to understand and avoid customer churn (Customer Churn: Definition, Measurement &amp; Prevention | Qualtrics, n.d.).
The objectives of this project are to answer questions such as the does the variables affect whether customers stay or go; and when
customers are prone to move to competitors. We aim to develop a model to predict customer churn.

### 2. Data Understanding

Second step of CRISP-DM is understanding the data we are working in this project. Therefore, we have searched for different datasets and discovered
a dataset from Kaggle website in kaggle.com/barelydedicated/bank-customer-churn-modeling/version/1 which contains useful information on
customer churn.
Once dataset was found we had to explore the data within the dataset. 
Therefore, we developed EDA – Exploratory Data Analysis and used Pandas Library in order to load into Jupiter Notebook and have a clear
understanding of the features names, the number of variables within the dataset, NumPy Library for mathematical calculations and also used Seaborn
and Matplot Libraries for data visualisation.
By exploring our dataset, we concluded it has 14 features and 10,000 observations. However, not all features are relevant such as Row Number,
Customer Id and Surname, these features have no impact in customer churn. Therefore, 11 of the total 14 columns are relevant to this project as
they can have an effect on customer churn which are:
Credit Score: customers with a higher credit score are less likely to leave the bank.
Geography: the customers their decision to leave the bank can be affected by their location.
Gender: it could be interesting for the bank to understand if gender has an important role in the customers decisions to leave.
Age: this is an important feature as older customers are more likely to stay.
Tenure: this feature is in regarding to the number of years the customers have been a client of the company. Usually, older customers tend to be
more loyal therefore less expected to leave.
Balance: this is an important indicator as people with a higher account balance are more likely to stay compared to clients with lower balances.
Number of Products: this feature informs the number of products the clients have purchased from the company.
Has Credit Card: this variable informs if the customer has a credit card or not. Also, an important feature as customers who have a credit card are
more likely to stay.
Is Active Member: the more active a customer is the more likely this customer will stay.
Estimated Salary: customers with lower salaries are more likely to leave the company compared to those clients with higher salaries.
Exited: this is the labelled variable and it brings the information whether or not the customer left.
The dataset chosen is a supervised dataset as it has a label which is the “Exited” variable. This is the dependent variable while the other ones are
the independent variables.
We have also checked for duplicates and missing values within this dataset and concluded there are no duplicate or missing values.

### 3. Data Preparation

This is perhaps the most time-consuming phase of CRISP-DM as in this step we need to manage any errors or inconsistencies within the dataset. In this
step, we performed the below changes to our data set:
We checked and removed the columns which were not relevant for our analysis. Therefore the 3 columns: Row Number, Customer Id and Surname
have been removed as these have no effect on customers&#39; churn; Renamed features to improve the readability of our dataset;
Performed main mathematical calculations on quantitative variables (mean, minimum, median, maximum, first and third quartile, standard deviation to
see the distance of the observations from their mean); Explored qualitative variables; Visualization the data by plotting histograms,
boxplot; Checked correlations between variables through Scatterplot and Heat Map.
The EDA (Exploratory Data Analysis) performed on Jupyter Notebook has been uploaded with this report.

### 4. Modelling
Fourth stage of CRISP-DM is Modelling. In this section we will assess different machine leaning algorithms in order to select the modelling
technique which we will apply to our project, we will also generate test design, build and assess the model.
As previously mentioned, the dataset chosen to conduct this project is a supervised dataset. Supervised learning which is determine by labelled
dataset in order to train the algorithms to classify or predict the outcome. In a broad explanation, the data used to feed the model is adjusted in order to
fit the model appropriately and this is the cross-validation part of the process (Education, 2020). Classification algorithms are used to create models which will allocate the
data into categories while Regression algorithms are used to understand the relation between the dependent variable and the independent variables of
the dataset. Therefore, for this project we will use Regression algorithms in order to understand the relationship between dependent and independent
variables and built a model to predict bank customers&#39; churn. 
In supervised learning there are many different algorithms available. Some of them such as Support Vetor Machine (SVN), K-Nearest Neighbour (KNN),
Linear Regression, Logistics Regression, Random Forest, Neural Network and many more. For this project we consider two different algorithms to build
the model:

Randon Forest
This supervised algorithm can be used for classification and regression models. “The forest references a collection of uncorrelated decision trees,
which are then merged together to reduce variance and create more accurate data predictions” (Education, 2020).

Logistic Regression
Logistic Regression is mostly used to answer binary classification problems.
It is adopted when the dependent variable has binary outputs (Education, 2020). In this project the dependent variable is “Exited” and the output of
this is either 0 or 1 for customers who left the bank or not respectively.

KNN
This supervised machine learning algorithm “relies on labelled input data to learn a function that produces an appropriate output when given new
unlabelled data” (Harrison, 2018).
It is an “non-parametric algorithm that classifies data points based on their proximity and association to other available data. This algorithm assumes
that similar data points can be found near each other” (Education, 2020).
KNN is commonly used for image recognition.
We plan to build our machine learning model based on one of the models mentioned above. In order to do that the dataset will be split into testing
and training set. Then the training data will be used to train our model to predict bank customers churn.

### 5. Evaluation
In this stage of CRISP methodology, we will evaluate the results of our model by checking the accuracy of the training and testing data, if the
training or testing scores are too low, the process will be reviewed in order to improve it. Furthermore, in this stage we will evaluate if the model works
correctly and all the important factors have been considered.
### 6. Deployment
Final step of CRISP-DM is the Deployment. In this step we will review our project, monitor and maintain our model, and produce a clear
final report to which our model can be reproducible and maintainable. Furthermore, we will include a Jupyter Notebook with detailed explanation of each step calculated using Python while justifying our answers and documenting all steps.
