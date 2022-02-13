# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## EQUIPMENT'S REQUIRED:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## ALGORITHM:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.

## PROGRAM:
```
Program for Univariate linear regression using the least squares method.
Developed by: Aashima Nazreen Sayeed S
RegisterNumber: 21500368

import numpy as np
import matplotlib.pyplot as plt

X = np.array(eval(input()))
Y = np.array(eval(input()))

Xmean = np.mean(X)
Ymean = np.mean(Y)
num,den = 0,0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
    
print (m, c)

Y_pred = m*X + c
print (Y_pred)

plt.scatter(X,Y)
plt.plot(X,Y_pred,color="purple")
plt.show()
```
## SAMPLE INPUT AND OUTPUT:

### Input:
![inp](./input.jpg)

### Output:
![output](https://user-images.githubusercontent.com/93427086/151491200-f2cf27af-f6e9-447d-b9e2-d28092266b50.png)

## RESULT:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
