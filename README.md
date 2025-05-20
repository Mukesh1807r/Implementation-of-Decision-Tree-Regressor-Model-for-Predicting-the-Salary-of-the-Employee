# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1. Import the standard libraries.

2. Upload the dataset and check for any null values using .isnull() function.

3. Import LabelEncoder and encode the dataset.

4. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5. Predict the values of arrays.

6. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7. Predict the values of array.

8. Apply to new unknown values.

## Program:
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: Mukesh R

RegisterNumber: 212224240098
```python
import pandas as pd


data = pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()

x = data[["Position", "Level"]]
y = data["Salary"]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse

r2 = metrics.r2_score(y_test, y_pred)
r2

dt.predict([[5,6]])
```

## Output:
![image](https://github.com/user-attachments/assets/5d7d6a29-b1ee-4b0a-be75-a01bbaa251d2)

![image](https://github.com/user-attachments/assets/c6688d3f-f30b-4187-9932-bee5d258aa4f)

![image](https://github.com/user-attachments/assets/16180c32-db55-4c51-8993-7c456b3c93ae)

![image](https://github.com/user-attachments/assets/e9133439-f592-4ffa-93e6-e2eb0da455a7)

![image](https://github.com/user-attachments/assets/1a4bd3ae-ce3a-4011-bf1a-87913ec6b7bc)

![image](https://github.com/user-attachments/assets/6c2dcc87-32bb-4ae6-8409-44b75ceab10f)

![image](https://github.com/user-attachments/assets/bc481464-33fd-4c01-8842-10c6e49e3c4f)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
