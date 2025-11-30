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
# To check linearly independent or linearly dependent

  import numpy as np
  from sympy import Matrix

  print("Linear Dependence check")
  v1 = [1,0,0]
  v2 = [0,1,1]
  v3 = [1,0,1]
  v_ind = Matrix([v1,v2,v3]).transpose()
  rank_ind = v_ind.rank()
  print(f"Vectors:[v1],[v2],[v3]")
  print(f"matrix:\n[v_ind")
  print(f"rank: (r_ind), Number of Vectors: 3")
  if rank_ind == 3:
      print("result: the vector are linearly INDEPENDENT.\n")
  else:
      print("Result: The vectors are linearly DEPENDENT.\n")

  
  v4 = [1,2,3]
  v5 = [4,5,6]
  v6 = [5,7,9]
  v_dep = Matrix([v4,v5,v6]).transpose()
  rank_dep = v_dep.rank()

  print(f"Vectors: [v4],[v5],[v6]")
  print(f"Matrix:\n[v_dep")
  print(f"rank[rank_dep),Number of Vector: 3")
  if rank_dep == 3:
      print("result: The vectors are linearly INDEPENDENT./n")
  else:
      print("Result: The vectors are linearly DEPENDENT.\n")
