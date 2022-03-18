# Linear System
```
Linear system Ax = b for fractional terms.
We start QUBO Model from the two norm square of Ax - b.
The maximum number of qubits used is 64 in D-Wave 2000Q.
The total number of uses of qubits is the product of the matrix multiplied by the qubits used by each xi.
```
## QUBO Model
```
A vector x represent as x = 1/2*q1 + 1/4*q2 + 1/8*q3 + ... - 1/2*q1' - 1/4*q2' - 1/8*q3' - ... .
This QUBO model is an expression for solving integers with respect to the vector x.
This method uses a lot of qubits, but finds more solutions.
```
### Examples
```
1. 3 by 3 matrix x and a vector b:
        1   -1    1
   A = -2    3    4 , b = (1, -1, 2)
        1   -4   -1
   12 qubits for QUBO 1, x = 1/2*q1 + 1/4*q2 - 1/2*q3 - 1/4*q4
```
### Comparison between QUBO with Coefficient Matching Algorithm (CMA) and general QUBO
```
CMA     vs    General 
4.78           1.38

1. The code and result using CMA for linear equation 1 can be found in "frcn_12qubits.ipynb".
2. The result of not using CMA for linear equation 1 can be found in proceedings of "Solving linear systems by quadratic
  unconstrained binary optimization on D-Wave quantum annealing device".
```
