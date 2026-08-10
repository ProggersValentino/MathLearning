[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-determinant-of-2x2-matrix/v/finding-the-determinant-of-a-2x2-matrix)

The **determinant** of a matrix is a special scalar number that can only be calculated through square matrices ($2 \times 2$, $3 \times 3$, $4 \times 4$, etc) 

The determinant value represents if a matrix can be [invertible](Inverse%20Of%20a%20Function) by determining if its [linearly independent](Linear%20Independence) 
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

##### The Short Way - Rule of Sarrus of Determinants
[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-determinants-and-inverses-of-large-matrices/v/finding-the-determinant-of-a-3x3-matrix-method-1), [khan acad vid linear algebra](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-of-matrices/v/linear-algebra-rule-of-sarrus-of-determinants)

The rule of Sarrus is a quicker way to solve the determinant compared to the standard way  

 To start we have our matrix:
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

## n x n Matrix Determinant
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-of-matrices/v/linear-algebra-nxn-determinant)

When solving for a matrix greater than $n \times n$ you have to recursively break down the matrix into submatrices until you are able to solve the determinant using the standard or short way.

![[Pasted image 20260728205634.png]]

$det(A) = a_{11}|A_{11}| - a_{12}|A_{12}| + a_{13}|A_{13}| -+ ... \pm \; a_{1n}|A_{1n}|$
$det(A_{11}) = b_{11}|B_{11}|$
$...$

This is otherwise known as a **recursive formula** where you're repeating the same calculation until you achieve the result 

for instance if we have a $4 \times 4$ matrix:

$A = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 1 & 0 & 2 & 0 \\ 0 & 1 & 2 & 3 \\ 2 & 3 & 0 & 0 \end{bmatrix}$

Then we can apply the determinant formula recursively until we are able to calculate it using the standard way:
![[Pasted image 20260728210857.png]]![[Pasted image 20260728210902.png]]
![[Pasted image 20260728210909.png]]

which now we know that matrix $A$ is invertible

### Determinants on other rows
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-of-matrices/v/linear-algebra-determinants-along-other-rows-cols)

When solving determinants you can choose freely what row you want to work with to find the determinant like instance, in the matrix $A$

$A = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 1 & 0 & 2 & 0 \\ 0 & 1 & 2 & 3 \\ 2 & 3 & 0 & 0 \end{bmatrix}$

We can see that row 4 only has two numbers and the rest are zeros cutting the workload in half to figure out the determinant

However, the equation that forms is a little different in signage

$det(A) = -2 det(A_{11}) + 3 det(A_{12})$

The reason is because, like the top row which follows an alternating pattern of $+$ and $-$, the whole matrix applies the same concept in a checker board pattern of signs, otherwise known as a **co-factor matrix**:

$cofactor \; matrix = \begin{bmatrix} + & - & + & - \\ - & + & - & + \\ + & - & + & - \\ - & + & - & + \end{bmatrix}$

Which then depending on the row and column we choose alternates the signage of the final equation.

An easy way to determine the signage of a number in the matrix is by applying:

$sign(i,j) = (-1)^{i+j}$

where $i$ and $j$ represent the row and column position of a specific number.

So going back to using our 4th row for find the determinant of $A$ we can verify that the $2$ signage by applying 

$sign(4, 1) = (-1)^{4 + 1} = -1$


## Rows multiplied by a scalar
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/determinant-depth/v/linear-algebra-determinant-when-row-multiplied-by-scalar)

When multiplying a row within the matrix, the determinant calculation changes a little bit. 

If we have:
$A = \begin{bmatrix} a & b \\ kc & kd \end{bmatrix}$

then using algebra to extract the formula, it simplifies to 

$det(A) = kad - kbc = k(ad-bc) = k |A|$

this is not the same as $det(kA)$ because $kA$ is multiplying the whole matrix by $k$ 

$kA = \begin{bmatrix} ka & kb \\ kc & kd \end{bmatrix}$

which if we expand the formula it becomes

$det(kA) = kakd - kbkc = k^2ad - k^2bc = k^2(ad-bc) = k^2 |A|$

as you can see, the formula leaves us with multiplying the determinant by $k^2$

## Adding a row
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/determinant-depth/v/linear-algebra-determinant-when-row-is-added)

You can find the determinant of a matrix where one of its rows is the sum product of two other matrices:
![[Pasted image 20260730114027.png]]

Given that all other matrices have the exact same rows except for the row that is being summed together. For matrices $X, Y, Z$ we see that the first row is all the same with $a, b$ and then the second row is different, which then it can be determined that:

$det(X) + det(Y) = det(Z)$

![[Pasted image 20260730114526.png]]

However, its important to note that

$Z = X + Y \ne det(Z) = det(X) + det(Y)$

$det(Z) = det(X) + det(Y)$ only works when only the same 1 row is different and **every other** row is the same across the matrices $X,Y,Z$

So it is not true if all other rows are different across the matrices 

This is especially prominent in row operations where a scalar multiple of a row vector within matrix $A$ is applied within matrix $B$ to achieve a different result but will create a duplicate row instead. 

