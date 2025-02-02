# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
~~~
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
~~~
# OUPUT
# DATA:
![image1](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/Ds%20image%201.png)
![image2](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/DS%20img%202.png)
# NON NULL BEFORE:
![image3](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/Ds%20mg%203.png)
![image4](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/DS%20img%204.png)
![image5](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/Ds%20img%205.png)
# MODE:
![image6](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/Ds%20img%206.png)
# MEAN:
![image7](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/DS%20img%207.png)
# MEDIAN:
![image8](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/Ds%20img%208.png)
# NON NULL AFTER:
![image9](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/DS%20img%209.png)
![image10](https://github.com/vijay21500269/Ex-01-Data-Cleaning/blob/main/DS%20img%2010.png)
# RESULT:
Thus,the given data is read,cleansed and the cleaned data is saved into the file.







