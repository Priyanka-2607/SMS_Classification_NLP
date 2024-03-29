## Project: SMS Clasification using NLP
Author : Priyanka Sawant 


#### Dataset 
The dataset used for this project is SMS Spam Collection Dataset from kaggle. Insted of directly copiying the csv file of the data I have used kaggle api to get required dataset.[1] 

#### Challenges faced: 
1. Encoding issue while reading the csv file using pandas, to fix the issue passed the encoding argument. 
2. One of the parameter for ROC curve is binary repesenation of values in target column so converted target column values to 0 and 1. [2]

#### implementation:  

1. Kaggel API usage to download the dataset 
2. EDA: 
  - Read the CSV into data frame. 
  - Removed the Unwanted columns which has no meaningful data. 
  - Convert Target column from string to interger for binary classification. 
  - Check for null values if present replace it. 
  - check for duplicate values if present remove duplicate. 
3. Text Processing: 
  - Remove the HTML tages, Alphanumaric chars, digits, white space and converted text to lower case. 
  - Performed Tokenization and lemmatization. 
4. Train /Test data spilt: 
  - spilt the dataframe in 80% train and 20% test data.  
  - Ploted the target distribution and found that SPAM class samples are less than tha ham class so performed the sampling  t0 fix the imbalanced train data set.  
5. Visualization of text data using word cloud for each class.
6. Created pipline with bagging classifier(DT as default one) and tfidf vectorization for data processing 
7. Performed model evaluation and ploted the ROC curve and its value is 93% for decision tree classifier. 
8. Performed hypertuning of parameter using grid search with SVC as best estimator for this model. 
9. Evaluated the best estmiator on test dataset and ROC curve value 96% 


####  Reference:   
[1] https://adityashrm21.github.io/Setting-Up-Kaggle/ . 
[2] https://scikit-learn.org/stable/modules/generated/sklearn.metrics.RocCurveDisplay.html 