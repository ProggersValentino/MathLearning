[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/introduction-to-the-null-space-of-a-matrix)

Null space is a set of all vectors within a matrix that if you multiply it by a $\vec{n}$ then you will produce a $\vec{0}$:

$\begin{aligned} A = \begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \\ 4 & 3 & 2 & 1 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \\[1em] \vec{x}\epsilon|R^4 \end{aligned}$

given the equation above we need to find what vector $x$ is equal to which will give the result of a $0$ vector no matter the number in $R^4$:

$N(A) = \vec{x}\epsilon|R^4 \; | \; A\vec{x} = \vec{0}$

to do this we can convert the equation into linear systems and then use [reduced row echelon](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FReduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to figure out $\vec{x}$:

![[Pasted image 20260701123224.png]]

which then once we have our reduced row echelon, we can create our linear combination that will allow us to find the **null space of $A$**:

![[Pasted image 20260701123350.png]]

so now, any real number substituted for $x_3$ and $x_4$ will give the null space of matrix $A$:
![[Pasted image 20260701123959.png]]

## Relation to Linear Independence
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/null-space-3-relation-to-linear-independence)


## Dimension of null space - Nullity
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/dimension-of-the-null-space-or-nullity)

Nullity is defined as the number of **non-pivot columns** within the [reduce row echelon form](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FReduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) of a matrix:



![[Pasted image 20260702174654.png]]