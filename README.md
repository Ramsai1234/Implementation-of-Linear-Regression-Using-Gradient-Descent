# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to implement the linear regression using gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
~~~
##step1
Use the standard libraries in python for Gradient Design.

##step2
Upload the dataset and check any null value using .isnull() function.

##step3
Declare the default values for linear regression.

##step4
Calculate the loss usinng Mean Square Error.

##step5
Predict the value of y.

##step6
Plot the graph respect to hours and scores using scatter plot function.

##step7
End the program
~~~

## Program:
```
~~~
Program to implement the linear regression using gradient descent.
Developed by:P.RAMSAI 
RegisterNumber:212221240041
~~~
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("student_scores.csv")
data.head()
data.isnull().sum()
X=data.Hours
X.head()
Y=data.Scores
Y.head()
X_mean=np.mean(X)
Y_mean=np.mean(Y)
n=len(X)
num=0
den=0
Loss=[]
for i in range(len(X)):
    MSE=(1/n)*((Y_mean-Y[i])**2)
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    den+=(X[i]-X_mean)**2
    Loss.append(MSE)
m=num/den
c=Y_mean-(m*X_mean)
print (m, c)
Y_pred=(m*X)+c
print (Y_pred)
plt.scatter(X,Y,color='pink')
plt.plot(X,Y_pred,color='blue')
plt.show()
```

## Output:
![GitHub Logo](/ml1/png)

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
