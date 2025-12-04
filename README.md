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

## Program and Output:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Moid Vanak
RegisterNumber: 212223080033
```
```
import numpy as np
import matplotlib.pyplot as plt

X=np.array(eval(input()))
Y=np.array(eval(input()))
```
![image](https://github.com/user-attachments/assets/9895adcf-9e95-4dfa-829d-5d8d7f8208a5)
```
X_mean = np.mean(X)
Y_mean = np.mean(Y)
num = 0
denom = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    denom += (X[i] - X_mean)**2
X_mean,Y_mean
```
![image](https://github.com/user-attachments/assets/c0e94adb-fa50-48c5-8106-a4b2fa215917)
```
m = num / denom
b = Y_mean - m * X_mean

print(m, b)
y_predicted = m * X + b
print(y_predicted)
```
![image](https://github.com/user-attachments/assets/b79fb35b-c130-48ca-b24c-56f9e60af9d3)
```
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```
![image](https://github.com/user-attachments/assets/42e844f6-c9a3-4d66-b459-8b0bffb0e985)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
