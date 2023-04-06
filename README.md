# Ex-04-Multivariate-Analysis

## AIM
To perform Multivariate EDA on the given data set.

## Explanation 
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM:

### STEP 1
Import the built-in libraries required to perform EDA.

### STEP 2
Read the given csv file

### STEP 3
Convert the file into a dataframe and get info of the data.

### STEP 4
And also use HeatMap Plot Method to analyse. 

### STEP 5
Plot the counts in the form of Scatterplot or Bar Graph.

### STEP 6
Use seaborn the bar graph comparison of data can be viewed.

### STEP 7
Find the pairwise correlation of all columns in the dataframe.corr()

## PROGRAM
```python
Developed by Udayakumar R
Ref No: 22008609

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("SuperStore.csv")
df.head()
df.info()
df.describe()
sns.scatterplot(x=df['Postal Code'],y=df['Sales'])
df.dtypes
sns.barplot(x=df['Postal Code'],y=df['Row ID'],data=df)
states=df.loc[:,["Region","Row ID"]]
states=states.groupby(by=["Region"]).sum().sort_values(by="Row ID")
sns.barplot(x=states.index,y="Row ID",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("Region")
plt.ylabel=("ROW ID")
plt.show()
sns.barplot(x=df['Postal Code'],y=df['Ship Mode'],hue=df['Region'])
df.corr()
sns.heatmap(df.corr(),annot=True)
```
## OUTPUT

### DATA HEAD
![image](https://user-images.githubusercontent.com/118708024/230453526-4532d613-c33a-42b7-9477-a556012afe0c.png)
### DATA INFORMATION
![image](https://user-images.githubusercontent.com/118708024/230453631-38ea812e-1383-4f2d-8293-c650b5245476.png)
### DATA DESCRIBE
![image](https://user-images.githubusercontent.com/118708024/230453723-5565d8e7-acae-4ca8-a63c-5de76aceabd7.png)
### DATA TYPES
![image](https://user-images.githubusercontent.com/118708024/230453824-8509be5a-c977-4fa1-8941-3e4ab5432613.png)
### SCATTERPLOT
![image](https://user-images.githubusercontent.com/118708024/230453947-3ca44cf5-b377-4029-895c-72a3cd2730d9.png)
### BARPLOT
![image](https://user-images.githubusercontent.com/118708024/230454087-ab4d9297-4c91-45ae-a059-5d4b6f3c72d9.png)
![image](https://user-images.githubusercontent.com/118708024/230454184-f93e53ea-f97f-42ee-a7d5-ed2cc88b5321.png)
![image](https://user-images.githubusercontent.com/118708024/230454262-40e346c7-045d-495c-b3f9-8ab048d586cb.png)
### CORRELATION 
![image](https://user-images.githubusercontent.com/118708024/230454379-2e4a00e0-4885-4cf3-b8d9-4b9b41c4eeab.png)
### HEATMAP
![image](https://user-images.githubusercontent.com/118708024/230454468-dc158102-6b32-4965-b248-a1eb74223eb1.png)

## RESULT
Therefore we have readed the given data and performed the multivariate analysis with different types of
plots.
