[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-determinant-of-2x2-matrix/v/finding-the-determinant-of-a-2x2-matrix)

The **determinant** of a matrix is a special scalar number that can only be calculated through square matrices ($2 \times 2$, $3 \times 3$, $4 \times 4$, etc) 

## $2 \times 2$ Matrix Determinant

For the average $2 \times 2$ matrix you multiply each opposites and minus them
$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$

$a \cdot d - b \cdot c = determinant$ 

which is represented by this layout $|A|$ 
![[Pasted image 20260601142835.png]]
![[Pasted image 20260601143040.png]]

## 3x3 Matrix Determinant

##### The Standard Way
[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-determinants-and-inverses-of-large-matrices/v/finding-the-determinant-of-a-3x3-matrix-method-2)

finding the determinant of a $3 \times 3$ matrix is a bit more complicated. The standard method is if we have a $3 \times 3$ matrix:

$A = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix}$

First we must do a checked like layout of $+$ and $-$  for each column.

This creates the final equation for solving the determinant which is:

$det = a \cdot \begin{bmatrix} e & f \\ h & i \end{bmatrix} - b \cdot \begin{bmatrix} d & f \\ g & i \end{bmatrix} + c \cdot \begin{bmatrix} d & e \\ g & h \end{bmatrix}$

but how do we create our final equation?

breaking it down, all of the **first row** in $A$ are defined as **scalars** which will be multiplied against sub matrices created from **rows 2 and 3**      

To create the submatrices, we start with the first scalar and go to the value **diagonally opposite** which creates the top right value in the first submatrix. from there, the values **right, down and diagonally opposite** from the first value in submatrix creates the rest of it leaving with:

$a \cdot \begin{bmatrix} e & f \\ h & i \end{bmatrix}$

lets follow steps with a real example
![[Pasted image 20260603150630.png]]
![[Pasted image 20260603150743.png]]
![[Pasted image 20260603150830.png]]
To which from there you find the determinant:
![[Pasted image 20260603151325.png]]

##### The Short Way
[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-determinants-and-inverses-of-large-matrices/v/finding-the-determinant-of-a-3x3-matrix-method-1)

There's another way to find the determinant which is shorter than the standard method. To start we have our matrix:
$A = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix}$

We take the **first two columns** of the matrix and **add them at the end of it**:

$A = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix} \; \color{#96f2d7}\begin{matrix} a \\ d \\ g \end{matrix} \;\; \color{#d0bfff}\begin{matrix} b \\ e \\ h\end{matrix}$

From here, we are able to create 2 sets of equations, one $+$ and one $-$ which will be applied to each other. 

To start lets get out positive equation which is done by grabbing the values diagonally from top left to bottom right **3 times**:

$A = \begin{bmatrix} {\color{#96f2d7}a} & {\color{#d0bfff}b} & {\color{#96f2d7}c} \\ d & {\color{#96f2d7}e} & {\color{#d0bfff}f} \\ g & h & {\color{#96f2d7}i} \end{bmatrix} \; \begin{matrix} a \\ {\color{#96f2d7}d} \\ {\color{#d0bfff}g} \end{matrix} \;\; \begin{matrix} b \\ e \\ {\color{#96f2d7}h}\end{matrix}$

$pe = (a \cdot e \cdot i) + (b \cdot f \cdot g) + (c \cdot d \cdot h)$

and our negative equation is like the positive but reversed, start at the top left and grab all values **diagonal to the starting** value 3 times:


$A = \begin{bmatrix} {a} & {b} & {\color{#ffd8a8}c} \\ d & {\color{#ffd8a8}e} & {\color{#a5d8ff}f} \\ {\color{#ffd8a8}g} & {\color{#a5d8ff}h} & {\color{#ffd8a8}i} \end{bmatrix} \; \begin{matrix} {\color{#a5d8ff}a} \\ {\color{#ffd8a8}d} \\ {g} \end{matrix} \;\; \begin{matrix} {\color{#ffd8a8}b} \\ e \\ {h}\end{matrix}$

$ne = -(c \cdot e \cdot g) - (a \cdot f \cdot h) - (b \cdot d \cdot i)$

which then we can find our determinant:

$det = pe - ne$

now lets apply to a real example: 
![[Pasted image 20260603124348.png]]
![[Pasted image 20260603124750.png|697]]
![[Pasted image 20260603125142.png]]

which gives us:
![[Pasted image 20260603151409.png]]

