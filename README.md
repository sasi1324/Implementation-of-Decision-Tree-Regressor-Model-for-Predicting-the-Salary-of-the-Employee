# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. Import the standard libraries.
2. Upload the dataset and check for any null values using .isnull() function.
3. Import LabelEncoder and encode the dataset.
4. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.
5. Predict the values of arrays.
6. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.
7. Predict the values of array.
8. Apply to new unknown values.
```

## Program:
```
Developed by: Tamil Pavalan M
RegisterNumber:  212223110058
```
```
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
![image](https://github.com/user-attachments/assets/3b23da30-64f1-4cbf-a4da-9984f0b8b47f)

![image](https://github.com/user-attachments/assets/7f29c9d2-1972-4541-a332-22e056f32fed)

![image](https://github.com/user-attachments/assets/84dad02e-0f66-4313-9f3b-0f839a4ec326)

![image](https://github.com/user-attachments/assets/3dd9edce-851d-4486-8a7e-e360a092b9b2)

![image](https://github.com/user-attachments/assets/7278ea6e-f674-43a9-b04b-3c8998ecf5f4)

![image](https://github.com/user-attachments/assets/19228555-0162-4c2a-a644-c1253e96efc0)

![image](https://github.com/user-attachments/assets/5e162e99-069d-455a-86e7-b2f8d17ba11e)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
