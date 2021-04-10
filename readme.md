TASK 3
Assignment Details-
Use a given dataset to build a model to predict the category using description. Write code in python. Using Jupyter notebook is encouraged. 

Show how you would clean and process the data
Show how you would visualize this data
Show how you would measure the accuracy of the model
What ideas do you have to improve the accuracy of the model? What other algorithms would you try?


DATSET:
The dataset flipkart_com-ecommerce_sample.csv(36.35)is taken from KAGGLE.
The link is given below:
https://www.kaggle.com/arindamroy23/product-category-prediction-99acc?select=flipkart_com-ecommerce_sample.csv

This is a pre-crawled dataset, taken as subset of a bigger data set (more than 5.8 million products) that was created by extracting data from Flipkart.com, a leading Indian eCommerce store.

  
Software USED:
Jupiter Nootebook

1)CLEANING DATA:

input: str_arg --> Takes string to clean
    output: cleaned_str --> Gives back cleaned string
    This fuction cleans the text in the mentioned ways as comments after the line.This has been copied from some other kernel.

    *Every char except alphabets is replaced
    *multiple spaces are replaced by single space
    *converting the cleaned string to lower case
    *Returning the preprocessed string in tokenized form


2)DATA VISUALIZATION:

data_df.info()
*it gives the summary of the dataframe and prive the information about the data.

data_df.shape
*this gives the size of the dataframe.

data_df.columns
*gives the columns which is presnt in the dataframe 

data_df.describe
*it is used to view statistical detailes such as mean,std, percentile etc.

data_df.head(n=5)
it gives top 5 rows

the Brand column has lots of null values.

plt.figure(figsize =(12,8))
sns.heatmap(data_df.isnull(),yticklabels=False,cmap='Blues',cbar=True)
cmap=sns.diverging_palette(220,220,as_cmap=True)
ax=sns.heatmap(data_df.corr(),cmap=cmap)
*Heat maps display numeric tabular data where the cells are colored depending upon the contained value.

3)ACCURACY OF THE MODEL:

For predicting the accuracy i have used the naive bayes model.
*first spliting the train and test data in the ratio of 70/30.
*convert the train data into vectorized form.
*and i found the good results 
0.9805858603212783
0.9719438877755511
              precision    recall  f1-score   support

           0       0.95      0.99      0.97       281
           1       0.89      0.95      0.92       205
           2       1.00      0.99      1.00      1895
           3       0.92      0.79      0.85       163
           4       0.98      0.98      0.98       368
           5       0.97      1.00      0.98       285
           6       0.98      0.97      0.98       210
           7       0.95      1.00      0.97      1081
           8       0.99      0.87      0.93       199
           9       0.97      0.87      0.92       303

    accuracy                           0.97      4990
   macro avg       0.96      0.94      0.95      4990
weighted avg       0.97      0.97      0.97      4990

Testing Block: Test your sting. Replace the 'car' string to test.


4)i have used the naive bayes it gives very good results.