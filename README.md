# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages and print the present data.
2. Print the placement data and salary data.
3. Find the null and duplicate values.
4. Using logistic regression find the predicted values of accuracy , confusion matrices.
5. Display the results.

## Program:
```
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Paul Samson.S
RegisterNumber: 212222230104
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score
from sklearn.metrics import confusion_matrix
from sklearn.metrics import classification_report
data=pd.read_csv('Placement_Data1.csv')
print(data.head())
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
print(data1.head())
print(data1.isnull().sum())
print(data1.duplicated().sum())
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
print(data1)
x=data1.iloc[:,:-1]
print(x)
y=data1["status"]
print(y)
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
print(y_pred)
accuracy=accuracy_score(y_test,y_pred)
print(accuracy)
confusion=(y_test,y_pred)
print(confusion)
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])
```

## Output:
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/ae7848d3-d7f6-4bee-8449-bb236ef7ab53)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/e5b072f9-2abb-427f-b3d7-114d410ca945)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/7bba24b8-4639-4732-b12c-070d0f36d06e)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/3298a7a1-5447-4673-b68c-ec84d1011486)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/36fe6ce3-ea53-492c-abdb-1242d82b00b7)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/8d8db01c-354a-40cd-8ed8-fb40a023eafd)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/a6884490-c3c0-4648-abcc-860499f9be45)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/7bdf306e-c668-4d9a-8ff2-8edf49b9983f)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/1215091c-5e46-4e2a-9464-41abb4db93f1)
![image](https://github.com/Gokkul-M/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144870543/95dc9125-43e8-4309-b9ea-9c2c121e13c0)


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
