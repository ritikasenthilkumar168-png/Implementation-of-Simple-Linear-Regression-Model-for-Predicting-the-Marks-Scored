# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1. Import required libraries and load input data (hours studied and marks).
2. Create a Linear Regression model and train it using the dataset.
3. Obtain slope and intercept, then predict marks for given input.
4. Plot actual data points and regression line to visualize the result.
 

## Program:
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Sample data

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

# Create model
model = LinearRegression()

# Train model
model.fit(X, Y)

# Get slope and intercept
m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)

# ---- Prediction ----
x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

# ---- Plot ----
Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()

Developed by: Ritika S
RegisterNumber:  212225220086
*/
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
<img width="828" height="743" alt="Screenshot 2026-04-21 225943" src="https://github.com/user-attachments/assets/b642d130-1d22-459e-8571-a13bd1d2f073" />
<img width="857" height="746" alt="Screenshot 2026-04-21 230004" src="https://github.com/user-attachments/assets/239c4a9b-5c01-495e-b967-b8a7a7302ca9" />




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
