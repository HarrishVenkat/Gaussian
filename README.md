# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy and sys
2. get the input as 'n'
3. solve a matrix using guassian elimination method without partial pivoting
4. produce the output

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Harrish Venkat V
RegisterNumber: 23013973
'''
import sys
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
X=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][i]==0.0:
        sys.exit("Divide by zero error")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
X[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i]=matrix[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-matrix[i][j]*X[j]
    X[i]=X[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,X[i]),end=' ')
*/
```

## Output:
![image](https://github.com/HarrishVenkat/Gaussian/assets/144979588/245ecc3e-066e-470d-813d-dc5dbadf4b16)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

