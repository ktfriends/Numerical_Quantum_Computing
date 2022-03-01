# Effective QUBO modeling for solving linear systems
```
Solving linear system: Ax = b
We make several QUBO models for matrices and compare the results.
From the results, we propose a new method for constrained problems.
```
## Example 1
```
Matrix A:    Vector b:
[[ 3  1]     [-1  5]
 [-1  2]]
Related files: Q1 to Q4
```
## QUBO Model 2
```
     Matrix A:                  Vector b:
[[ 3   8   1   2]        [-265  1177  1162  -164]
 [ 3  -2   5   4]
 [ 4  -3   7   0]          Translation vector T:
 [ 4   2  -2   0]]         [48  -96   96   80]
Related files: Subrange_1 to 4
```
