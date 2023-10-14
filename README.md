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
DEVELOPED BY : YUVASREE

REGISTER NO : 212221040188
```
- Diabetes.csv
```Python 
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
df=pd.read_csv('diabetes.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x="Glucose",data=df)
Glucose_q1 = df['Glucose'].quantile(0.25)
Glucose_q3 = df['Glucose'].quantile(0.75)
Glucose_IQR = Glucose_q3 - Glucose_q1
Glucose_low = Glucose_q1 - 1.5 * Glucose_IQR
Glucose_high = Glucose_q3 + 1.5 * Glucose_IQR
df=df[((df['Glucose']>=Glucose_low)&(df['Glucose']<=Glucose_high))]
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)
```
- Output(diabetes.csv) :<br>
![1](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/5d11ecab-30ad-4ad9-8745-179ea397b4c0)
![2](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/27c8ff73-3e54-41ae-b1ea-050f2a88cb4c)
![3](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/0fddfe3e-503b-427d-ba8d-c189dff2bfe9)
![4](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/94797d7a-94a2-4f41-b771-a6c10fe35c77)
![5](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/885e838b-2752-419e-8b03-91aafa18a43d)
![6](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/8f7a6cef-1de6-464e-863b-086ae215aec4)
![7](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/2f8c987b-c8d8-4aa7-b7f8-5c9ce8e1a9a4)
![8](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/2d58dfcf-c2d9-4836-9e7a-d82fba03929c)
- SuperStore.csv:

```Python
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
df=pd.read_csv('SuperStore.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
df['Postal Code']=df['Postal Code'].fillna(method='ffill')
sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x="Postal Code",data=df)
```
- Output(SuperStore.csv) :
![1 1](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/2e0a334e-65d2-4415-9f9b-dc7c9033fc30)
![1 2](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/ab730fd1-2d37-4936-a16d-6dd4142ccbc4)
![1 3'](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/4c3c8ed2-d67b-42d0-aaeb-7521225c05b0)
![1 4](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/3aad2042-88a0-4047-8a3b-3af61012ccd5)
![1 5](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/2affa64d-448f-4755-a2d5-46a99318bd38)
![1 6](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/5bcb0d34-4caf-4cfc-8ba1-7e6dcd0a6efa)
![1 7](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/4a747a26-9f2e-47d6-8041-19a770a05ed9)
![1 8](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/c5e8519c-e7b2-4962-83ee-6cc1481c9e47)
- employeesal.csv:
```Python
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
df=pd.read_csv('employeesal.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x='Experience_Years',data=df)
sns.countplot(x="Experience_Years",data=df)
sns.distplot(df['Experience_Years'])
sns.histplot(x="Experience_Years",data=df)
```
- Output(employeesal.csv) :
![2 1](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/827bb379-f853-4063-b1c1-5023b47267b0)
![2 2](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/4e00764d-90ba-48fd-bcfe-a8a2ed46ff54)
![2 3](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/81137f5d-77ab-4ba5-8a12-8b8fc5ce4c0a)
![2 4](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/d4a563dd-1a9b-45db-9eb6-775abe492195)
![2 5](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/cc0374f6-28b6-40ed-8607-f0339d71f495)
![2 6](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/c6398558-1410-4b79-bee8-214e40be2b93)
![2 7](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/0b311056-4393-416b-b365-7127ab3fc824)
![2 8](https://github.com/Aakash0407/ODD2023-DataScience-Ex-03/assets/118799103/54ea4074-8cc5-4167-905a-dd63f131fe57)
## Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.
