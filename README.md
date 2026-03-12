# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
import pandas as pd.

### Step2
Read the csv file.

### Step3
Get the value of X and y variables

### Step4
Create the linear regression model and fit.

### Step5
Predict the CO2 emission of a car where the weight is 2300kg, and the volume is 1300cm cube.

## Program:
```
Developed by:Geetha shri.G
Register number:212225220032
import matplotlib.pyplot as plt
import numpy as np
from sklearn import datasets,linear_model,metrics
from sklearn.datasets import fetch_california_housing

california=fetch_california_housing()
x=california.data
y=california.target

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.4,random_state=1 )

reg=linear_model.LinearRegression()
reg.fit(x_train,y_train)
print('coefficients',reg.coef_)  
print("\n")
print('Variance score:{}'.format(reg.score(x_test,y_test)))
print("\n")
plt.style.use('fivethirtyeight')
plt.scatter(reg.predict(x_train),reg.predict(x_train)-y_train,color='green',s=10,label='Train data')
plt.scatter(reg.predict(x_test),reg.predict(x_test)-y_test,color='blue',s=10,label='Test data')
plt.hlines(y=0,xmin=0,xmax=50,linewidth=2)
plt.legend(loc='upper right')
plt.title('Residual errors')
plt.show()





```
## Output:
<img width="1011" height="599" alt="Screenshot 2026-03-12 142220" src="https://github.com/user-attachments/assets/bc4a2081-46a3-47b8-8d20-8e46dbf439e7" />
<img width="874" height="680" alt="Screenshot 2026-03-12 142244" src="https://github.com/user-attachments/assets/74701363-dbcb-4d17-9640-50215d437791" />



<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
