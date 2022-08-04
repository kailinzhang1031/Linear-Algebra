# Lecture 2 Elimination with Matrices

## Introduction

We try to define, or explore methods to solve $A\mathbf{x}=\mathbf{b}$.

## Method of Elimination

Using *Elimination* technique, we get terminologies shown as following:
- *Pivot*: non-zero
- *Upper Triangular Matrix* $U$: The determinant of $U$ is the product of the pivots.
- *Augmenting*: from $\mathbf{b}$ to $\mathbf{c}$
- Simplified Equation $U\mathbf{x}=\mathbf{c}$
- *Back Substitution*: to solve $U\mathbf{x}=\mathbf{c}$

To ensure pivots not be zero, we can exchange rows. When this does not work, $A$ is *invertible*, otherwise $A$ is *vertible*.

## Elimination Matrices

Elimination is almost a repeatance of multiplication and subtraction. We then need to combine several steps of elimination in one way. Then we get *Elimination Matrices* $E$. 

- Matrix multiplication is *associative*:

$$E_{32}(E_{21}A=U) \Leftrightarrow (E_{32} E_{21} A=U)$$

Note that elimation matrices represents row operations, so we need to consider both $E$ and $A$ by rows.

A **special case** of elimination matrices is the *Permutation Matrix* $P$.
- Matrix multiplication is not *commutative*: 
$$PA \not ={AP}$$

## Inverses

We try to "undo" the operation from the elimination matrix. Then, we get the other **special case** of elimination matrices: *Inverse Matrix* $E^{-1}$.

This can be also interpreted as, we try to find a matrix to solve out $\mathbf{x}$ from the right hand side of the equation.

It yields the following formulas.

$$E_{21}^{-1}E_{21}=I$$

$$\mathbf{x}=A^{-1}\mathbf{b}$$