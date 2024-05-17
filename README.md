# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## 
STEP 1 STAR

STEP 2:Import the required packages.

STEP 3:Import the dataset to operate on.

STEP 4:Split the dataset.

STEP 5:Predict the required output.

STEP 6:End the program.

STEP 7 STOP       
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: MS Sanjay
RegisterNumber:212223040183
```
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
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
*/
```

## Output:
## Data Head:
![173077929-279a193a-55f7-4de7-b705-e7260abc5290](https://github.com/vksachin2018/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149366019/9dbbeb36-a1c6-40d2-ad75-ed4ada3dbbfd)

## Data Info:
![173077947-8ca5a120-b620-4691-8485-70c09b0e6255](https://github.com/vksachin2018/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149366019/f457e92d-7659-4524-9ef5-135ce18a3925)

## Data isnull():
![173077964-17c3b6d5-931d-4119-8c3e-48814bdfe88b](https://github.com/vksachin2018/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149366019/90a9d012-746a-4fa7-8031-8b870d745578)

## y_pred:
![173077974-78d5cb5d-6b93-4039-9dfe-34f08aee366b](https://github.com/vksachin2018/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149366019/48b9ee90-a32f-4b04-8882-a23ff0a44e6b)

## Accuracy:
![173077981-f93e4363-a74f-4488-80ec-c0142756fbe4](https://github.com/vksachin2018/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149366019/708231ab-89a8-404e-80cd-107e3ec69c68)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
