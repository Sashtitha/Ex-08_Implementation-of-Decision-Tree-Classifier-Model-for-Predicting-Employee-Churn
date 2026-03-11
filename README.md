# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: SASHTITHA K
RegisterNumber:  212225230253



import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
data = pd.read_csv("Employee.csv")

print("data.head():")
print(data.head())

print("\ndata.info():")
print(data.info())

print("\nMissing values:")
print(data.isnull().sum())

print("\nValue counts of left:")
print(data["left"].value_counts())

# Encode salary column
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["salary"] = le.fit_transform(data["salary"])

print("\nEncoded Salary Column:")
print(data.head())

# Feature selection
X = data[["satisfaction_level",
          "last_evaluation",
          "number_project",
          "average_montly_hours",
          "time_spend_company",
          "Work_accident",
          "promotion_last_5years",
          "salary"]]

print("\nFeatures:")
print(X.head())

# Target variable
y = data["left"]

# Train test split
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=100)

# Decision Tree Model
from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(X_train, y_train)

# Prediction
y_pred = dt.predict(X_test)

# Accuracy
from sklearn.metrics import accuracy_score
accuracy = accuracy_score(y_test, y_pred)

print("\nAccuracy value:", accuracy)

# Example Prediction
print("\nData Prediction:")
prediction = dt.predict([[0.5, 0.8, 9, 260, 6, 0, 1, 2]])
print(prediction)

# Decision Tree Visualization
from sklearn.tree import plot_tree

plt.figure(figsize=(12,8))
plot_tree(dt,
          feature_names=X.columns,
          class_names=['Stay','Left'],
          filled=True)

plt.show()


*/
```

## Output:
![alt text](<image copy 3.png>)
![alt text](info.jpg)
![alt text](<image copy 2.png>)
![alt text](<image copy.png>)
![alt text](image.png)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
