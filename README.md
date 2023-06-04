# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. Import pandas library to read csv or excel file.
2.Import LabelEncoder using sklearn.preprocessing library.
3.Transform the data's using LabelEncoder.
4.Import decision tree classifier from sklearn.tree library to predict the values.
5.Find accuracy.
6.Predict the values.
7.End of the program.
```

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: G R PRASANNA 
RegisterNumber:  212221040129
*/
```

```
import pandas as pd
data=pd.read_csv("Employee.csv")
print("data.head()")
data.head()

print("data.info()")
data.info()

print("isnull() and sum()")
data.isnull().sum()

print("data value counts()")
data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

print("data.head() for salary")
data["salary"]=le.fit_transform(data["salary"])
data.head()

x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()

y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("Accuracy value")
accuracy

print("data.prediction")
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

```
## Output:


![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/958cbec4-4002-460d-8eeb-baffd7324071)

![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/ec41ff4a-bd88-4d4f-bf88-8c6c454216ad)


![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/81025151-7460-4660-99ec-acf63a05a3fd)



![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/dd4cde60-d662-4af5-90fe-6ae23a5d19a8)


![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/57e80db7-be41-4536-ae75-5a7682768d52)


![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/5a70094e-c2d9-46f2-8196-79e4d7d53ac0)

![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/6cdf663d-bd24-4b30-b981-214d24c08a8d)

![image](https://github.com/KARTHICKRAJM84/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/128134963/25c7046b-0a8d-49e7-afad-22f494c64043)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
