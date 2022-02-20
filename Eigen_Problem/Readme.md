# Eigenvalues and Eigenvectors
```
We are developing generator code optimized for D-Wave.
```
```
Linear system Ax = b.
We start HUBO Model from the two norm square of Ax - rx. (r is eigenvalue)
The maximum number of qubit variables is 64 in D-Wave 2000Q.
The total number of uses of qubits is the product of the matrix multiplied by the variable qubits used by each xi, and addition of qubits for eigenvalue variable.
```
## Designed Equation
```
First eigen value and eigen vector
 1   0 *  1 = 1 *  1
-4   3    2        2
minimum qubit status: 1 0 0 1 1 0
```
```
Second eigen value and eigen vector
 1   0 *  0 = 3 *  0
-4   3    3        3
minimum qubit status: 0 0 1 1 1 1
```
## Used Qubits
```
x = (a+2b, c+2d) : Eigenvector
r = e+2f         : Eigenvalue
```
### Result for D-Wave simulator
```
num  a  b  c  d  e  f   energy   num_oc.
0    0  0  0  0  0  0    0.0       1
7    0  0  0  0  0  1    0.0       1
8    0  0  0  0  1  1    0.0       1
15   0  0  0  0  1  0    0.0       1
23   0  0  1  0  1  1    0.0       1
40   0  0  1  1  1  1    0.0       1
51   1  0  0  1  1  0    0.0       1
```
### Discussion
```
The following four solutions have trivial numbers.
0    0  0  0  0  0  0    0.0       1
7    0  0  0  0  0  1    0.0       1
8    0  0  0  0  1  1    0.0       1
15   0  0  0  0  1  0    0.0       1
```
