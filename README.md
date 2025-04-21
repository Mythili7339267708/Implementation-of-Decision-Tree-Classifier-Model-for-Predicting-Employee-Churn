# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn
## NAME: V MYTHILI
## REG NO: 212223040123

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import Libraries and Load Dataset.
2. Preprocess the Data.
3. Split the Dataset.
4. Train the Decision Tree Classifier.
5. Make Predictions and Evaluate the Model
 

## Program:
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: v mythili
RegisterNumber:  212223040123


```
import pandas as pd
data=pd.read_csv("Employee.csv")
data

```
```
data["left"].value_counts()
```

```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
```
```
data.head()
```
```
data["salary"]=le.fit_transform(data["salary"])
data
```
```
x=data[["satisfaction_level","last_evaluation","number_project","time_spend_company"]]
x.head()
```
```
y=data["left"]
```

```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
```

```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
```

```
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

```

```
dt.predict([[0.5,0.8,2,9]])
```
## Output:

![image](https://github.com/user-attachments/assets/15cf96a2-4951-4d64-8e66-fe0dc78382fe)


![image](https://github.com/user-attachments/assets/8afe4c67-f657-4406-82bd-8488d9aff4d8)


![image](https://github.com/user-attachments/assets/06827b40-31a0-47d5-8ed8-e8a9dd667135)


![image](https://github.com/user-attachments/assets/662c9aec-f1ed-476e-aae2-2aae0bb6a40b)


![image](https://github.com/user-attachments/assets/c78451d4-11b3-474f-a41b-f7e224254d46)

![image](https://github.com/user-attachments/assets/fde7e99a-00bc-49f2-81fd-5c4d74ee56cd)


![image](https://github.com/user-attachments/assets/9ba6c79b-6349-47b1-9bb9-14cc3e36d650)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
