[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/introduction-to-the-null-space-of-a-matrix)

Null space is a set of all vectors within a matrix that if you multiply it by a $\vec{n}$ then you will produce a $\vec{0}$:

$\begin{aligned} A = \begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \\ 4 & 3 & 2 & 1 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \\[1em] \vec{x}\epsilon|R^4 \end{aligned}$

given the equation above we need to find what vector $x$ is equal to which will give the result of a $0$ vector no matter the number in $R^4$:

$N(A) = \vec{x}\epsilon|R^4 \; | \; A\vec{x} = \vec{0}$

to do this we can convert the equation into linear systems and then use [reduced row echelon](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to figure out $\vec{x}$:

![[Pasted image 20260701123224.png]]

which then once we have our reduced row echelon, we can create our linear combination that will allow us to find the **null space of $A$**:

![[Pasted image 20260701123350.png]]

so now, any real number substituted for $x_3$ and $x_4$ will give the null space of matrix $A$:
![[Pasted image 20260701123959.png]]

## Relation to Linear Independence
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/null-space-3-relation-to-linear-independence)

This relates to linear independence as if the only way to get the $\vec{0}$ from the matrix $A$ is to multiply it by each $x$ component where $x = 0$ 

going back to our example
$A = \begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \\ 4 & 3 & 2 & 1 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$

because the $N(A) = spans ( \begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix},  \begin{bmatrix} 1 \\ -2 \\ 1 \\ 0 \end{bmatrix},  \begin{bmatrix} 2 \\ -3 \\ 0 \\ 1 \end{bmatrix})$
Then it's clear that $A$ is not linearly independent because to get the $\vec{0}$ from $A$ we can apply multiple $x$ components to get there but if the null space was:

$N(A) = span( \begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix})$

Then $A$ would be linearly independent 

## Dimension of null space - Nullity
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/dimension-of-the-null-space-or-nullity)

Nullity is defined as the number of **non-pivot columns** within the [reduce row echelon form](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) of a matrix:



![[Pasted image 20260702174654.png]]

## Left Null Space 
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-rowspace-and-left-nullspace)

The left null space of a matrix is the null space of a [transposed matrix](Transposing) 

$N(A^T) = Left \; Null \; Space \; of \; A$

Its called the left null space because if we apply a transpose to $A\vec{x} = \vec{0}$ then the order is reversed and $\vec{x}^T$ is on the left 

$\vec{x}^T \; A = \vec{0}^T$

$N(A^T) = (\vec{x} | A^T \vec{x} = \vec{0}) = (\vec{x} \; | \; \vec{x}^T A = \vec{0}^T)$

For instance if we have matrix $A$ and its null space from applying the [reduced row echelon](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations)  

$A = \begin{bmatrix} 2 & -1 & -3 \\ -4 & 2 & 6 \end{bmatrix}$

$N(A) = Span(\begin{bmatrix} {1\over2} \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} {3\over2} \\ 0 \\ 1 \end{bmatrix})$

Which then if we transpose $A$ and find its null space we'll see that its a different result
![[Pasted image 20260805172440.png]]

$N(A^T) = Span(\begin{bmatrix} 2 \\ 1 \end{bmatrix})$

Another property with the left null space is that it will be orthogonal with the [column space](Column%20Space) which is clear if we visualize it with a graph 
![[Pasted image 20260806133509.png]]

and if we find the dot product between the column space and left null space, the result ends up to be $0$
![[Pasted image 20260806133936.png]]

