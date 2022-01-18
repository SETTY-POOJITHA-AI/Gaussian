# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Define a function. 

2.Get the numbers from the user. 

3.Compare the values,to find the solution.

4.Use for() and if() loop to find the guassian elimination of the matrix.
 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by:poojithasetty 
RegisterNumber: 21003760
*/
import numpy as np
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0:
        sys.exit('Divide by zero detected')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
#Back Substitution
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
#Displaying Solution
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
```

## Output:
![gaussian elimination](https://github.com/SETTY-POOJITHA-AI/Gaussian/blob/b4600125b20a6ee6f3f5331c53c31407a4c0e266/settygaussian.PNG)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

