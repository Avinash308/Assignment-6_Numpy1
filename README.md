# Assignment-6_Numpy1

# problem statement Write a function so that the columns of the output matrix are powers of the input vector.
# The order of the powers is determined by the increasing boolean argument. Specifically,
# when increasing is False, the i-th output column is the input vector raised element-wise
# to the power of N - i - 1.

import numpy as np
x = np.array([1, 2, 3, 5])
N = 3
np.vander(x, N)
np.column_stack([x**(N-1-i) for i in range(N)])
x = np.array([1, 2, 3, 5])
print(np.vander(x))
print(np.linalg.det(np.vander(x)))
