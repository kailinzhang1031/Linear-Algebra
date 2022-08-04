# Lecture 3 Mutiplication and Inverse Matrices

## Introduction

From this lecture, we still need to define, or explore basic rules to solve $A\mathbf{x}=\mathbf{b}$. 

We've discussed about the product of matrix $A$ multiplies with vector $\mathbf{x}$. We can now ask: What's the product between matrix $A, B$? Also, how can we get $AB=C$?

**Note that** matrix multiplication is still rooting on the structure of coefficient matrix $A$.

This lecture provides 4 ways to interprete matrix multiplication.

## Standard(row times column)

Observing $C$ by elements.

## Columns

Observing $C$ by columns, columns of $C$ are combinations of columns of $A$. Here we consider $B$ as operation matrix.

## Rows

Observing $C$ by rows, rows of $C$ are combinations of rows of $B$. Here we consider $A$ as operation matrix.

## Column times row

Observing $A$ and $B$, we ask: What's the product of column times row?

This case can be generalized by solving the base case, which is $m*1$ vector $A$ times $1*n$ vector $B$. The product of these two vectors is a matrix.


## Blocks

$A$ and $B$ can also be divided into blocks and then do multiplication.

## Inverses

The second part of this lecture discusses about **Inverses**.

To simplify our discussion, we firstly focus on **square matrix** $A$.

Existence: 
- If $A^{-1}$ exists: 
  - $A^{-1}A=I=AA^{-1}$, 
  - $A$ is invertible or nonsingular.
- If $A^{-1}$ does not exist: 
  - $A$ is singular, 
  - $det(A)=0$,
  - exists some non-zero vector $\mathbf{x}$,for which $A\mathbf{x}=0$.
  - columns of $A lie on the same line.


## Gauss-Jordan Elimination

As mentioned above, we have actually get a new equation:
$$AA^{-1}=I \tag{3-1}$$

We then ask: Given a square matrix $A$, can we solve out $A^{-1}$ more efficiently?

Here we discuss about *Gauss-Jordan Elimination*, which use the methode of elimnation to solve two or more linear equations at the same time.

The essence of Gauss-Jordan Elimination can be interperetated by block matrices as below.

$$ \begin{aligned}
    E[A|I] &= [I|E] \\
    EA &= I
\end{aligned} \Rightarrow E=A^{-1}$$
