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
import numpy as np
import matplotlib.pyplot as plt


X= np.array([1, 2, 3, 4, 5])
Y= np.array([20, 40, 50, 65, 80])


plt.scatter(X, Y, color='blue', label="Data Points")
plt.show()
```

```
plt.scatter(X, Y, color='blue', label="Data Points")
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2

m=num/den
b=Y_Mean-(m*X_Mean)

y_pred =(m*X)+b

plt.plot(X, y_pred, color='red', label=f"y = {m}x + {c}")
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.legend()
plt.show()



```
## Output
<img width="1855" height="852" alt="image" src="https://github.com/user-attachments/assets/aa1e3a49-f22d-49a2-97b0-2d6d86ab72d3" />
<img width="1780" height="947" alt="image" src="https://github.com/user-attachments/assets/b19bc67a-b305-4ecd-b64c-e16d1a8e5237" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
