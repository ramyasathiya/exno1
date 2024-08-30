# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
## Data cleaning process:
```
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```
![image](https://github.com/user-attachments/assets/7de4e842-d2d4-4345-aaea-7c9688d3d357)
```
df.head()
```
![image](https://github.com/user-attachments/assets/a5bed056-620e-4cb0-b882-f34f2b3f1384)
df.tail(5)
```
![image](https://github.com/user-attachments/assets/6c822ae8-3521-4d54-af92-abecee72f8a2)
df.isnull()
```
![image](https://github.com/user-attachments/assets/64c618f6-8bcb-4d54-850b-872bba873524)
df.notnull()
```
![image](https://github.com/user-attachments/assets/3e6d66cd-aa72-4a93-bbae-f88f86dd4cb0)
df.dropna(axis=0)
```
![image](https://github.com/user-attachments/assets/394f2e97-7563-4d77-b4bf-c2272a4bec54)
df.dropna(axis=1)
```
![image](https://github.com/user-attachments/assets/01f5af3c-a9d2-41c6-bb3d-52fdc2e04e07)
df.fillna(0)
```
![image](https://github.com/user-attachments/assets/069fcdcb-eca5-4409-9a48-6c831c655552)








# Result
          <<include your Result here>>
