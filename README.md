# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2.For gaussian elimination method, we want to make 2nd and 3rd column zero.
3.For that we want to make a range accorting to our program output.
4.Then print the program with correct form then the output will display.

## Program:
      '''Program to solve a matrix using Gaussian elimination without partial pivoting.
      Developed by: SIBHIRAAJ R
      RegisterNumber: 24010177
      '''
      import numpy as np
      n=int(input())
      matrix=np.zeros((n,n+1))
      x=np.zeros(n)
      for i in range(n):
          for j in range(n+1):
              matrix[i][j]=int(input())
      for i in range(n):
          for j in range(i+1,n):
              ratio=matrix[j][i]/matrix[i][i]
              for k in range(n+1):
                  matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
      x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
      for i in range(n-2,-1,-1):
          x[i]=matrix[i][n]
          for j in range(i+1,n):
              x[i]=x[i]-matrix[i][j]*x[j]
          x[i]=x[i]/matrix[i][i]
      for i in range(n):
          print("X%d = %0.2f" %(i,x[i]),end = " ")


## Output:
![Screenshot 2024-12-01 185803](https://github.com/user-attachments/assets/d954682b-2a7b-45b4-904e-0dd6d20b52cf)
![Screenshot 2024-12-01 185811](https://github.com/user-attachments/assets/da5c5d6e-752c-42fc-bf77-bbae031b62b3)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

