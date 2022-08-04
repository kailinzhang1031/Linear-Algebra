# Lecture 5 Transposes, Permutations, Spaces $R^{n}$

This lecture firstly discusses properties of Permutations and Transposes, then introduces Vector spaces and their subspaces.

## Permutations

Using permutation matrices, we can do row exchanges during $A=LU$ factorization. Here we get the following euqation:
$$PA=LU\tag{5-1}$$

Properties of permutation matrix $P$:
- $P^{-1}=P^{T}$
- $P^{T}P=I$

## Transposes

*Symmetric* is a **special case** of transposes.

A matrix $A$ is *symmetric* if $A$ fits the following euqation.
$$A^{T}=A\tag{5-2}$$

For square matrix, we can identify symmetric matrices easily. Given any matrix $R$ (not necessarily square), we ask: How can we construct a symmetric matrix? This question inspires us try to get the following equation.

$$(R^{T}R)^{T}= R^{T}(R^{T})^{T}=R^{T}R\tag{5-3}$$

The product $R^{T}R$ is always symmetric because it fits expression (5-2).

## Vector spaces

Addition and Multiplication are two basic operations of vectors. They forms linear combinations of vectors. All linear combinations forms a vector space. These combinations follow the **rules** of a vector space.

A typical vector space is $\R^{2}$. 

- This vecor space is the set of all vectors with excatly **two real number components**.
- This vector space can be dipicted and we cll $\R^{2}$ the "$x-y$ plane".


This can be generalized to $\R^{n}$.


## Closure

The basic property of vector space is closure under addition and multiplication. Additionally, if mulitiplicationand addition behave in a reasonable way, they we call that collection a vector space.

Considering the closure of vector spaces, we get another property of vector space.
- Zero vector $0$ is in every vector space. 

## Subspaces

After defining spaces, we try to find a smaller collection of vectors that forms a smaller space inside a space. The smaller spaces is called subspace.

In analogy with properties of space, we can explore further on properties of subspaces. Here we analyse some base cases.

The subspaces of $\R^{2}$ are:

1. all of $R^{2}$,

2. any line through $\begin{bmatrix}
    0 \\
    0
\end{bmatrix}$ and

3. the zero vector alone $(Z)$.

The subspaces of $\R^{3}$ are:

1. all of $\R^{3}$,
2. any plane through the origin,
3. any line through the origin, and
4. the zero vector alone $(Z)$.

## Column space

Using definitions above, we can oberserve $A$ in a new way.

Given a matrix $A$ with columns in $\R^{3}$, 1)these columns and 2)all their linear combinations form a subspace of $\R^{3}$.

Next, we ask: How to understand the equation $A\mathbb{x}=\mathbb{b}$ in terms of subspaces and the column space of $A$?