
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
