# Ex03-Univariate-Analysis

## AIM:
To read the given data and perform the univariate analysis with different types of plots.

## EXPLAINATION:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

## ALGORITHM:

Step1:Read the given data set  using standard libraries.

Step2:Get the information about the data.

Step3:Remove the null values from the data.

Step4:Mention the datatypes from the data.

Step5:Count the values from the data.

Step6:Do plots like sepallength,species,sepalwidth.

## PROGRAM:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/iris.csv")

df.head()

df.tail()

df.nunique()

df.iloc[:,4].value_counts()

for i in range(0,df.shape[1]):
  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")

sns.countplot(x='species',data=df)

dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
##plt.plot(df_setosa['sepal_length'],np.zeros_like(df_setosa['sepal_length']),'o')

dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_width","sepal_width").add_legend();
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_length","sepal_length").add_legend();
plt.show()

sns.pairplot(df,hue="species",size=3)

```

## OUPTUT:

![image](https://github.com/Anuayshh/expt3/assets/127651217/24f72aa6-30d5-4730-ad1b-b3e346c61d87)

![image](https://github.com/Anuayshh/expt3/assets/127651217/7840530c-6bd5-40a0-b412-b76c61fd437d)


![image](https://github.com/Anuayshh/expt3/assets/127651217/d6431996-e619-4b6a-bcd0-583abce52c4f)


![image](https://github.com/Anuayshh/expt3/assets/127651217/8ee531b2-e299-4a12-af85-8af757122b37)

![image](https://github.com/Anuayshh/expt3/assets/127651217/c4d3d1ac-0fcb-4ca6-b7db-6e6401ff89cd)


![image](https://github.com/Anuayshh/expt3/assets/127651217/629e6f67-5d59-4452-b1ad-bf4d78920035)


![image](https://github.com/Anuayshh/expt3/assets/127651217/1a06bd6c-1c97-49f8-a58a-d3165cc5709b)


![image](https://github.com/Anuayshh/expt3/assets/127651217/0a2acb0d-3c1f-45d7-9a2d-4b6b8108f32a)


![image](https://github.com/Anuayshh/expt3/assets/127651217/1eefb090-94ca-4f66-be37-12f9e0d588b9)

![image](https://github.com/Anuayshh/expt3/assets/127651217/89d52162-4154-4177-9d70-1a0d75ad9ca9)

![image](https://github.com/Anuayshh/expt3/assets/127651217/2af23bbc-8fab-4f8b-8087-8edf19b4bd7a)


## RESULT:
Thus we have read the given data and performed the univariate analysis with different types of plots are created and verified successfully.
