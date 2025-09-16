Name : VISWAJITH LALITHRAM R.V

Reg.no : 212224240187

---

# EXNO2DS

---

# AIM:
  ---

To perform Exploratory Data Analysis on the given data set.

---

# EXPLANATION:
  -----------
  
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

---

# ALGORITHM:
  ---------
  
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

---

## CODING AND OUTPUT :
   -----------------

```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df
```

<img width="1312" height="590" alt="Screenshot 2025-09-15 113710" src="https://github.com/user-attachments/assets/294904d6-6458-40e0-a088-1693c81a00d8" />

```
df.info()
```

<img width="589" height="467" alt="Screenshot 2025-09-15 113807" src="https://github.com/user-attachments/assets/1c61ca6c-aa96-4943-b22c-2bfcba96aeb6" />

```
df.describe()
```

<img width="839" height="364" alt="Screenshot 2025-09-15 113852" src="https://github.com/user-attachments/assets/d9b2a648-445f-4789-93c9-fb33f42f5d6b" />

```
df.dtypes
```

<img width="353" height="341" alt="Screenshot 2025-09-15 113933" src="https://github.com/user-attachments/assets/c3612a8c-d288-4364-b59e-7577858feb6b" />

```
df.shape
```

<img width="202" height="88" alt="Screenshot 2025-09-15 114022" src="https://github.com/user-attachments/assets/2967ef3c-5bf5-4653-9a47-ef16639366cb" />

```
df.value_counts()
```

<img width="1346" height="594" alt="Screenshot 2025-09-15 114110" src="https://github.com/user-attachments/assets/a53037cc-1cdc-488e-a1f8-9ca231c49750" />

```
df['Age'].value_counts()
```

<img width="457" height="317" alt="Screenshot 2025-09-15 114143" src="https://github.com/user-attachments/assets/7e6a70fb-a572-4864-ac12-24330f72ff9b" />

```
df.set_index("PassengerId", inplace = True)
df
```

<img width="1281" height="551" alt="Screenshot 2025-09-15 114226" src="https://github.com/user-attachments/assets/fcd8215e-7913-4dba-912c-f28d2803eeb9" />

```
df.nunique()
```

<img width="254" height="312" alt="Screenshot 2025-09-15 114312" src="https://github.com/user-attachments/assets/f48f3c01-90e3-43e7-ba86-60666459a5d0" />

```
sns.countplot(data=df,x='Age')
```

<img width="816" height="618" alt="Screenshot 2025-09-15 114357" src="https://github.com/user-attachments/assets/8f6d923b-df34-44d0-8261-eb050b916cfd" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```

<img width="1297" height="549" alt="Screenshot 2025-09-15 114442" src="https://github.com/user-attachments/assets/317d09c9-d0c2-42c3-bb5c-daf68ca4b8e9" />

```
sns.catplot(x="Gender",col="Survived",kind="count",data=df)
```

<img width="1330" height="702" alt="Screenshot 2025-09-15 114525" src="https://github.com/user-attachments/assets/941fc8f1-a2b9-41d0-a826-c705f6f4e845" />

```
df.boxplot(column="Age",by="Survived")
```

<img width="801" height="662" alt="Screenshot 2025-09-15 114608" src="https://github.com/user-attachments/assets/f2ff64cd-93dc-4216-86be-40ca0b924388" />

```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```

<img width="835" height="622" alt="Screenshot 2025-09-15 114653" src="https://github.com/user-attachments/assets/efb2d221-36f8-4859-b06c-32ec622267d5" />


```
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
```

<img width="805" height="588" alt="Screenshot 2025-09-15 114838" src="https://github.com/user-attachments/assets/321a1c0c-5dcb-4c8a-851f-ebf9126833cd" />

```
sns.catplot(x='Pclass',y='Age',hue='Gender',col="Survived",kind="box",data=df)
```

<img width="1328" height="646" alt="Screenshot 2025-09-15 114922" src="https://github.com/user-attachments/assets/af8d4d40-461c-43d2-9ced-6f39d5d8b17a" />

```
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
```

<img width="772" height="640" alt="Screenshot 2025-09-15 115010" src="https://github.com/user-attachments/assets/47885f8b-15eb-4395-818f-cd0dca0a622d" />      

---

# RESULT :
  ------

 Performing Exploratory Data Analysis on the given data set was completed......
    
