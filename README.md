# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by:Pradeep.M 
RegisterNumber: 212225220071 
*/
import numpy as np
import matplotlib.pyplot as plt
X=np.array([1,2,3,4,5])
Y=np.array([2,3,4,5,6])
x_m=np.mean(X)
y_m=np.mean(Y)
nu=np.sum((X-x_m)*(Y-y_m))
de=np.sum((X-x_m)**2)
m=nu/de
b=y_m-m*x_m
print("Slope:",m)
print("Intercept:",b)
y_p=m*X+b
plt.scatter(X, Y, label='Data Points')
plt.plot(X, y_p,label='Regression Line')
plt.title("Linear Regression")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.show()
```

## Output:
<img width="762" height="514" alt="Screenshot 2026-08-20 210907" src="https://github.com/user-attachments/assets/e3981acc-2b3e-4019-9f32-78de474d1430" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
