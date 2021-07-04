# Housing_prices_competition_Kaggle
Contains the datasets and code for creating the submission for the housing prices competition in kaggle

To correctly access the code file do remember to extract the zip file "home-data-for-ml-course.zip" into a file with the same name and in the same directory as that of the jupyter notebook.

Though, the notebook contains comments for the steps taken in preprocessing to building a model and predicting with it, here I'll write down the work flow -->
1. Open the train and test sets into separate files (features are in columns and each row represents a single training example)
2. Delete the rows of data which have missing target values i.e. NULL in "SalePrice" from the train dataset.
3. Remove the SalePrice feature from the train dataset into a new variable Y.
4. Divide the train and test data into two parts, one having columns with object datatype and one with non-object datatype
5. Remove the GarageYrBlt column from the non-object dataframes of the test and train sets and Impute the missing values in them
6. Remove columns from the test and train dataframes having object datatypes, which don't have similar unique values between them
7. Remove columns with high number of missing values.
8. Label-encode the columns with high cardinality and One-Hot encode the columns with low cardinality.
9. Join the two pairs of dataframes into two final train and test set having non-object datatype values and categorized values
10. Train a random forest regressor with n_estimators as needed.
11. Fit the data using the train set and Y, and predict the result using the test set.

The submitted result yielded a MAE score of **16047.039**
![Kaggle Score](https://user-images.githubusercontent.com/49501411/124383999-07bb3000-dced-11eb-9909-7b801a1bdaeb.png)
