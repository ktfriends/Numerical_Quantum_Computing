# Numerical Quantum Computing

## Team members at Quantum Research Center, Innovative Quantum Computed Tomography
```
Kyungtaek Jun: ktfriends@gmail.com
Hyunju Lee: hyunjulee0824@gmail.com
```


## Effective QUBO formulations
```
Solving linear system: Ax = b
We make several QUBO models for matrices and compare the results.
From the results, we propose a new method for constrained problems.
```


## Eigenvalues and Eigenvectors
```
Solving eigenvalue and eigenvector problem: Ax = kx
To solve Ax = kx, we use the two norm square of Ax - kx.
If any k and x satisfies Ax = kx, then the absolute value Ax - kx satisfies the minimum value 0.
```

## Linear System
```
Solving linear system: Ax = b
To solve Ax = b, we use the two norm square of Ax - b.
If any x satisfies Ax = b, then the absolute value of Ax - b satisfies the minimum value 0.
Related preprint (with Eigenvalue problem): https://arxiv.org/abs/2106.10819
```

## QAOA - Quantum Approximate Optimization Algorithm
```
It is an algorithm that finds the maximum value of the energy Hemiltonian used in quantum annealers in the gate model quantum computer.
We generally do QUBO modeling to use q^2 = q when creating an energy Hemiltonian.
```


## Range dependent Hamiltonian Algorithm
```
We introduce an algorithm that can be used by dividing the size of the entire domain according to the number of qubits.
We also form a QUBO model related to each subregion. 
Related preprint: https://arxiv.org/abs/2202.07692
```