## Duplicate Determinants
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/determinant-depth/v/linear-algebra-duplicate-row-determinant)

If a row is swapped within a matrix then its determinant calculation will result in the opposite 

$row \; swap = det(A) = -det(A)$

However, if the row that is swapped is a duplicate then nothing happens and the result of the determinant will be the same. 

With this, it does mean that the two identical rows make the matrix [linear dependent](Linear%20Independence) because there is another matrix within the subset of vectors that can be made from other linear combinations of the rest of the subset. 

So therefore, we can determine that if there is a duplicate row within the matrix then the determinant result will always be equal to $0$

$Duplicate \; row => det(A) = 0$

## Upper Triangular Determinant
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/determinant-depth/v/linear-algebra-upper-triangular-determinant)

Upper triangular matrices are where a lower diagonal half of a matrix is zeros

$A = \begin{bmatrix} a & b & c \\ 0 & e & f \\ 0 & 0 & i \end{bmatrix}$

This allows us to solve a matrix using the **upper triangle matrix** where all values that go diagonally across the center are multiplied together to get the determinant

$det(A) = aei$

the reason this is because, if we use the standard way of finding the determinant

$det(A) = a \cdot \begin{bmatrix} e & f \\ 0 & i \end{bmatrix} - b \cdot \begin{bmatrix} 0 & f \\ 0 & i \end{bmatrix} + c \cdot \begin{bmatrix} 0 & e \\ 0 & 0 \end{bmatrix}$

$det(A) = a(ei) - b(0) + c(0)$

you'll notice the other submatrix determinants are $0$ leaving the final result of $det(A) = aei$

So therefore, if a matrix is represented in a upper triangular form, then the determinant of that matrix can be found using the values diagonal across the center multiplied by each other.

for instance:

$A = \begin{bmatrix} 7 & 3 & 4 & 2 \\ 0 & -2 & 3 & 6 \\ 0 & 0 & 1 & 7 \\ 0 & 0 & 0 & 3 \end{bmatrix}$

$det(A) = 7 \cdot (-2) \cdot 1 \cdot 3 = -42$

$\therefore det(A) = -42$

So this can be used to solve the determinant of matrices especially if we have a matrix larger than a $3 \times 3$, for instance if we have a $4 \times 4$ matrix:

$A = \begin{bmatrix} 1 & 2 & 2 & 1 \\ 1 & 2 & 4 & 2 \\ 2 & 7 & 5 & 2 \\ -1 & 4 & -6 & 3 \end{bmatrix}$

We can use [matrix row operations](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to turn it into an upper triangular matrix
![[Pasted image 20260803122009.png]]

so then after its put into upper triangular form the determinant can be solved:
$-(1 \cdot 3 \cdot 2 \cdot 7) = -42$

$\therefore det(A) = -42$



## Determinant as Scaling factor
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/determinant-depth/v/linear-algebra-determinant-as-scaling-factor)

The determinant can also be used as a scaling factor for when we apply [linear transformations to a subset of vectors](Image%20of%20a%20subset%20under%20a%20transformation)

For instance, given the vectors:
$\vec{a} = \begin{bmatrix} 0 \\ 0 \end{bmatrix} \;\;\; \vec{b} = \begin{bmatrix} k_1 \\ 0 \end{bmatrix} \;\;\; \vec{c} = \begin{bmatrix} k_1 \\ k_2 \end{bmatrix} \;\;\; \vec{d} = \begin{bmatrix} 0 \\ k_2 \end{bmatrix}$

Where a rectangle can be create from joining together each vector
![[Pasted image 20260803185732.png]]

From this rectangle, if we were to solve for its area it would follow the formula

$Area = k_1 \cdot k_2$

because the length is the $x$-component and the width is the $y$-component which vectors $\vec{d}, \vec{b}$ fulfill

Which then we want to transform the rectangle by matrix $A$

$\begin{aligned} T: \; R^2 \rightarrow R^2 \\[1em] T(\vec{x}) = \begin{bmatrix} a & b \\ c & d \end{bmatrix} \vec{x} \end{aligned}$

We'll calculate the transformations for each vector
![[Pasted image 20260803190444.png]]

which provides the final image of the rectangle under $T$ transforming into a parallelogram
![[Pasted image 20260803190555.png]]

The transformation matrix would be represented as  

$Im(Rec) = \begin{bmatrix} k_1a & k_2b \\ k_1c & k_2d \end{bmatrix}$

And if we want to find the [area of this parallelogram](Area%20of%20Parallelogram%20using%20Determinant), we would need to find the absolute of the determinant of matrix $A$ which looks like

$|det(Im(Rec))| = |k_1k_2ad - k_1k_2bc|$

and can be simplified to 

$|k_1k_2 \; (ad-bc)| = |k_1k_2 \;\; det(Im(Rec))|$

$\therefore area \; of \; Im(Rec) = |k_1k_2 \; det(Im(Rec))|$

Which if we were to pull apart the formula, it is just the area of a rectangle **scaled** by the determinant of the transformation matrix which is the [area of this parallelogram](Area%20of%20Parallelogram%20using%20Determinant) on its own