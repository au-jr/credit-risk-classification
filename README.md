# Module 12 Credit Risk Analysis

## Overview of the Analysis

In this Challenge, we used machine learning techniques to train and evaluate models to make an assessment based on loan risk. Logistic Regression modelling analysed historical lending information from a peer-to-peer lending services company identify the creditworthiness of borrowers, either as a healthy loan (0) or high-risk loan (1). The criteria, or features, we used to train model the data were loan size, interest rate, borrower income, debt ot income ratio, number of accounts, derogatory marks and total debt.

The credit risk data was split into training and testing datasets using train_test_split from sklearn.model_selection:

    from sklearn.model_selection import train_test_split

In order to prepare the data for machine learning we first needed to standardise the feature data using the StandardScaler module from sklearn.preprocessing:

    from sklearn.preprocessing import StandardScaler

Standardising the data reduces your features to their standard deviations. By doing so you eliminate 'big figure' bias where the magnitude of the measured feature may skew/bias the machine learning model to a greater extent than that feature influences the outcome in real life.

From here we've fitted the scaled training data into a logistic regression model using the LogisticRegression module from sklearn.linear_model:

    from sklearn.linear_model import LogisticRegression

The logistic regression model is a great way to assess and make predictions on data which yield a binary outcome, i.e yes/no or in this case, approved or denied for a loan.

Using the fitted training data a model has been created to which we can assess the real testing outcomes against the predicted testing outcomes using the model.

## Results

#### Accuracy Score:
- 0.99

#### Precision Score:

Approved: 
  - 1.00   
     
Denied: 
  - 0.84 
  
#### Recall Score:

Approved: 
  - 0.99    
    
Denied: 
  - 0.98     

## Summary

The LogisticRegression modelling technique produced a model capable of accurately preciting loan approval to 99% accuracy. From a pure mathematical stand-point this is a fantastic result and would be recommended for implementation.

In the model it is important that we're able to accurately predict successful loan applicants. If we were to approve an applicant unsuitable to receive a loan or who through traditional verification methods would be denied the loan, the organisation could expose themselves to significant losses. 

If we look at what the potential costs would be using the loan data we currently have avaiable:

  - The maximum loan size was: $23,800.00
  - The average loan size was: $9,805.56
  - The median loan size was: $9,500.00
  - The total number of applicants was: 77536
  - The number of expected high risk applicants receiving a loan accoring to the model is: 452.0
  - The potential cost of lending to high risk applicants is: $4,294,000.00

Overall given the potential gains through accrued interest or return customers should prompt the implementation of the model.





