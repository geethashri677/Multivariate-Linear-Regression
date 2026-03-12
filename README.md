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
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("car.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
predictedCO2 = regr.predict(pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume']))
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)





```
## Output:
<img width="1011" height="599" alt="Screenshot 2026-03-12 142220" src="https://github.com/user-attachments/assets/bc4a2081-46a3-47b8-8d20-8e46dbf439e7" />
<img width="874" height="680" alt="Screenshot 2026-03-12 142244" src="https://github.com/user-attachments/assets/74701363-dbcb-4d17-9640-50215d437791" />



<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
