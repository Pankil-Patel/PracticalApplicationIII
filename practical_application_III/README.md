# Practical Application III
AI ML practical application 3
Link to my gibhub URL: https://github.com/Pankil-Patel/practical_application_III/edit/main/prompt_III.ipynb
<br/><br/><b>Key Findings</b>
1. Original total records in the dataset was as shown below.
![alt text](images/1_totalrecords_eachcolumn.PNG)

   Of the 41188 records, Total duplicate records removed: 12. Below is the plot showing the total remaining records.
 ![alt text](images/2_totalrecords_afterremovingduplicates.PNG)
2. Based on the above finding, there are no specific outliers that we need to remove.
3. Based on the unique values, only the yes/no column is getting changed to 1/0 which will allow us to include it in the correlation matrix. The correlation matrix can provide more information on whether the target data has any corelation with any of the other features.
4.  ![alt text](images/3_correlationmatrix.PNG)
<br/>Based on the correlation map, The duration and previous call can possibly be two reasons that are directly related to customer making a decsion. However, based on the data the user's employment status, Euro Rate, consumer price index and employment variable rate could be impacting that decision. 
5. Based on the histogram plots, the data is distributed for most columns except for duration, campaign, pdays and previous. We are going to keep this records intact for now until further analysis.
6. Based on the box plots, only Job, Month and POutcome are the only three categorical features that have direct relationship with outcome of user subscribing to bank's cd.
7. <b>Business Objective</b>: The main business objective is to review the data and predict what criteria will lead to customer opting for subscribing to a bank deposit with the bank. This determination can help the bank focus on those customers to increase the success rate for the people opting for term deposit with the bank.
8. Based on the initial model performance for <b>LogisticRegression</b>, the accuracy of the model was <b>89.32%</b> which was better than the baseline performance set for 80%.
9. Based on the table below, <b>SVM</b> took the longest in terms of execution time but had similar Test accuracy, precision and recall score to <b>LogisticRegression</b> suggesting LogisticRegression performed the best. 
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Model</th>
      <th>Train Time</th>
      <th>Train Accuracy</th>
      <th>Test Accuracy</th>
      <th>Precision</th>
      <th>Recall</th>
      <th>F1-Score</th>
      <th>ROC-AUC</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td><font color="green">Logistic Regression</font></td>
      <td><font color="green">0.184549</font></td>
      <td>0.912386</td>
      <td><font color="green">0.904687</font></td>
      <td>0.791551</td>
      <td>0.684107</td>
      <td>0.720955</td>
      <td>0.684107</td>
    </tr>
    <tr>
      <th>1</th>
      <td>KNN</td>
      <td>1.283232</td>
      <td>0.926806</td>
      <td>0.895580</td>
      <td>0.753734</td>
      <td>0.677607</td>
      <td>0.705939</td>
      <td>0.677607</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Decision Tree</td>
      <td>0.262966</td>
      <td>1.000000</td>
      <td>0.883439</td>
      <td>0.719475</td>
      <td>0.717120</td>
      <td>0.718287</td>
      <td>0.717120</td>
    </tr>
    <tr>
      <th>3</th>
      <td>SVM</td>
      <td>96.417101</td>
      <td>0.920795</td>
      <td>0.905051</td>
      <td>0.799054</td>
      <td>0.674053</td>
      <td>0.713904</td>
      <td>0.674053</td>
    </tr>
  </tbody>
</table>
</div>
10. <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Model</th>
      <th>Train Time</th>
      <th>Train Accuracy</th>
      <th>Test Accuracy</th>
      <th>Precision</th>
      <th>Recall</th>
      <th>F1-Score</th>
      <th>ROC-AUC</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td><font color="green">Logistic Regression</font></td>
      <td><font color="green">0.184549</font></td>
      <td>0.912386</td>
      <td><font color="green">0.904687</font></td>
      <td>0.791551</td>
      <td>0.684107</td>
      <td>0.720955</td>
      <td>0.684107</td>
    </tr>
    <tr>
      <th>1</th>
      <td>KNN</td>
      <td>1.283232</td>
      <td>0.926806</td>
      <td>0.895580</td>
      <td>0.753734</td>
      <td>0.677607</td>
      <td>0.705939</td>
      <td>0.677607</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Decision Tree</td>
      <td>0.262966</td>
      <td>1.000000</td>
      <td>0.883439</td>
      <td>0.719475</td>
      <td>0.717120</td>
      <td>0.718287</td>
      <td>0.717120</td>
    </tr>
    <tr>
      <th>3</th>
      <td>SVM</td>
      <td>96.417101</td>
      <td>0.920795</td>
      <td>0.905051</td>
      <td>0.799054</td>
      <td>0.674053</td>
      <td>0.713904</td>
      <td>0.674053</td>
    </tr>
    <tr>
      <th>4</th>
      <td>SVM</td>
      <td>1.524682</td>
      <td>0.912386</td>
      <td>0.904687</td>
      <td>0.791551</td>
      <td>0.684107</td>
      <td>0.720955</td>
      <td>0.684107</td>
    </tr>
    <tr>
      <th>5</th>
      <td>SVM</td>
      <td>4.826636</td>
      <td>0.918913</td>
      <td>0.900194</td>
      <td>0.778379</td>
      <td>0.663716</td>
      <td>0.700345</td>
      <td>0.663716</td>
    </tr>
    <tr>
      <th>6</th>
      <td>SVM</td>
      <td>1.787235</td>
      <td>0.918124</td>
      <td>0.910879</td>
      <td>0.793954</td>
      <td>0.746504</td>
      <td>0.767230</td>
      <td>0.746504</td>
    </tr>
    <tr>
      <th>7</th>
      <td>SVM</td>
      <td>2.617027</td>
      <td>0.912386</td>
      <td>0.904687</td>
      <td>0.791551</td>
      <td>0.684107</td>
      <td>0.720955</td>
      <td>0.684107</td>
    </tr>
    <tr>
      <th>8</th>
      <td>SVM</td>
      <td>4.874183</td>
      <td>0.918913</td>
      <td>0.900194</td>
      <td>0.778379</td>
      <td>0.663716</td>
      <td>0.700345</td>
      <td>0.663716</td>
    </tr>
    <tr>
      <th>9</th>
      <td>SVM</td>
      <td>3.234069</td>
      <td>0.918124</td>
      <td>0.910879</td>
      <td>0.793954</td>
      <td>0.746504</td>
      <td>0.767230</td>
      <td>0.746504</td>
    </tr>
    <tr>
      <th>10</th>
      <td>SVM</td>
      <td>1464.007474</td>
      <td>0.920795</td>
      <td>0.905051</td>
      <td>0.799054</td>
      <td>0.674053</td>
      <td>0.713904</td>
      <td>0.674053</td>
    </tr>
  </tbody>
</table>
</div>
<b><font color="green">Conclusion</font></b>:<br/> In this project, we used a dataset from UCI Machine Learning Repository to predict whether a customer will subscribe to a term deposit or not. The dataset contains 41188 rows and 21 columns. We performed data cleaning, exploratory data analysis, feature engineering, feature selection, and model building. We used four different models to predict the outcome. The best model was Logistic Regression with an accuracy of 90.4%. We also used GridSearchCV to find the best hyperparameters for each model. The best hyperparameters for Logistic Regression were C = 1 and penalty = l2. The best hyperparameters for KNN were n_neighbors = 9. The best hyperparameters for Decision Tree were criterion = gini and max_depth = 5. The best hyperparameters for SVM were C = 1 and kernel = rbf. We also compared the performance of each model before and after hyperparameter tuning. The performance of each model improved after hyperparameter tuning. 
