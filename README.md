# EX1 Implementation of Univariate Linear Regression to fit a straight line using Least Squares
## DATE:
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
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: YOGAVARMA B
RegisterNumber: 2305002029
```

```
import numpy as np
import matplotlib.pyplot as plt
x=np.array([2,9,5,5,3,7,1,8,6,2])
y=np.array([69,98,82,77,71,84,55,94,84,64])
XMEAN=np.mean(x)
YMEAN=np.mean(y)
num,den=0,0
for i in range(len(x)):
  num+=(x[i]-XMEAN)*(y[i]-YMEAN)
  den+=(x[i]-XMEAN)**2
m=num/den
c=YMEAN-m*XMEAN
print(m,c)
Y_pred=m*x+c
print(Y_pred)
plt.scatter(x,y)
plt.plot(x,Y_pred,color='red')
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/7475d611-d1db-4030-b330-3ac14282705e)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
