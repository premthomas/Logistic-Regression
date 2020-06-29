# Logistic Regression (and the thinking behind it)

## The case study
Data was collected using the Spotify Web API. The data consists of nineteen features. For example: danceability, loudness, chorus_hit). The author of the data has also populated a target column with the values 'hit' or 'flop' based on some conditions. The explaination of the dataset can be found on the Kaggle website which can be accessed by this [link](https://www.kaggle.com/theoverman/the-spotify-hit-predictor-dataset).

## Objective
To predict whether a song is a 'hit' or a 'flop'.

## Question: How do we know we have to use logistic regression?
The objective statement is one of your biggest indicators that you should be using logistic regression. First, we note that the output of the program will be a 'class'. The target columm in the data contains all the classes it needs to learn. In this example, the target column contains two classes: 'hit' and 'flop'. Secondly, the target column is categorical rather than a numerical value. The output could be a 1 or a 5. But these numbers represent classes and should not be taken as a numerical value. Besides the output cannot be a numerical value like 3.1415, which means nothing in terms of class numbers (which are ideally programmed as integer values). In a classification problem, the idea is to use the simplest classifier like logistic regression and to continue to test against different classifiers like Decision tress for better accuracies.


Should you not be given an objective statement, explore the data and see if you can identify the dependent and independent variables. If a column stands out to you to be the dependant column, then analyse the data in this column and check to see if you can find a pattern in the data. 

## Importing the data
The data is provided in a comma separated value (CSV) file. We can open in file in any spreadsheet reader (like Microsoft Excel) and explore the file as a whole. Viewing it in this manner gives us opportunities to look at the data in its entirety. We can quickly find the number of columns (or features), the number of rows of data, and maybe if we see any missing values. Using filters on the data allows us to check the data for missing values, the class names etc. 


The next part, is to explore using code. For this, we will first have to import the data from the file into the program
```Python
song_data = pd.read_csv('dataset-of-00s.csv')
song_data.head()
```

Output:
![song_data_head](https://github.com/premthomas/Logistic-Regression/blob/master/Images/song_data_head.jpg)

## Exploring the data
Start with find the number of columns (also popularly called features) and the number of rows of data. A dataframe object has the method called shape which returns a tuple with the number of rows and number of columns. The format of this data is '(no. of rows, no. of columns)'.

```Python
song_data.shape
```
Output:
![song_data_shape](https://github.com/premthomas/Logistic-Regression/blob/master/Images/song_data_shape.png)


