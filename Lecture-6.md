# Lecture 6 Column Space and Null Space

This lecture focuses on studying subspaces, including column spaces and null spaces of a matrix.

## Review of subspaces

At the begining, we need to make some basic rules of subspaces clear:

- A vector space must follow the rule of linear combination.
- Given a plane $P$ and a line $L$, which are subspaces of $\mathbb{R}^{3}$, the union $P\cup L$ is not a subspace while the intersection $P\cap L$ is a subspace.

## Column space of $A$

We then need to ask: How do we build up a Column Space?

The column space of a matrix $A$ is the vector space made up of all linear combinations of the columns of $A$.

## Solving $A\mathbf{x}=\mathbf{b}$

Firstly, by considering $\mathbf{b}$, We ask: Given a matrix $A$, for what vectors $\mathbf{b}$ does $A\mathbf{x}=\mathbf{b}$ have a solution $\mathbf{x}$?

Note that $A\mathbf{x}=\mathbf{b}$ may not have solutions because solving $A\mathbf{x}=\mathbf{b}$ is equivalent to solving four linear euqations with three unknowns.

If there is a solution $\mathbf{x}$ to $A\mathbf{x}=\mathbf{b}$, we can get following conclusion.
- $\mathbf{b}$ must be a linear combination of the columns of $A$.

Geometrily, only three columns cannot fill the entire four dimensional vector space, some vectors $\mathbf{b}$ cannot be expressed as linear combinations of $A$.

Next, we ask: Big question: what $\mathbf{b}$'s allow $A\mathbf{x}=\mathbf{b}$ to be solved?

By considering $\mathbf{b}=A\mathbf{x}$, we can get the following conclusion.

- The system of linear equatiion $A\mathbf{x}=\mathbf{b}$ is *solvable* exactly when $\mathbf{b}$ is a vector in the column space of $A$.

After that, we can further study the column space of $A$. In the case of the lecture, the columns of $A$ are not all indepen and we can choose 2 columns as pivot columns and another column is the non-pivot column. We can get that the column space of our matrix $A$ is a two dimensional subspace of $\mathbb{R}^{4}$.

## Nullspace of $A$

In this section, we set $\mathbf{b}=\mathbf{0}$.

The nullspace of a matrix $A$ is the collectio of all solutions $\mathbf{x}=\begin{bmatrix}
    x_1 \\
    x_2 \\
    x_3 \\
\end{bmatrix}$ to the equation
$$A\mathbf{x}=0 \tag{6-1}$$


Here we can also explore properties of the nullspace:
-The column space of the matrix in our example was a subspace of $\mathbb{R}^{4}$.
- The nullspace of $A$ is a subspace of $\mathbb{R}^{3}$.
- The nullspace of $A$ still fits the rules of linear combination.
- The nullspace $N(A)$ consists of all multiples of $\begin{bmatrix}
    1 \\
    1 \\
    -1
\end{bmatrix}$ and can be expressed as $c\begin{bmatrix}
    1 \\
    1 \\
    -1
\end{bmatrix}$.

## Other values of $\mathbf{b}$

After setting $\mathbf{b}=\mathbf{0}$, we ask: can we solve the equation $A\mathbf{x}=\mathbf{b}$ with other values of $\mathbf{b}$?

At this time, we need to consider $\mathbf{x}$. The solutions to the equation may form a subspace.

The lecture provides an exmaple that the solutions to the equation do not form a subspace. The zero vector is not a solution to this equation. The solutions form a line in $\mathbb{R}^{3}$ without the origin $\begin{bmatrix}
    0 \\
    0 \\
    0
\end{bmatrix}$.

