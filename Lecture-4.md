# Lecture 4 Factorization into $A=LU$

## Introduction

This lecture starts with how to understand Guassian elimination in terms of matrices.

Firstly, we focus on some operation on the product of matrices.

## Inverse of a product

The inverse of a matrix product $AB$ is $B^{-1}A^{-1}$.

## Transpose of a product

The inverse of a matrix product $AB$ is $B^{T}A^{T}$.

For any invertible matrix, the inverse of $A^{T}$ is $(A^{-1})^{T}$.


## $A=LU$

We've dicussed how to solve $EA=U$. Here we ask: Can we do elimination on the right side of the equation? Also, we want to find a matrix $L$ so that

$$A=LU\tag{4-1}$$

This leads to the factorization of $A=LU$. This process it the inverse operation of $EA=U$. We can do this by canceling the elimination matrix by multiplying its inverse: $E_{21}^{-1}E_{21}A=E_{21}^{-1}U$.

- $U$ is upper triangular with pivots on the diagonal.
- $L$ is lower triangular and har ones on the diagonal.

This factorization can be further written with a diagnal matrix whose entries are the pivots:

$$A = LDU^{-1} \tag{4-2}$$

## How expensive is elimination?

Given an $n\times n$ matrix, the total number of operations needed to factor $A$ into $LU$ is on the order of $n^{3}$, which is $\frac{1}{3}n^{3}$.

## Row exchanges

As discussing above, we suppose there are no row exchanges. Here we ask: What if there are row exchanges? In other words, what happens if there's a zero in a pivot position?

We can do row exchanges by permutation matrix $P$.

- The inverse of any permutation matrix $P$ is $P^{-1} = P^{T}$.
- There are $n!$ different ways to permute the rows of an $n\times n$ matrix(including the permutation that leaves all rows fixed) so there are $n!$ permutation matrices.
- These matrices form a *multiplicative group*. 