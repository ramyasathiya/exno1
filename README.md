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
```
df.tail(5)
```
![image](https://github.com/user-attachments/assets/6c822ae8-3521-4d54-af92-abecee72f8a2)
```
df.isnull()
```
![image](https://github.com/user-attachments/assets/64c618f6-8bcb-4d54-850b-872bba873524)
```
df.notnull()
```
![image](https://github.com/user-attachments/assets/3e6d66cd-aa72-4a93-bbae-f88f86dd4cb0)
```
df.dropna(axis=0)
```
![image](https://github.com/user-attachments/assets/394f2e97-7563-4d77-b4bf-c2272a4bec54)
```
df.dropna(axis=1)
```
![image](https://github.com/user-attachments/assets/01f5af3c-a9d2-41c6-bb3d-52fdc2e04e07)
```
df.fillna(0)
```
![image](https://github.com/user-attachments/assets/069fcdcb-eca5-4409-9a48-6c831c655552)
```
print(df.shape)
```
(21, 12)
```
import pandas as pd
import seaborn as sns
ir=pd.read_csv('/content/iris.csv')
ir
```
![image](https://github.com/user-attachments/assets/f57ceb30-8ce5-4ec5-9fe1-46faa0ba19e5)
```
ir.describe()
```
![image](https://github.com/user-attachments/assets/5be98e24-27d0-4329-a192-15fa936cf117)
```
sns.boxplot(x='sepal_width',data=ir)
```
![image](https://github.com/user-attachments/assets/04f9fcee-3ff2-48e3-b08d-fa390378eb64)
```
c1=ir.sepal_width.quantile(0.25)
c3=ir.sepal_width.quantile(0.75)
iq=c3-c1
print(c3)
```
3.3
```
rid=ir[((ir.sepal_width<(c1-1.5*iq))|(ir.sepal_width>(c3+1.5*iq)))]
rid['sepal_width']
```
![image](https://github.com/user-attachments/assets/997036e0-bc99-44ab-be98-6fa2be13d16f)
```
delid=ir[~((ir.sepal_width<(c1-1.5*iq))|(ir.sepal_width>(c3+1.5*iq)))]
delid
```
![image](https://github.com/user-attachments/assets/60ba40ab-d7a3-417f-b3f8-b0d94d1d869c)
```
sns.boxplot(x='sepal_width',data=delid)
```
![image](https://github.com/user-attachments/assets/3c6a2f34-5796-46f0-a4b4-cd0cfccdb45e)
```
import matplotlib.pyplot as plt
import pandas as pd
import pandas as pd
import numpy as np
import scipy.stats as stats
dataset=pd.read_csv("/content/heights.csv")
dataset
```
![image](https://github.com/user-attachments/assets/63dbbfb5-03ec-4213-867d-574e3bd7653c)
```
df = pd.read_csv("heights.csv")
q1 = df['height'].quantile(0.25)
q2 = df['height'].quantile(0.5)
q3 = df['height'].quantile(0.75)
iqr = q3-q1
iqr
```
0.9249999999999998
```
low = q1 - 1.5*iqr
low
```
3.8625000000000003
```
high = q3 + 1.5*iqr
high
```
7.5625
```
df1 = df[((df['height'] >=low)& (df['height'] <=high))]
df1
```
![image](https://github.com/user-attachments/assets/71b8cc19-86c3-4db1-9e38-355f44991a15)
```
z = np.abs(stats.zscore(df['height']))
z
```
![image](https://github.com/user-attachments/assets/2bc21a74-15ba-457c-83e9-8fbd4e9b9079)
```
df1 = df[z<3]
df1
```
![image](https://github.com/user-attachments/assets/e910ddff-9a26-462e-aa60-3bb24e24689c)


















# Result
          Thus,it read the given data and perform data cleaning and save the cleaned data to a file.
          
