# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import the NumPy library using the statement import numpy as np.
2. Define the given matrix A
3. Compute the Gaussian Elimination using np.linalg.inv()
4. print and end the program

## Program:
```
'''program to solve a matrix using Gaussian elimination without partial pivoting.
 Develeped by : K.Deekshitha
 RegisterNumber:2305002005
 '''
 
 import numpy as np
 import sys
 n=int(input())
 #making numpy array of n x n+1 size and initializing
 #to zero for storing augmented matrix
 a=np.zeros((n,n+1))
 #making numpy array ofn size and initializing
 x=np.zeros(n)
 for i in range(n):
 for j in range(n+1):
 a[i][j]=float(input())
 #Applying Gauss Elimination
 for i in range(n):
  for j in range(i+1, n):
 ratio=a[j][i]/a[i][i]
 for k in range(n+1):
 a[j][k]=a[j][k]-ratio*a[i][k]
 #Back substitution
 x[n-1]=a[n-1][n]/a[n-1][n-1]
 for i in range(n-2,-1,-1):
 x[i]=a[i][n]
 for j in range(i+1,n):
 x[i]=x[i]-a[i][j]*x[j]
 x[i]=x[i]/a[i][i]
 for i in range(n):
 print('X%d= %0.2f'%(i,x[i]),end=' ')
```
 

## Output:
![image](https://github.com/kilarideekshi/Gaussian/assets/155507099/000ddf54-b641-48ba-82bf-7cf328930c25)
![image](https://github.com/kilarideekshi/Gaussian/assets/155507099/926e2783-66d4-41dd-8871-4f157dc7f7e5)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

