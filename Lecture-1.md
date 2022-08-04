# Lecture 1 The Geometry of Linear Equations

## Introduction

This lecture proposes a topic, which is "How to solve Systems of Linear Equations". This question acts as a basic and major role in Linear Algebra.

According to what we have learnt, $Ax=b$ is the base case when we get in touch with equations. For the convenience of future, we set equation above as $A_1x_1=b_1$. $A_1x_1=b_1$ is known as Linear Equation with One Unkown, which contains one unknown and has the highest power of 1. We name it as Equation 1.

We can expand the case above. Firstly, we introduce Equation 2 in the same form of Equation 1: $A_2x_2=b_2$. Secondly, we combine these two equations and get a system, which is known as Linear Equations with Two Unkowns: 
$$A_1x_1=b_1, \\ A_2x_2=b_2 \tag{1-1}$$

An intuitive try is that, can we observe equations in a different way? Moreover, can we visualize these equations to help us understand?

## Row Picture

When observing systems of linear equations in a row way, we get a row picture. In this picture, equations are interpretated as lines in coordinate systems and solutions are visualized as the intersection of two lines.

## Column Picture

We can also observe this system in a column way. By doing so, we get column picture. In this picture, the system is interpretated as linear combination of two vectors. Furthure more, when observing by columns, we get 2 coefficients each column. Each vector is composed by 2 coffecients. In (1-1), we get 
$\mathbf{c}=\begin{bmatrix}
    2 \\
    -1
\end{bmatrix}, 
\mathbf{d}=\begin{bmatrix}
    -1 \\
    2
\end{bmatrix}$.

The system can be interpretated as linear combination $x\mathbf{c}+y\mathbf{d}$ gets vector $\begin{bmatrix}
    0 \\
    3
\end{bmatrix}$.


## Matrix Picture

When the system contains 3 or more euqations, it's more difficult for us to find the intersection of planes or hyperplanes. The column picture provides us a way to oberserve systems of equations in a new way.

Using a new set of expression, We try to simplify a system, which contains serious of linear equations, to only 1 equation .

So, we got fundamental terminologies shown as following:

- *Coefficient Matrix* $A$

- *Vector of Unkowns* $\mathbf{x}$

- *Vector of Values in the Right Side* $\mathbf{b}$

The system of equations is simplified as 
$$A\mathbf{x}=\mathbf{b} \tag{1-2}$$
and we get the Matrix Picture.

## Matrix Multiplication

After define several terms above, we ask: what can we do with these letters? This question can be interpretaed as How to use these letters to solve (1-2)?

Note that we have got a simplied form of systems of equations. So, here we need to define new rules of multiplication and calculation.

When defining rules of multiplication, we need to consider the original form of (1-2), which is (1-1). As discussed above, we prefer to consider system of equations in a Column Way. We got 2 ideas on defining methods of multiplication: 

- Based on the definition of Linear Combination.

- Based on the definition of Vector: Dot Product.

## Linear Independence

Then, we ask: Given a matrix $A$, can we solve
$$A\mathbf{x}=\mathbf{b}$$
for every possible vector $\mathbf{b}$? 

In other words, do the linear combinations of the column vectors fill the $xy$-plane (or space, in the three dimensional case)?

We try to find when given $A$, a special case for all $\mathbf{b}$.

If the answer is no, then $A$ is a *singular matrix*, its column vectors are *linearly dependent*.

If the answer if yes, then $A$ is a *non-signular matrix*, its column vectors are *linearly independent*.
