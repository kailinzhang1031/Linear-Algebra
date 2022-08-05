# Lecture 7 Solving $A\mathbf{x}=\mathbf{0}$: Pivot Variables, Special Solutions
 
 After defining serveral subspaces, this lecture focuses on How to Compute these Subspaces? Also, we ask: How can we solve $A\mathbf{x}=\mathbf{b}$ in terms of subspaces?

 ## Computing the nullspace

 Firstly, We focus on a more special case: $A\mathbf{x}=\mathbf{0}$. We can do eliminations to simplify matrix $A$. 
 
Note that
- The row operations used in the method of elimination don’t change the 
solution to $A\mathbf{x}=\mathbf{0}$ so they don’t change the nullspace.
- They do affect the column space.
- The all-zero row are linear combination of the pivot rows.

By elimination, the original equation $A\mathbf{x}=\mathbf{0}$ is transformed to
$$U\mathbf{x}=\mathbf{0} \tag{7-1}$$

Here we get
- The matrix $U$ is in *echelon* (staircase) form.
- The non-pivot columns are linear combination of previous columns.
- The *rank* of a matrix $A$ = The number of pivots it has.

## Special solutions

We can use back-substitution to find the solutions $\mathbf{x}$ to the euqation $U\mathbf{x}=\mathbf{0}$.

By observing the columns of $U$, we get
- *Pivot Columns*
- *Free Columns*
- *Free Variables*

The basic algorithm of solving $U\mathbf{x}=\mathbf{0}$ can be decribed as following.
- Elimination: find pivot/free columns & variables
- Assign values to free variables
- Back-substitution: complete the solution.

We can slove out solutions with given values of free variables. These solutions are called *special solutions*.

The nullspace of $A$ is the collection of all linear combinations of these "special solution" vectors.

We can also analyse the rank of $A$.
- The rank $r$ of $A$ = The number of pivot columns
- The number of free columns = $n-r$
- The number of free columns = The number of special solutions = The dimension of the nullspace

# Reduced row echelon form

We can further simplify $U$ to a matrix $R$ in reduced row echelon form (rref form), the equation $U\mathbf{x}=\mathbf{0}$ can be transformed into
$$R\mathbf{x}=\mathbf{0}\tag{7-2}$$

By exchanging some columns, $R$ can be convert into
$$R=\begin{bmatrix}I & F \\ 0 & 0 \end{bmatrix}$$

- $F$ denotes free columns.
- Here $I$ is an $r\times r$ square matrix.

If $N$ is the *nullspace*, we can solve $R\mathbf{x}=\mathbf{0}$ for $\mathbf{x}$ as
$$N=\begin{bmatrix}
    -F \\
    I
\end{bmatrix} \tag{7-3}$$

That is to say
$$RN=\mathbf{0} \tag{7-4}$$

- Here $I$ is an $n-r \times n-r$ square matrix.
- $\mathbf{0}$ is an $m \times n-r$ matrix.
- The columns of $N$ are the special solutions.
