# Math Practical

import numpy as np

matrix_X = np.array([[1,2,3],
                   [2,6,4],
                   [3,1,4]], dtype=float)  

print("coefficient of Matrix X is as follows:\n", matrix_X,'\n')
column_matrix = np.array([[8],
                          [-11],
                          [-3]],dtype = float)
print("Column Matrix (B) is as follows :", '\n', column_matrix, '\n')
solution_of_the_system_of_equations = np.linalg.solve(matrix_X,column_matrix)
print("Solution of the system of equations (X) using Gauss elimination method:")
print(solution_of_the_system_of_equations)
# column space and all

import numpy as np
from sympy import Matrix

A_X = np.array([[1,2,3],
                   [2,6,4],
                   [3,1,4]], dtype=float)  
A=Matrix(A_X)
print("Matrix(A) is as follows:",'\n',A,'\n')
print("NULL Space & nullity")
ns=A.nullspace()
print("Basis for Null space:",ns)
rank = A.rank()
print("Rank of A:",rank)
num_cols = A.shape[1]
nullity = num_cols - rank
print("Nullity of As:",nullity,'\n')
print("column space")
col_space = A.columnspace()
print("Basis for Column space :",col_space,'\n')
print("ROW SPACE")
row_space = A.rowspace()
print("Basis for Row space:", row_space, '\n')
print("LEFT NULL SPACE")
A_T = A.transpose()
print("Transpose of A(A^T)is:",'\n', A_T,'\n')
Left_ns = A_T.nullspace()
print("Basis for left null space:",Left_ns)
