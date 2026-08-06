[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/linear-transformations/v/matrix-vector-products-as-linear-transformations)

A matrix vector product is equivalent to a [linear transformation](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FFunction) where we are **transforming** a vector to a new vector with a [linear combination](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FLinear%20Combination%20and%20span) of a given coordinate vector with a group of basis vectors. 

![[Pasted image 20260710141830.png]]

For instance say we have:
$B = \begin{bmatrix} 2 & -1 \\ 3 & 4 \end{bmatrix}$

![[Pasted image 20260710143259.png]]

we can see that the transformation defined is just [matrix multiplication](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FMatrix%20Multiplication)

But is it a **Linear Transformation?**

If we try to apply the two necessary rules of linear transformations, we'll find that they align directly with [properties of matrix multiplication](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FProperties%20of%20Matrices) being that they are distributive fulfilling the two rules:

![[Pasted image 20260710144338.png]]

Therefore, matrix product with vectors are **ALWAYS** a linear transformation
^linearTwithMatrices

## Linear Transformations as matrix vector products
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/linear-transformations/v/linear-transformations-as-matrix-vector-products)

We know that [identity matrices](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FIdentity%20Matrix) are a square matrix with 1s and 0s:
![[Algebra/Matrices/Identity Matrix#What is an Identity Matrix|Identity Matrix]]

And with linear transformations, these have a very unique property in that, if multiplied against any vector within the same $R^n$ then it will result in that vector:

![[Pasted image 20260713125731.png]]

Additionally, **identity matrices** are generally referred to as [basis vectors](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FLinear%20Subspaces), more specifically orthonormal basis vectors. 

Which if we look at each individual column vector within of the identity matrix, its clear that each vector is perpendicular to the other vectors AND they are [linearly independent](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FLinear%20Independence) 

Therefore, we are able to construct any vector from the [linear combination](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FLinear%20Combination%20and%20span) with the identity matrix. 

![[Pasted image 20260713131228.png]]
So then putting it up against linear transformations, we are able to apply all linear transformations to any vectors 


All linear transformations can be represented as a matrix vector product
^linearTransformationVecProduct

For instance, if we want to transform a vector from $R^2$ to $R^3$ then we can use the identity matrix to define a translator layer to transform any vector from $R^2$ to $R^3$ given the [function definition](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FFunction):
![[Pasted image 20260713132617.png]]

Thus, the identity matrices can be used to create a transformation definition to apply any type of transformation to a vector.

## Sums and scalars multiples of linear transformations
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/linear-transformations/v/sums-and-scalar-multiples-of-linear-transformations)

We know that when taking a matrix product with vectors will always be a linear transformation, but what about when applying multiple transformations together, is that a linear transformation? 

$\begin{aligned} S:R^n \rightarrow R^m \;\;\;\; T:R^n \rightarrow R^m \\[1em] Def: \; (S + T)(\vec{x}) = S(\vec{x}) + T(\vec{x}) => (S + T):R^n \rightarrow R^m \\[1em] Def:\; (cS)(\vec{x}) = c(S(\vec{x})) \; => \; cS:R^n \rightarrow R^m \end{aligned}$

As you can see the definitions established above align with the **rules of linear transformation** and looking at it when we go in depth, we can show that these definitions are true:
![[Pasted image 20260715131115.png]]