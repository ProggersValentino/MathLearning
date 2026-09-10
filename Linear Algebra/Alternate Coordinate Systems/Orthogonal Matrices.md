[game math 6.3](https://gamemath.com/book/matrixmore.html#orthogonal_matrices)

An orthogonal matrix is a square matrix where all the vectors within the matrix are [orthonormal](Orthonormal%20Bases). Like for instance the identity matrix:
$A = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$


A matrix is said to be orthogonal **if and only if** the product of the matrix and its [transpose](Transposing) equals the identity matrix:

$A^TA = I$

The transpose of a matrix presents to be a powerful representation of the [inverse matrix](Inverse%20Matrices) simplifying a lot of computations where the inverse matrix is required to solve it.

Any square matrix can become orthogonal, if its not already, using the [Gram-Schmidt process](Gram-Schmidt%20Process) allowing us to access the benefits of an orthogonal matrix

## Geometric Interpretation



## Orthogonal Matrices Preserve Angles and Lengths
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/lin-alg-orthogonal-matrices-preserve-angles-and-lengths)



```desmos-graph-3d

(1t, 0t, 0t)|0 <= t <= 1 | RED

(0t, 1t, 0t)|0 <= t <= 1 | GREEN

(0t, 0t, 1t)|0 <= t <= 1 | BLUE

```


Orthogonal Matrices have the unique property to preserve **angles** and **lengths** of vectors after a transformation has been made

### Length Proof
![[Pasted image 20260901214907.png]]

### Angle Proof
![[Pasted image 20260901214919.png]]