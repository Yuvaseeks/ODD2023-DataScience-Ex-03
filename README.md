# ODD2023-DataScience-Ex-03
# Ex-03 Univariate Analysis
# Aim:
To read the given data and perform the univariate analysis with different types of plots.

# Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

# Algorithm:
### Step1:
Read the given data.

### Step2:
Get the information about the data.

### Step3:
Remove the null values from the data.

### Step4:
Mention the datatypes from the data.

### Step5:
Count the values from the data.

### Step6:
Do plots like boxplots,countplot,distribution plot,histogram plot.

# Program:
DEVELOPED BY : AAKASH P

REGISTER NO : 212222110001
```
import pandas as pd
import numpy as np
import seaborn as sns

df=pd.read_csv('superstore.csv')
df

df.head()
df.info()
df.describe()
df.isnull().sum()

df.dtypes

df['Postal Code'].value_counts()

sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x='Postal Code',data=df)
```
# OUTPUT:
# Dataset:
![1](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/781b5d74-727f-46a4-9828-ceecfb0e956e)

# Head:
![2](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/2508722f-131d-40b2-b1ee-8e95bed3601a)

# Info:
![3](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/6cbf9100-ea78-47c4-8c87-3d75e37097fb)

# Describe:
![4](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/ae407d2d-4f45-40ab-bd97-0d68dcf2ee17)

# Isnull:
![5](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/dcbba605-09ec-4c00-9ddc-bfe6310c11ec)

# dtypes:
![6](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/9dcf75d9-529d-4301-b766-bfc92760b489)

# Valuecount:
![7](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/b578e876-6433-4748-af15-30df40c161dc)

# Boxplot:
![8](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/4fe0798d-ccb3-434c-af5c-af1c699c0fc3)

# Countplot:
![9](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/5e4c263f-c860-4706-be7d-c3cc6aa0c2c4)

# Distribution plot:
![10](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/025b0641-20d7-408f-8e93-560a46384bf5)

# Histogram plot:
![11](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/de773a9d-a25a-44a6-9eaf-57937a5d1a4a)

# Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.

