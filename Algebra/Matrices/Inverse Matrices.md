[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-intro-to-matrix-inverses/v/inverse-matrix-part-1)
A **matrix inverse** is a calculation where it gets the direct opposite of any matrix $A$ which is known as $A^{-1}$. And when the equation $A \cdot A^{-1}$ is applied the result will be the identity matrix ($I_n$)

$A^{-1} \cdot A = I_n$
^inverseToIdentity

For a matrix to be invertible, it must follow the same rules for an [inverse function](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FInverse%20of%20a%20Function) which in translation for matrices the matrix **must** 

- be a square matrix ($n \times n$) 
- have its [determinant](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FDeterminant%20Matrices) $\ne 0$ 

The reason is if the equation $A^{-1} \; A = I_n$ were true then it must be [surjective and injective](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FSurjective%20and%20Injective%20Functions) meaning that the matrix's column vectors must be [linearly independent](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FLinear%20Independence) and must achieve [full rank](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FColumn%20Space) in both domain and co-domain of the transformation

So therefore, if the matrix is not a square matrix, then it cannot achieve full rank and if the determinant $= 0$ then the matrix is not linearly independent and therefore cannot span across its $R^n$ space.


## 2 x 2 Inverse Matrices
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-of-matrices/v/linear-algebra-formula-for-2x2-inverse)



Which is done by

$\begin{aligned} A = \begin{bmatrix} a & b \\ c & d \end{bmatrix} \\[1em] A^{-1} = {1 \over {ad - bc}} \cdot \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}\end{aligned}$
^gettingInverse2x2
![[Pasted image 20260728165702.png]]


which $ad - bc$ is just the [determinant](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FDeterminant%20Matrices) of $A$ so it be simplified to:

$A^{-1} = {1 \over {|A|}} \cdot \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$

Lets apply to actual matrix
![[Pasted image 20260601151252.png]]
![[Pasted image 20260601153611.png]]

now that we have our inverse matrix, when we multiply it to the original matrix: 
![[Pasted image 20260601153629.png]]


## Singular Matrix 

A square matrix with no inverse is called a **Singular Matrix**

What makes a singular matrix is if the [determinant](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FDeterminant%20Matrices) of the matrix is equal to $0$ which explained from a linear algebra stand point, either the slopes of each line **are parallel from each other** OR the **lines intersect infinitely giving no true definitative value**  

This is determined if the matrix has equal ratios for either side which can be describe as below:

$\begin{aligned} ad = bc \\[1em] {a \over b} = {c \over d} \\[1em] OR \\[1em]  {a \over c} = {b \over d}\end{aligned}$

this tells us that no matter what adjustments we make to vectors it will not being able to reach the end result vector. for instance:

$\begin{bmatrix} a & b \\ c & d \end{bmatrix} \cdot \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} e \\ f \end{bmatrix}$

which going through the equation we get:
$\begin{aligned} ax + by = e \\[1em] cx + dy = f \end{aligned}$

To visualize whats happening, lets put the equations in y-slope equations to find the intercept

$\Large y = {- ax + e \over b}$

$\Large y = {-cx + f \over d}$

So at the start if ${a \over c} = {b \over d}$ then the two slope equations above, when substituted with numbers, will be **on the same slope** because both lines are **parallel each other** and wont ever intersect if the equation holds true
![[Pasted image 20260602160831.png]]

In cases where ${e \over b} = {f \over d}$, the equation still holds true as while they'll intercept infinitely there is **no definitive intersection to draw from** 
![[Pasted image 20260602162726.png]]

looking at the above drawing, all the modifications we can apply to vectors $ac$ and $bd$ will just magnify or shrink it making it impossible to reach and intersection at $ef$

## Inverse 3x3 Matrix 
[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-determinants-and-inverses-of-large-matrices/v/inverting-matrices-part-3), [khan acad linear algebra vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-of-matrices/v/linear-algebra-deriving-a-method-for-determining-inverses)

##### Gaussian Elimination
One of the ways (and much easier) to find the inverse of a $3 \times 3$ matrix is the Gaussian Elimination method.

The method involves taking a matrix and putting it against an identity matrix

$\begin{bmatrix} 1 & -1 & -1 & | & 1 & 0 & 0 \\ -1 & 2 & 3 & | & 0 & 1 & 0 \\ 1 & 1 & 4 & | & 0 & 0 & 1\end{bmatrix}$

and apply [reduced row echelon](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FReduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to the augmented matrix until left side is the identity matrix which is just a [composition](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FComposition%20of%20Linear%20Transformations) of transformations which when applied, grant the inverse matrix result ($A^{-1}$)

$\begin{bmatrix} 1 & 0 & 0 & | & 5 & 3 & -1 &  \\ 0 & 1 & 0 & | & 7 & 5 & -2 \\ 0 & 0 & 1 & | & -3 & -2 & 1 \end{bmatrix}$
![[Pasted image 20260728152410.png]]
##### Standard way

The standard way is more long and a little more complex.

Take $A$:
$A = \begin{bmatrix} 1 & 4 & -2 \\ 2 & 1 & -3 \\ 5 & 2 & 1 \end{bmatrix}$

we first got to calculate the determinants of each value making the matrix looking like this. but how do we find the submatrix for each value?

| $\times$ | 1                                    | 2                                    | 3                                    |
| -------- | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| **1**    | ![[Pasted image 20260604161101.png]] | ![[Pasted image 20260604161141.png]] | ![[Pasted image 20260604161215.png]] |
| **2**    | ![[Pasted image 20260604161311.png]] | ![[Pasted image 20260604161411.png]] | ![[Pasted image 20260604161520.png]] |
| **3**    | ![[Pasted image 20260604161619.png]] | ![[Pasted image 20260604161702.png]] | ![[Pasted image 20260604161759.png]] |
^submatrixDeterminants


![[Pasted image 20260604152411.png]]

from we calculate each individual determinant:
![[Pasted image 20260604152649.png]]


Next we need to adjust the matrix to a cofactor matrix, which is essentially a checkered board pattern of $+$ and $-$ which for each value in the determinant matrix we calculated we do scalar multiplication for each factor:

$cofactor \; matrix = \begin{bmatrix} + & - & + \\ - & + & - \\ + & - & + \end{bmatrix}$


![[Pasted image 20260604160828.png]]

So now we have to find the [determinant of the original matrix](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FDeterminant%20Matrices) :
![[Pasted image 20260604165932.png]]
so now we can finally apply the inverse equation which is similar to the $2 \times 2$ matrix one except we use an **adjugate** of the transpose of the co-factor matrix which is where the **rows** of matrix becomes the **columns**:

$\begin{aligned} A = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix} \\[1em] adj(A) = \begin{bmatrix} a & d & g \\ b & e & h \\ c & f & i \end{bmatrix} \end{aligned}$

which then leaves us the overall equation of:
$\begin{aligned} \\[1em] A^{-1} = {1 \over {|A|}} \cdot adj(C)\end{aligned}$

![[Pasted image 20260604165943.png]]