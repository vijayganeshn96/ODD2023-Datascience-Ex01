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

# CODE
```py
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
```


# Output

<img width="438" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/4aff9e29-73a1-421f-aa2e-1b82869ed549">

<br><br>

<img width="438" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/a44d9869-5a93-406e-84f6-3332f30e2d61">
<br><br>

<img width="408" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/5cc94334-3ed5-43d2-8ac0-8a80cda67703">
<br><br>

<img width="180" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/31e46049-62ff-439e-a700-fd04604df209">
<br><br>

<img width="438" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/d1a5a1de-5b68-46fd-aeba-db7697e25325">
<br><br>

<img width="446" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/1856bd2e-322f-4246-a428-0bcbaace20c7">
<br><br>

<img width="451" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/2dcc5f91-fde1-4770-9bf7-b815d95140af">
<br><br>

<img width="445" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/b588d631-d9b4-42a5-816f-440705edc5d0">
<br><br>

<img width="357" alt="image" src="https://github.com/knight7080/ODD2023-Datascience-Ex01/assets/88542035/e553adbb-04cd-4057-927f-35256241cf90">
<br><br>


# RESULT

Thus the given data is read,cleansed and the cleaned data is saved into the file.
