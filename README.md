# Implementation of Univariate Linear Regression
### AIM:  
To implement univariate Linear Regression to fit a straight line using least squares. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**DATE:**
### Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook
### Algorithm:
<table>
<tr>
<td width=70%>

1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.
4. Compute the y -intercept of the line by using the formula.
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

</td> 
<td>

<img alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png"> <br>
<img height=80% width=60% alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
</td>
</tr> 
</table>



<table>
<tr>
<td valign='top'>

### Program:
```Python
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
Nume,Deno=0,0
for i in range(len(X)):
    Nume+=(X[i]-Xmean)*(Y[i]-Ymean)
    Deno+=(X[i]-Xmean)**2
M=Nume/Deno
C=Ymean-(M*Xmean)
print("Slope : ",M)
print("Y-intercept: ",C)
Ypred=(M*X)+C
print("Predicted Values:",Ypred)
plt.scatter(X,Y)
plt.plot(X,Ypred,color='Red')
plt.title("Univariate Linear Regression")
plt.xlabel("X values")
plt.ylabel("Y values")
plt.show()
```
<br>

Developed By: **Thirukaalathessvarar S** <br>
Register No: **212222230161**
</td> 
<td>
  
### Output:
[8,2,11,6,5,4,12,9,6,1]  
[3,10,3,6,8,12,1,4,9,14]    
Slope :  -1.1064189189189189      
Y-intercept:  14.08108108108108  
Predicted Values: [ 5.22972973 11.86824324  1.91047297  7.44256757  8.54898649  9.65540541
  0.80405405  4.12331081  7.44256757 12.97466216]  
  
![download](https://github.com/ROHITJAIND/EX-01-BestFitLine-using-LeastSquaresMethod/assets/118707073/70dcf735-82d9-4e80-a548-981286ae8ccd)

</td>
</tr> 
</table>

### Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
