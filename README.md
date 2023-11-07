# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages.
2. Read the given csv file and display the few contents of the data.
3. Assign the features for x and y respectively.
4. Split the x and y sets into train and test sets.
5. Convert the Alphabetical data to numeric using CountVectorizer.
6. Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.
7. Find the accuracy of the model.


## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Srihariharan S A
RegisterNumber: 212221040160


import chardet
file='/content/spam (1).csv'
with open(file, 'rb') as rawdata:
     print('Result output')
    result = chardet.detect(rawdata.read(10000))
result

import pandas as pd
data=pd.read_csv("/content/spam (1).csv",encoding="windows-1252")

print("Data Head ")
data.head()

print("data info")
data.info()

print("data.isnull()")
data.isnull().sum()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)


from sklearn.feature_extraction.text import CountVectorizer 
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)

y_pred=svc.predict(x_test)
print("y_pred")
y_pred


from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("accuracy")
accuracy


*/
```

## Output:

1. Encoding
   
![Encoding](https://github.com/AaronDominic/Implementation-of-SVM-For-Spam-Mail-Detection/assets/143015231/85dd4436-3ac2-4fea-9d04-1746dd37e11a)

2. Head
   
![2  Head](https://github.com/AaronDominic/Implementation-of-SVM-For-Spam-Mail-Detection/assets/143015231/0b7810a2-ec3f-481e-8999-c5acca62dc90)

3. Info
   
![3  info](https://github.com/AaronDominic/Implementation-of-SVM-For-Spam-Mail-Detection/assets/143015231/a826fe10-0552-4066-b0d3-e46c6349ba9c)

4. Isnull.sum
   
![4  isnull sum()](https://github.com/AaronDominic/Implementation-of-SVM-For-Spam-Mail-Detection/assets/143015231/853cdd43-98f0-4ff5-97d9-2f9fa0d63317)

5. y_pred
   
![5  y_pred](https://github.com/AaronDominic/Implementation-of-SVM-For-Spam-Mail-Detection/assets/143015231/0aebfd66-7522-46e0-9cd2-2cd2bb86dd9e)

6. Accuracy
   
![6  Accuracy](https://github.com/AaronDominic/Implementation-of-SVM-For-Spam-Mail-Detection/assets/143015231/294c1e87-33f3-44b2-86a4-0f16437d55fa)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
