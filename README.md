# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
~~~
1.Import pandas
2.Import Decision tree regressor
3.Fit the data in the model
4.Find the accuracy score
~~~

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Mourya .G
RegisterNumber:  212224230170
*/
```
~~~
import pandas as pd
df=pd.read_csv("/content/Salary.csv")
df.head()
df.info()
df.isnull().sum()
import pandas as pd
df=pd.read_csv("/content/Salary.csv")
df.head()
df.info()
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["Position"]=le.fit_transform(df["Position"])
df.head()
x=df[['Position','Level']]
x.head()
y=df['Salary']
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
~~~

## Output:
![436161953-644df758-f1a5-4448-90cf-94d9c6aef823](https://github.com/user-attachments/assets/8693b65c-0db8-47ea-ad19-fc2b20e45f8f)
![436162042-e6e61d23-58fc-4dd4-8df3-3f2fe6b09290](https://github.com/user-attachments/assets/88664e73-e010-4630-8808-a7cdecd807b5)
![436162132-01350199-bcd2-4cae-858a-8f7c09ec38c8](https://github.com/user-attachments/assets/80caf92f-ee6a-4b58-bca7-40f6669f9d2f)
![436162230-67a785ab-424d-466d-aa97-fb51470afd8a](https://github.com/user-attachments/assets/f55d8f0e-af9a-45d8-a59e-c0ddac808c00)
![436162341-40507576-4984-481e-8c79-75c34130e50a](https://github.com/user-attachments/assets/02fb5466-266b-45e6-a155-0cac4db047ab)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
