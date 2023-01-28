# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Declare the variables and read the order of the matrix n.
2. Take the coefficients of the linear equations as: Do for k=1 to n. ...
3. Do for k=1 to n-1. Do for i=k+1 to nDo for j=k+1 to n+1. ...
4. Compute x[n]=a[n][n+1]/a[n][n]
5. Do for k=n-1 to 1. sum=0. ...
6. Display the result x[k]

## Program:
```py
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Arshatha P
RegisterNumber: 22009104
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
x[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range (n-2,-1,-1):
    x[i]=arr[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-arr[i][j]*x[j]
    x[i]=x[i]/arr[i][i]    
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output:
![gaussian elimination](/Screenshot%202023-01-28%20204636.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

