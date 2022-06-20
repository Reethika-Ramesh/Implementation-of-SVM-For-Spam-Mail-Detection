# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the necessary packages using import statement.
2.Read the given csv file and print the number of contents to be displayed.
3.Split the dataset using train_test_split.
4.Calculate Y_Pred and accuracy.
5.Display the result. 

## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: REETHIKA.R
RegisterNumber:  212219220042

import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["EmailText"].values
y=data["Label"].values
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
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

```

## Output:

## Data.head():

![image](https://user-images.githubusercontent.com/98681990/174660497-82d7f30e-c8da-423f-b298-6e3208a42595.png)

## Data.info():

![image](https://user-images.githubusercontent.com/98681990/174660571-71df2803-7e89-41d8-93b8-b6862a12eee4.png)

## Data.isnull().sum():

![image](https://user-images.githubusercontent.com/98681990/174660705-cc2eb579-3bab-4238-957c-6057094fc173.png)

## Y_Pred:

![image](https://user-images.githubusercontent.com/98681990/174660743-c5f26956-4a00-40c8-8e65-a81f579dec6b.png)


## Accuracy:

![image](https://user-images.githubusercontent.com/98681990/174660764-eecc1fce-2712-48c1-a8c8-7a83280e987c.png)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
