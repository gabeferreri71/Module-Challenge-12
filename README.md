# Module-Challenge-12: Credit Risk Resampling
## Split the Data into Training and Testing Sets
### 1. First, because I used google.colab, we "from google.colab import files", and store the uploaded files with uploaded = files.upload(). We next create a variable, lending_df, with contains the .csv info via the pd.read_csv() function. lending_df can then be reviewed with the .head() function. 

### 2. For y and X, we set y to the 'loan_status' column of lending_df, and X to all the columns of lending_df except 'loan_status', with lending_df.loc[:, lending_df.columns != 'loan_status']. Both can then be reviewed with the .head() function. 

### 3. To check the labels variable balance of y, we simply use y.value_counts()

### 4. First, train_test_split is imported from sklearn. To split the data, the following is entered with random_state = 1:

### X_train, X_test, y_train, y_test = train_test_split(X, y, random_state = 1)

## Create a Logistic Regression Model with the Original Data
### 1. First, LogisticRegression is imported from sklearn. To initiate the model, we created a variable and assigned it to LogisticRegression(random_state = 1), and then fit the variable using .fit() with interior parameters of X_train and y_train.

### 2. We made a predictions variable assigned to the initiated model this time using .predict() with an interior parameter of X_test.

### 3. To print a balanced accuracy score, we simply input balanced_accuracy_score(y_test, predictions); for the confusion matrix, we simply input confusion_matrix(y_test, predictions); to print the classification report for the model, we simply input print(classification_report_imbalanced(y_test, predictions)).

### 4. See response in notebook file.

## Predict a Logistic Regression model with Resampled Training Data
### 1. We first import randomOverSampler from imblearn. Similar to before, we now need to instantiate the oversampler model this time, which can be done by creating a variable and assigning it to RandomOverSampler(random_state=1). Next, we need to fit the original training data to the random oversampler model, using the fit_resample(X_train, y_train) function applied to the variable of the instantiated model. Lastly, now y_resampled can have its distict values counted using y_resampled.value_counts.

### 2. With the LogisticRegression classifier, we instantiate a model, in this case named 'model', with LogisticRegression(random_state=1). We next fit the model with the .fit() function and X_resampled and y_resmapled interior parameters. Last, we predict the model with the .predict() function and interior parameter of X_test. 

### 3. For the balanced accuracy score, we simply input balanced_accuracy_score(y_test, y_pred); for the confusion matrix, we input print(confusion_matrix(y_test, y_pred)); lastly, for the imbalanced classification report printed, we input print(classification_report_imbalanced(y_test, y_pred)).

### 4. For answer, please refer to the notebook file.
