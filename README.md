# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program for univariate linear regression
#Developer: GOKHULRAJ V
#Registraion number: 212223230064
import numpy as np
import matplotlib.pyplot as plt
X = np.array(eval(input()))
Y = np.array(eval(input()))
Xmean = np.mean(X)
Ymean = np.mean(Y)
num, den = 0, 0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
print(m, c)
Y_pred = m*X+c
print(Y_pred)
plt.scatter(X, Y)
plt.plot(X, Y_pred, color="red")
plt.show()

```
## Output
![Screenshot 2023-12-27 121333](https://github.com/Gokhulraj2005/Univariate-Linear-Regression/assets/138849253/65accc67-b74e-40bc-a7e7-47dc2b39b000)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
