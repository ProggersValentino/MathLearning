

## Matrices
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-transpose-of-a-matrix)

A **matrix transpose** is the process of swapping a matrix's rows and columns. So if you have matrix $A$ being a $4 \times 2$ matrix then when transposed it becomes a $2 \times 4$ matrix where the $4$ rows become the columns and the $2$ columns become the rows. 

A transpose of a matrix is represented like $A^T$ 
![[Pasted image 20260804140259.png]]

For instance, if we have matrix $C$ which is a $4 \times 3$ matrix which consist of:
![[Pasted image 20260804142115.png]]

So then if take the transpose of $C$ ($C^T$) then it will become a $3 \times 4$ matrix where the $4$ rows become the columns and the $3$ columns become the rows
![[Pasted image 20260804142427.png]]

### Determinant of transpose
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-determinant-of-transpose)

When a matrix undergoes a transpose and then solve for its [determinant](Determinant%20Matrices), the determinant of $A^T$ is equivalent to the determinant of $A$

This is because, despite transposing, the transpose does not change the matrix enough to impact the result of the determinant, like for instance if we have matrix $A$ and its determinant

$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$

$det(A) = ad - bc$

and then transpose matrix $A$

$A^T = \begin{bmatrix} a & c \\ b & d \end{bmatrix}$

$det(A^T) = ad - bc$

It is clear that it is the same result despite matrix $A$'s rows and columns swapping. 

$\therefore det(A) = det(A^T)$

This applies to the $n + 1 \times n + 1$ matrices to where if we have matrix $A$ and $A^T$ and find the determinant for each matrix
![[Pasted image 20260804154850.png]]

![[Pasted image 20260804154916.png]]

If we apply an induction to where all cases follow the same result as the $2 \times 2$ then $det(A^T)$ is really just the $det(A)$

$det(A^T) = a_{11} \; det(A_{11} - a_{12} \; det(A_{12} + ... + (-1)^{1 + m} \; det(A_{1m}$

so then we can safely say that $det(A) = det(A^T)$ proving that this concept works for all cases

### Transpose of Matrix Product
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-transpose-of-a-matrix-product)

Multiplying matrices together and then transposing the matrix product is equivalent to taking transposing each matrix and then multiplying them together to get the matrix product:

$(AB)^T = B^TA^T$

where 
![[Pasted image 20260804172920.png]]

If we want to generate matrix $C = AB$ and $D = B^TA^T$ then we can see that the numbers multiplied against each other are same in both equations when finding the matrix $C$ and $D$
![[Pasted image 20260804173650.png]]

so therefore, we can denote that the transpose of $C$ equals $D$ ($(AB)^T$) and the matrix product of $C$ is equal to the transpose of $D$ ($B^TA^T$)

This is handy because it reduces the amount of steps needed to achieve the exact same result 

### Transpose of sums and inverses
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-transposes-of-sums-and-inverses)

Another two properties of the transpose is summing two matrices together and then transposing the product is the same as transposing the two matrices and then summing them together

$C = A + B$
$C^T = (A+B)^T = A^T + B^T$


And the transpose of an [inverse matrix](Inverse%20Matrices) is the inverse of transpose

$(A^T)^{-1} = (A^{-1})^T$


## Vectors
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/linear-algebra-transpose-of-a-vector)

Because vectors can be represented in matrix form, they can also be transposed 

$\vec{v} = \begin{bmatrix} v_1 \\ v_2 \\ . \\ . \\ . \\ v_n \end{bmatrix} \;\;\; \vec{v}^T = \begin{bmatrix} v_1 & v_2 & . & . & . & v_n \end{bmatrix}$

This has a few interesting properties in that if we do the [dot product](Vector%20Dot%20Product%20and%20Length) of $v$ and $w$ we know that it expands to

$\vec{v} \cdot \vec{w} = v_1w_1 + v_2w_2 + ... + v_nw_n$

But if we were to transpose $\vec{v}$ [multiply](Matrix%20Multiplication) it by $\vec{w}$ to get a matrix product, you can see that its exactly the same process as the dot product

$\vec{v}^T \; \vec{w} = v_1w_1 + v_2w_2 + ... + v_nw_n$

So therefore, we can say that the dot product is **equivalent** to getting a the matrix product of the transpose of a vector multiplied by another vector

$\vec{v} \cdot \vec{w} = \vec{v}^T \; \vec{w}$

this is because, when the vectors undergo the dot product, they are both $n \times 1$ matrix which does not fulfill the [closure of multiplication property](Properties%20of%20Matrices) 

However, when we transpose $\vec{v}$ all of the sudden $\vec{v}^T$ becomes an $1 \times n$ and $\vec{w}$ still $n \times 1$ which then it becomes a valid matrix multiplication 

![[Pasted image 20260805124018.png]]

This expands to multiplying a matrix against a vector where 

$\vec{x} \epsilon R^n \; \;\; \vec{y} \epsilon R^m$
$A = m \times n$

$(A\vec{x}) \cdot \vec{y} = (A\vec{x})^T \; \vec{y}$

Then if we take the dot product of the $A\vec{x}$ against $\vec{y}$ that is equivalent to the transpose of $A\vec{x}$ multiplied by $\vec{y}$ which when expanded out

$= \vec{x}^T A^T \; \vec{y}$

 We know that matrices are [associative](Properties%20of%20Matrices) so then the equation becomes

$= \vec{x}^T \; (A^T \; \vec{y})$

And because we mentioned earlier that the dot product is equivalent to multiplying a transposed vector against another vector the equation will finally look

$\vec{v} \cdot (A^T \; \vec{y})$

$\therefore \vec{x}^T \; (A^T \; \vec{y}) = \vec{v} \cdot (A^T \; \vec{y})$


## Can the transpose be invertible?
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/matrix-transpose/v/lin-alg-showing-that-a-transpose-x-a-is-invertible)

A matrix is considered invertible if its [a square matrix and its column vectors are linearly independent](Surjective%20and%20Injective%20Functions).

if matrix $A$ and $A^T$ are not a square matrix 

$A = \begin{bmatrix} | & | &  &  &  & | \\ \vec{a_1} & \vec{a_2} & . & . & . & \vec{a_n} \\ | & | &  &  &  & | \end{bmatrix}$

$A = n \times k \;\;\; A^T = k \times n$

then we can make a square matrix from [multiplying](Matrix%20Multiplication) $A^TA$ which then assuming all column vectors from the matrix $A^TA$ are [linear independent](Linear%20Independence) then the product matrix will be **invertible**

The reason why its invertible, is because, if matrix $A$ is already linearly independent then its [null space](Null%20space) will only have the $\vec{0}$

$A\vec{v} = \vec{0}$

meaning that the only way for matrix $A$ to equal a vector within the span of the $N(A)$ then it must be multiplied by the $\vec{0}$

And if $\vec{v}$ is a member of the null space of $A^TA$ and it result will be the $\vec{0}$

$\vec{v} \; \epsilon \; N(A^TA) => A^TA\vec{v} = \vec{0}$ 

Then $\vec{v}$ must also be a member of $N(A)$ which as stated previously $N(A) = Span(\vec{0})$ so then the $N(A^TA)$ is equivalent to the $N(A)$

$N(A^TA) = N(A) = Span(\vec{0})$

so therefore, matrix $A^TA$ is invertible under the assumption that its column vectors are linearly independent and its a square matrix

$(A^TA)\vec{x} = \vec{0}$

