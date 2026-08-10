[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-rowspace-and-left-nullspace), [khan acad vid rank(A) = Rank(A transpose)](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-rank-a-rank-transpose-of-a)

A row space is the [column space](Column%20Space) of the [transposed matrix](Transposing), 

$C(A^T) = Row \; space \; of \; A$

so for instance, if we have matrix $A$

$A = \begin{bmatrix} 2 & -1 & -3 \\ -4 & 2 & 6 \end{bmatrix}$

its column space can represented as 

$C(A) = Span(\begin{bmatrix} 2 \\ -4 \end{bmatrix}, \begin{bmatrix} -1 \\ 2 \end{bmatrix}, \begin{bmatrix} -3 \\ 6 \end{bmatrix})$

Which then if we transpose $A$ and find its column space, the result is the span of all the rows from the original matrix $A$ hence why its called the **Row space** 

$A^T = \begin{bmatrix} 2 & -4 \\ -1 & 2 \\ -3 & 6 \end{bmatrix}$

$C(A^T) = Span(\begin{bmatrix} 2 \\ -1 \\ -3 \end{bmatrix}, \begin{bmatrix} -4 \\ 2 \\ 6 \end{bmatrix})$

This is because, when a matrix is transposed its columns and rows switch, so matrix $A$ went from $2 \times 3$ to a $3 \times 2$ matrix after transpose. So naturally, when we get the column space, it ends up being the span of the rows from matrix $A$

When it comes to determining the [rank](Column%20Space) of $A^T$, it follows the same process and produces the same result as $Rank(A)$ where its determined by the amount of pivot entries produced from putting matrix $A$ into [reduced row echelon form](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations)

![[Pasted image 20260805160259.png]]

$Rank(A) = 1$

$Basis \; of \; A = Span(\begin{bmatrix} 2 \\ -4 \end{bmatrix})$

![[Pasted image 20260805160517.png]]

$Rank(A^T) = 1$

$Basis \; of \; A^T = Span(\begin{bmatrix} 2 \\ -1 \\ -3 \end{bmatrix})$

So therefore, no matter if its pivot rows or pivot columns the amount of pivot entries will always be the same and thus the rank of matrix $A$ and $A^T$ are equivalent to one another 

$Rank(A) = Rank(A^T)$

Another property with the row space is that its orthogonal to the [null space](Null%20space) as if we visualize it
![[Pasted image 20260806134423.png]]

and apply the [dot product](Vector%20Dot%20Product%20and%20Length) to each vector in the null space against the row space, it works out to be orthogonal

![[Pasted image 20260806134558.png]]