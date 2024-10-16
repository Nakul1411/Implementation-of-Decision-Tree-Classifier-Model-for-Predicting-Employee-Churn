# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas module and import the required data set.
2. Find the null values and count them .
3. count numbers of left values.
4. From sklearn import LabelEncoder to convert string values to numerical values.
5. From sklearn.model_selection import train_test_split.
6. Assign the train dataset and test dataset.
7. From sklearn.tree import Decision Tree Classifier.
8. Use criteria as entropy.
9. From sklearn import metrics.
10. Find the accuracy of our model and predict the required values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: NAKUL R
RegisterNumber: 212223240102
*/
```
import pandas as pd 
data=pd.read_csv("/content/Employee.csv")
data.head()
![Screenshot 2024-10-16 142841](https://github.com/user-attachments/assets/8c557537-5c41-42ce-8eba-d1d30931b1b2)
data.info()
![Screenshot 2024-10-16 143002](https://github.com/user-attachments/assets/ce1895ce-14fb-4038-a788-52786196be6f)
data.isnull().sum()
![Screenshot 2024-10-16 143109](https://github.com/user-attachments/assets/f70b3d97-ede0-40b0-8364-f44dd235cfe5)
data["left"].value_counts()
![Screenshot 2024-10-16 143217](https://github.com/user-attachments/assets/98efdcbd-f54a-414e-addd-6d1cad797c44)
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
![Screenshot 2024-10-16 143454](https://github.com/user-attachments/assets/94462e65-f9db-414d-b9c1-f4c672250648)
x=data[["satisfaction_level","last_evaluation","number_project"
x.head()
![Screenshot 2024-10-16 143646](https://github.com/user-attachments/assets/51ddbdd6-54e5-49a5-a7b3-941e89f4a623)
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

## Output:
![decision tree classifier model](sam.png)
![Screenshot 2024-10-16 143738](https://github.com/user-attachments/assets/5fb3e555-e24a-48c6-bafb-ccdda706f385)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
