[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/lin-trans-examples/v/linear-transformation-examples-scaling-and-reflections)

Previously, it was seen that [identity matrices](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FIdentity%20Matrix), when a linear transformation is applied to it, create an [image](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FImage%20of%20a%20subset%20under%20a%20transformation) under that transformation consisting the new basis vectors which when [linearly combined](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FDrawings%2Flinear%20combinations%20%26%20spans) with any subset of vectors transforms the image based of the subset.
## Diagonal Matrices
Diagonal matrices are matrices where only the positions from the top left to diagonally bottom right are filled with numbers and the rest are $0$s:

$Diagonal \; Matrix = \begin{bmatrix} -1 & 0\\ 0 & 2 \end{bmatrix}$

These matrices are used for various positional transformations like reflection and stretching  
### Reflection
Reflection is where a subset of vectors are flipped creating an image reflecting on either the $x$ or $y$-axis from the original positions of the subset. 

In diagonal matrix form, it is represented with a negative symbol as when a vector is multiplied it will flip it to either negative or positive depending on its original signage:

$Reflection = \begin{bmatrix} -1 & 0\\ 0 & -1 \end{bmatrix}$
![[Pasted image 20260716144202.png]]
### Stretching

stretching is where a subset of vectors are scaled on either axis' creating larger or smaller scaled image under the transformation.

In diagonal matrix form, its represented with whatever scalar number to multiply against the subset:
$y-axis \; stretch = \begin{bmatrix} 1 & 0\\ 0 & 2 \end{bmatrix}$
$x-axis \; stretch = \begin{bmatrix} 2 & 0\\ 0 & 1 \end{bmatrix}$
![[Pasted image 20260716150511.png]]

If we combine them, then we can get a more complex image, for instance say we have the subset of vectors with when joined create a triangle:
![[Pasted image 20260716150643.png]]

and we want to apply a reflection transformation on the $y$-axis and a stretch transformation in the $y$ direction by a scale of $2$:

$T(\begin{bmatrix} x \\ y \end{bmatrix}) = \begin{bmatrix} -x \\ 2y \end{bmatrix}$

which to create a basis for this transformation, we'll need to create an image from the identity matrix by multiplying against the transformation:

$\begin{aligned} A = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \cdot \begin{bmatrix} -1 \\ 2 \end{bmatrix} \\[1em] A = \begin{bmatrix} -1 & 0 \\ 0 & 2 \end{bmatrix} \end{aligned}$

which now we have the basis vectors of the identity matrix under the transformation, we can create images under the transformation by linearly combinate any subset of vectors:

![[Pasted image 20260716151845.png]]

outputting a final result of:
![[Pasted image 20260716151937.png]]

 