# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
import pandas as pd
df = pd.read_csv("Data_set.csv")

df.info()

df.isnull()

df.isnull().sum()

df=df.dropna(subset=['show_name'])
df.head()

df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()

df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].median())
df.head()

df=df.dropna(subset=['current_overall_rank'])
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].mean())
df.head()

df.info()
