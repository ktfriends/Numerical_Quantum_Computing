# QUBO Refinement: Achieving Superior Precision through Iterative Quantum Formulation with Limited Qubits
```
Iterative solving algorithm (Example: quantum linear system: Ax = b)
Advantage: Precise calculations possible with a small number of qubits
```
## Example 1: Paper_Iter_Acc_2by2_easy_1qubit.ipynb
## Example 2: Paper_Iter_Acc_2by2_easy_3qubits.ipynb
```
Matrix A:    Vector b:
[[ root(2)   -root(3)]     [ 1024pi  
 [ root(5)    root(7)]]      -32e   ]
```

```
Radix-2 representation of the variable xi: 
1st representation: xi = -{P2^(-m)q_(i,-m) + 2^(-m+1)q_(i,-m+1) + --- + 2^mq_(i,m)} 
                        + {2^(-m)q_(i,-m) + 2^(-m+1)q_(i,-m+1) + --- + 2^mq_(i,m)}
2nd representation: xi = 2^(-m)q_(i,-m) + 2^(-m+1)q_(i,-m+1) + --- + 2^mq_(i,m)} - 2^(m+1)q_(i,m+1)
```
```
Qubit decomposition (one step): 
Example 1: xi = 2^(k){q_(i,k)^(+) - q_(i,k)^(-)}
Example 2: xi = 2^(k){q_(i,k)^(+) - q_(i,k)^(-)} + 2^(k-1){q_(i,k-1)^(+) - q_(i,k-1)^(-)} + 2^(k-2){q_(i,k-2)^(+) - q_(i,k-2)^(-)} 
```
```
The reason for using the first representation in this paper: 
The minimum energy discovery rate is higher than the second method when using constraints.
```
