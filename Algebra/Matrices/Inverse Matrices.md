[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-intro-to-matrix-inverses/v/inverse-matrix-part-1)

As we've seen with identity matrices
![[Algebra/Matrices/Identity Matrix#What is an Identity Matrix|Identity Matrix]]

and we know that $I_n \cdot A = A$ and vice versa if a square matrix each calculation done with an identity matrix and regular matrix always equals the regular matrix but there is a way to get the identity matrix and that is the **inverse matrix**

$A^{-1} \cdot A = I_n$
^inverseToIdentity

Which is done by

$\begin{aligned} A = \begin{bmatrix} a & b \\ c & d \end{bmatrix} \\[1em] A^{-1} = {1 \over {ad - bc}} \cdot \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}\end{aligned}$
^gettingInverse2x2

which $ad - bc$ is just the determinant of $A$ so it be simplified to:

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
[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-determinants-and-inverses-of-large-matrices/v/inverting-matrices-part-3)

##### Gaussian Elimination
One of the ways (and much easier) to find the inverse of a $3 \times 3$ matrix is the Gaussian Elimination method.

The method involves taking a matrix and putting it against an identity matrix

$\begin{bmatrix} 1 & 4 & -2 & | & 1 & 0 & 0 \\ 2 & 1 & -3 & | & 0 & 1 & 0 \\ 5 & 2 & 1 & | & 0 & 0 & 1\end{bmatrix}$

and applying matrix row operations to matrix and the identity matrix until you get an identity matrix on the left which then on the right will be the inverse matrix:

![[Reduced Row Echelon with Matrix Row Operations#^rowOperationTable]]


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

$cofactor matrix = \begin{bmatrix} + & - & + \\ - & + & - \\ + & - & + \end{bmatrix}$


![[Pasted image 20260604160828.png]]

So now we have to find the [determinant of the original matrix](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FDeterminant%20Matrices) :
![[Pasted image 20260604165932.png]]
so now we can finally apply the inverse equation which is similar to the $2 \times 2$ matrix one except we use an **adjugate** of the transpose of the co-factor matrix which is where the **rows** of matrix becomes the **columns**:

$\begin{aligned} A = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix} \\[1em] adj(A) = \begin{bmatrix} a & d & g \\ b & e & h \\ c & f & i \end{bmatrix} \end{aligned}$

which then leaves us the overall equation of:
$\begin{aligned} \\[1em] A^{-1} = {1 \over {|A|}} \cdot adj(C)\end{aligned}$

![[Pasted image 20260604165943.png]]