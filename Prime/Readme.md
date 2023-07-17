# RSA cryptosystem 
```
RSA cryptosystem N = pq.
We start QUBO Model from the norm square of N - pq.
We only upload HUBO models 
```
## HUBO model
```
Qubit representation
x1 = q0 + 2q1 + 4q2 + --- + 2^(n-1)q(n-1)
x2 = qn + 2q(n+1) + 4q(n+2) + ---  2^(n-1)q(2n-1)
x1x2 = N

Integers
x1 = 10111
x2 = 101
RSA number: 1021211

Used qubits n = 14
File name: PF_RSA_100x_small.ipynb
```
## HUBO model with subrange algorithm
```
Qubit representation
x1 = q0 + 2q1 + 4q2 + --- + 2^(n-1)q(n-1) + Si
x2 = qn + 2q(n+1) + 4q(n+2) + ---  2^(n-1)q(2n-1) + Sj
x1x2 = N

Integers
x1 = 1000033
x2 = 1000037
RSA number: 1000070001221
Si = 1000000
Sj = 1000000

Used qubits n = 6
File name: PF_RSA_Subrange.ipynb
```
