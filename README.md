# IBM Final Project for Machine Learning with Python course

To finish this IBM course provided by Coursera, I have to finish this project. I created model using the following algorithm :

*   K Nearest Neighbor(KNN)
*   Decision Tree
*   Support Vector Machine
*   Logistic Regression

The model built using Loan_train.csv dataset. After finding the model based on each algorithm, I used Loan_test.csv (another dataset which never seen by the model) to train the model and see the score in the evaluation matrix

## 1. About Dataset

This dataset is about past loans. The **Loan_train.csv** data set includes details of 346 customers whose loan are already paid off or defaulted. It includes following fields:

| Field          | Description                                                                           |
| -------------- | ------------------------------------------------------------------------------------- |
| Loan_status    | Whether a loan is paid off on in collection                                           |
| Principal      | Basic principal loan amount at the                                                    |
| Terms          | Origination terms which can be weekly (7 days), biweekly, and monthly payoff schedule |
| Effective_date | When the loan got originated and took effects                                         |
| Due_date       | Since it’s one-time payoff schedule, each loan has one single due date                |
| Age            | Age of applicant                                                                      |
| Education      | Education of applicant                                                                |
| Gender         | The gender of applicant                                                               |

Model will predict the customer from **Loan_test.csv** whether they likely to "Paid Off" the loan or the loan will keep hanging on "Collection" after the due date

## 2. Data Visualization
Insight derived from dataset to see hidden pattern on the data

* Loan is paid off or no after due date based on basic loan amount. ( grouping by Gender, 0 = Male, 1 = Female)

![Screenshot](https://github.com/astry-ec/loan_prediction/blob/main/images/gender.png)

* Loan is paid off or no after due date based on age. ( grouping by Gender, 0 = Male, 1 = Female)

![Screenshot](https://github.com/astry-ec/loan_prediction/blob/main/images/gender02.png)

* Loan is paid off or no after due date based on day the loan took effect. ( grouping by Gender, 0 = Male, 1 = Female)

![Screenshot](https://github.com/astry-ec/loan_prediction/blob/main/images/gender03.png)

## 3. Feature Selection and Preprocessing Data

Based on insight on point 2. Feature Selection choosen are below
'Principal','terms','age','Gender','weekend']]
* Principal
* Terms
* Age
* Gender
* The day loan made (weekend or not)
* Education

I used StandardScaler as preprocessing to Normalize the data

## 4. Algorithm

As mentioned, algorithm used are

*   K Nearest Neighbor(KNN)
*   Decision Tree
*   Support Vector Machine
*   Logistic Regression

## 5. Evaluation Matrix

Model will predict the customer from **Loan_test.csv** which is data that never seen by the models. 
I perform Jaccard, F1 Score and Log Loss (only for Logistic Regression) Evaluation Matrix.

Below is the result of the model evaluation

![Screenshot](https://github.com/astry-ec/loan_prediction/blob/main/images/evaluation%20matrix%20models.png)
