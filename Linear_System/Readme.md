# Linear System
```
Linear system Ax = b.
We start QUBO Model from the two norm square of Ax - b.
```
## QUBO Model 1
```
A vector x represent as x = q1 + 2q2 + 4q3 + ... - q1' - 2q2' - 4q3' - ... .
This QUBO model is an expression for solving integers with respect to the vector x.
This method uses a lot of qubits, but finds more solutions.
```
## QUBO Model 2
```
For QUBO model 2, a vector x = q1 + 2q2 + 4q3 + ... - 2^(m+1)q'.
This QUBO model is an expression for solving integers with respect to the vector x.
This method minimizes the total qubits used.
```
### Examples


