# Eigenvalues and Eigenvectors
```
We are developing generator code for D-Wave's qpu solver.
```
```
Eigenvalue problem: Ax = λx.
We start HUBO Model from the two norm square of Ax - λx. (λ is eigenvalue)
The recommanded maximum number of logical qubit is 60 for D-Wave's qpu solver.
Because the qpu solver for the HUBO model finds all cases, using more than 60 logical qubits makes the number of cases too large. 
So it can bring problems to the data sent and received.
The total number of uses of qubits is the product of the matrix multiplied by the variable qubits used by each xi, and addition of qubits for eigenvalue variable.
```
## Example: HUBO_Eigen_6qubits.ipynb
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
### Used Qubits
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
We found 3 solutions for this eigenvalue problem.
An eigenvector space is a ray starting from the origin.
So, there can be multiple eigenvectors for the same eigenvalue.
```
```
num  a  b  c  d  e  f   energy   num_oc.
51   1  0  0  1  1  0    0.0       1 
Related Equation: 
   A    *  x  =  r  *  x
 1   0  *  1  =  1  *  1
-4   3     2           2
```
```
num  a  b  c  d  e  f   energy   num_oc.
23   0  0  1  0  1  1    0.0       1
Related Equation:
   A    *  x  =  r  *  x
 1   0  *  0  =  3  *  0
-4   3     1           1

num  a  b  c  d  e  f   energy   num_oc.
40   0  0  1  1  1  1    0.0       1
Related Equation:
   A    *  x  =  r  *  x
 1   0  *  0  =  3  *  0
-4   3     3           3
```
```
The following four solutions have trivial numbers.
0    0  0  0  0  0  0    0.0       1
7    0  0  0  0  0  1    0.0       1
8    0  0  0  0  1  1    0.0       1
15   0  0  0  0  1  0    0.0       1
```
## Other Examples
```
File name: Paper_HUBO_Ex1_2by2.ipynb
Matrix size: 2by2
Variable range: [-3, 3]
```
```
File name: Paper_HUBO_Ex2_2by2.ipynb
Matrix size: 2by2
Variable range: [-3, 3]
```
```
File name: Paper_HUBO_Ex3_2by2_repeated.ipynb
Matrix size: 2by2
Variable range: [-3, 3]
Repeated eigenvalues: Two eigenvalues are the same
```
```
File name: Paper_HUBO_Ex4_3by3.ipynb
Matrix size: 3by3
Variable range: [-7, 7]
```
```
File name: Paper_HUBO_Ex1_3by3_repeated.ipynb
Matrix size: 3by3
Variable range: [-7, 7]
Repeated eigenvalues: Two eigenvalues are the same
```
