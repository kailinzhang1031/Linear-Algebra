# Lecture 8 Solving $A\mathbf{x}=\mathbf{b}$: row reduced form $R$

In the previous lecture, we explored how to solve $A\mathbf{x}=\mathbf{0}$. This lecture will focus on $A\mathbf{x}=\mathbf{b}$.

Now, we ask:
- Exisitence of solutions: When does $A\mathbf{x}=\mathbf{b}$ have solutions $\mathbf{x}$ ?
- Structure of solutions: How can we describe those solutions?

## Solvability conditions on $\mathbf{b}$

We will firstly observe $\mathbf{b}$ to decide the existence of solutions of $A\mathbf{x}=\mathbf{b}$.

Given the original euqation $A\mathbf{x}=\mathbf{b}$, we can have a intuitive way to decide the existence,
-  If a combination of the rows of $A$ gives the zero row, 
-  then the same combination of the entries of $\mathbf{b}$ must equal zero.

We can solve it using **elimination on the augmented matrix**. We can choose $\mathbf{b}$ that ensures the existence of solutions. 

We can conclude $A\mathbf{x}=\mathbf{b}$ is solvable exactly when
- From the eliminated augmented matrix, the non-pivot rows fit $0=0$.
- From an earlier lecture, $\mathbf{b}$ is in the column space $C(A)$.


## Complete solution

The *complete solution* for $A\mathbf{x}=\mathbf{b}$ can be built up by adding the *particular solution* to all vectors in the nullspace. This is applicable in all linear euqations.

### A particular solution

One way to find a particular solution to the equation $A\mathbf{x}=\mathbf{b}$ is to 
- set all *free variables* to zero, 
- then solve for the *pivot variables*.

### Combined with the nullspace

The general solution to $A\mathbf{x}=\mathbf{b}$ is given by
$$\mathbf{x}_{complete} = \mathbf{x}_{p} + \mathbf{x}_{n}$$
where $\mathbf{x}_n$ is a generic vector in the nullspace.

The general solution can be proved by
$$\begin{aligned}
    A\mathbf{x}_p &= \mathbf{b} \\
    A\mathbf{x}_n &= \mathbf{0} 
\end{aligned} \Rightarrow A(\mathbf{x}_p + \mathbf{x}_n)=\mathbf{b}$$

for every vector $\mathbf{x}_n$ in the nullspace.

The general solution can also be interperted geometircally. It's simillar to a specific dimensional subspace in the space of $\mathbb{R}^n$.


## Rank

*Rank* provides us a way to union both the existence and the description of solutions.

We've got some properties of rank that
- The rank of a matrix = The number of pivots of that matrix
- If $A$ if an $m\times n$ matrix of rank $r$, we know $r \leqslant m$ and $r \leqslant n$.

### Full column rank

If $r=n$, we know that
- The nullspace has dimension $n-r = 0$.
- The nullspace contains only the zero vector.
- There are no free variables or special solutions.

If $A\mathbf{x}=\mathbf{b}$ has a sloution
- it is unique;
- there is either 0 or 1 solution,
- examples in which columns are independent are common in applications

We also know that $r \leqslant m$,
- The row reduced echolon form of the matrix will look like $R=\begin{bmatrix}I\\0\end{bmatrix}$.
- For any vector $\mathbf{b}$ in $\mathbb{R}^m$ that's not a combination of the columns of $A$,
- there is no solution to $A\mathbf{x}=\mathbf{b}$.

### Full row rank

If $r=m$, then
- the reduced matrix $R=[I F]$ has no rows of zeros
- and so there are no requirements for the entires of $\mathbf{b}$ to satisfy.
- The equation $A\mathbf{x}=\mathbf{b}$ is solvale for every $\mathbf{b}$.
- There are $n-r=n-m$ free variables,
- so there are $n-m$ special solutions to $A\mathbf{x}=\mathbf{0}$.

### Full row and column rank

If $r=m=n$ is the number of pivots of $A$, then
- $A$ is an invertible square matrix
- and $R$ is the identity matrix.
- The nullspace has dimension zero,
- and $A\mathbf{x}=\mathbf{b}$ has a unique solution for every $\mathbf{b}$ in $\mathbb{R}^{m}$.

### Summary

If $R$ is in row reduced form with pivot columns first(rref), the table below summarized our results.

||$r=m=n$|$r=n<m$|$r=m<n$|$r<m, r<n$|
|:-:|:-:|:-:|:-:|:-:|
|$R$|$I$|$\begin{bmatrix}I \\0\end{bmatrix}$|$\begin{bmatrix}I&F\end{bmatrix}$|$\begin{bmatrix}I & F \\0 & 0\end{bmatrix}$|
|# solutions to $A\mathbf{x}=\mathbf{b}$| $1$ | $0$ or $1$ | infinitely many | $0$ or infinitely many |