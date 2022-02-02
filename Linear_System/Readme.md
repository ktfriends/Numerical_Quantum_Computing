# Linear System
```
Linear system Ax = b.
We start QUBO Model from the two norm square of Ax - b.
The maximum number of qubits used is 64 in D-Wave 2000Q.
The total number of uses of qubits is the product of the matrix multiplied by the qubits used by each xi.
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
```
1. 2 by 2 matrix x and a vector b:
   A =  3    1 , b = (-1, 2)
       -1    5 
   8 qubits for QUBO 1, x = q1 + 2q2 - q3 - 2q4: QUBO1_LS_8qubits.ipynb
   6 qubits for QUBO 2, x = q1 + 2q2 - 4q3:      QUBO2_LS_6qubits.ipynb
```
2. 3 by 3 matrix x and a vector b:
        1   -1    1
   A = -2    3    4 , b = (4, -4, 8)
        1   -4   -1
   12 qubits for QUBO 1, x = q1 + 2q2 - q3 - 2q4: QUBO1_LS_12qubits.ipynb
   9 qubits for QUBO 2, x = q1 + 2q2 - 4q3:       QUBO2_LS_9qubits.ipynb
```
3. 4 by 4 matrix x and a vector b:
        9   -2   -2   9
   A = -3   10   -3  -3 , b = (-29, 19, 30, -19)
       -8    6   -9  -8
       -8    8   10   9 
      16 qubits for QUBO 1, x = q1 + 2q2 - q3 - 2q4: QUBO1_LS_16qubits.ipynb
      12 qubits for QUBO 2, x = q1 + 2q2 - 4q3:      QUBO2_LS_12qubits.ipynb
```
4. 4 by 4 matrix x and a vector b:
        9   -2   -2   9
   A = -3   10   -3  -3 , b = (-29, 19, 30, -19)
       -8    6   -9  -8
       -8    8   10   9 
      24 qubits for QUBO 1, x = q1 + 2q2 + 4q3 - q4 - 2q5 - 4q6: QUBO1_LS_24qubits.ipynb
      16 qubits for QUBO 2, x = q1 + 2q2 + 4q3 - 8q4:            QUBO2_LS_16qubits.ipynb
```

