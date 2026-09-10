[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/eigen-everything/v/linear-algebra-introduction-to-eigenvalues-and-eigenvectors)

An Eigen Vector is a vector which **only scales along its span** when a transformation is applied to it. 
Eigen values is the scalar representation of how much an eigen vector has scaled. 
An Eigen space represents all the eigen vectors that correspond the eigen value 

Eigen vectors make interesting bases in that they can simplify some of computation needed to solve a transformation.

**Eigen vectors** are generally represented with the basis vector that represents the coordinate system its in

**Eigen Values** are generally represented with the lambda symbol ($\lambda$) which get substituted for a real-number that represents how much the Eigen vector has been scaled by

$T(\vec{x}) = \lambda\vec{v}_1$

**Eigen Spaces** are generally represented with the following symbol: $E_\lambda$ which means that all the possible eigen vectors can be represented within the space $\lambda$ which is evaluated using the null space of $\lambda I_n - A$:

$E_\lambda = N(\lambda I_n - A)$

For instance if we have two eigen vectors that form a basis for $R^2$ with a transformation that [maps](Function) to and from $R^2$ where it flips a vector across a set line which spans $[1, 2]$

$B = [\begin{bmatrix} 1 \\ 2 \end{bmatrix}, \begin{bmatrix} 2 \\ -1 \end{bmatrix}] \hspace{1em} B = basis \; for \; R^2 \hspace{2em} L = span(\begin{bmatrix} 1 \\ 2 \end{bmatrix})$

which can be visually represented below:
![[Pasted image 20260902174924.png]]

When a transformation occurs the eigen vectors go through no change in direction but may change in how much they're scaled by:
![[Pasted image 20260902175614.png]]

as you can see, after the transformation, the the eigen vector $\vec{v}_2$ doesn't change its direction but it eigen value changes to $-1$ to match with the mirror transformation so then:

$\lambda\vec{v} = -1\vec{v}_2$

## Eigen Bases are good coordinate systems
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/eigen-everything/v/linear-algebra-showing-that-an-eigenbasis-makes-for-good-coordinate-systems)

Eigen bases are a kind of basis where all the vectors are are eigen vectors:

$B = [\vec{v}_1, \vec{v}_2, ..., \vec{v}_n] = eigen \; basis \hspace{1em} where \; \vec{v}_1, \vec{v}_2, ... \vec{v}_n \; are \; L.I. \; eigen \; vectors$

and if all eigen vectors within the basis are [linearly independent](Linear%20Independence) and span all of at least the linear space we're in ($R^n$) then they are considered good coordinate systems to solve for transformations of $\vec{v}$ with [respect to a particular basis](Coordinates%20with%20respect%20to%20a%20basis) 

![[Pasted image 20260903175238.png]]

The reason is that, we know that the definition for each transformation can be boiled down to a linear combination of $\lambda$ with the eigen vector because $T(\vec{x}) = A\vec{x} = \lambda\vec{x}$:
![[Pasted image 20260903175158.png]]

So because we know that the transformations are a linear combination of $\lambda$ and $\vec{v}$, we can also define our transformation with respect to a particular basis the same way defining our matrix $D$ where:
![[Pasted image 20260903175617.png]]
![[Pasted image 20260903175629.png]]
## Determining Eigenvalues
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/eigen-everything/v/linear-algebra-proof-of-formula-for-determining-eigenvalues)

eigen values and vectors can be represented in matrix form for a linear transformation:

$T(\vec{v}) = A\vec{v} = \lambda\vec{v}$

We can figure out eigen values through our the determinant of $(\lambda I_n - A)$ meaning that 

$A\vec{v} = \lambda \vec{v}$ for non-zero $\vec{v}$'s $iff \; det(\lambda I_n - A) = 0$

There are two assumptions to be made for eigen vectors:

	$Assumption \; 1: \vec{v} \ne 0$
	$Assumption \; 2: A \; is \; n \times n$

We arrive to this conclusion after some manipulating of the equation we defined earlier: $A\vec{v} = \lambda \vec{v}$

Which we can start by shifting $A\vec{v}$ over to other side updating the equation to:

$\lambda \vec{v} - A\vec{v} = \vec{0}$

From here we can expand $\vec{v}$ that is connected to the lambda to a matrix equation of $I_n\vec{v}$ because anything vector multiplied by the [identity matrix](Identity%20Matrix) will just equal that exact vector. 

$\lambda I_n \vec{v} - A\vec{v} = \vec{0}$

Now that we have two matrix equations, and because matrix equations [distributable](Properties%20Of%20Matrices) and each equation has the vector $\vec{v}$, we can simplify the equation to wrap the matrix equation around $\vec{v}$ leaving us with the final equation:

$(\lambda I_n - A)\vec{v} = \vec{0}$

![[Pasted image 20260902185838.png]]

and interesting note from this equation is that when the matrix equation $\lambda I_n - A$ multiplies against $\vec{v}$ the result will be the $\vec{0}$. Which means that $\vec{v}$ is a member of the [null space](Null%20space) of $\lambda I_n - A$ 
![[Pasted image 20260902191358.png]]

which further indicates that $N(\lambda I_n - A)$ is non-trivial meaning that it contains more than just the $\vec{0}$ therefore creates the conclusion that the matrix $\lambda I_n - A$ must have [linearly dependent](Linear%20Independence) columns because it's null space contains other vectors than the $\vec{0}$ 

This further extends onto the matrix's inversibility meaning that matrix $\lambda I_n - A$ cannot be [invertible](Inverse%20Matrix) because its columns are linearly dependent which further means it's [determinant](Determinant%20Matrices) will equal $0$

## Example solving eigen values 2x2
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/eigen-everything/v/linear-algebra-example-solving-for-the-eigenvalues-of-a-2x2-matrix)

if we have matrix $A$ and we want to find its eigen values then we got to find the determinant of $\lambda I_n - A$:

$A = \begin{bmatrix} 1 & 2 \\ 4 & 3 \end{bmatrix} \hspace{1em} det(\lambda I_n - A) = 0$

which then we apply some algebra to find matrix we'll be finding the determinant:
![[Pasted image 20260902195335.png]]

from here we find the determinant of the matrix we found:

$det(\begin{bmatrix} \lambda - 1 & - 2 \\ -4 & \lambda - 3 \end{bmatrix})$

$\begin{aligned} det = ((\lambda -1 ) \cdot (\lambda - 3)) - (-4 \cdot -2) \\[1em] det = (\lambda - 1)(\lambda - 3) - 8 \end{aligned}$


from here we can expand and simplify the equation which will result in a **characteristic polynomial**:
![[Pasted image 20260902200215.png]]

From the equation is factorable leaving the final equation:

$(\lambda - 5)(\lambda + 1) = 0$

which if we apply the **zero-product property**, we finally solve that the eigen values for $A$ can be:

$\lambda = 5 \hspace{1em} OR \hspace{1em} \lambda = -1$

### Finding Eigen vectors and spaces 2x2
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/eigen-everything/v/linear-algebra-finding-eigenvectors-and-eigenspaces-example)

We can use eigen spaces to help solve for the eigen vectors given matrix $A$ has the eigen values of $5$ and $-1$ as solved earlier:

$A = \begin{bmatrix} 1 & 2 \\ 4 & 3 \end{bmatrix} \hspace{1em} \lambda = 5 \hspace{1em} OR \hspace{1em} \lambda = -1$

To figure out our eigen space ($E_\lambda$) for each eigen vector by substituting in and solving for the [null space](Null%20space) of $\lambda I_n - A$, which requires applying the [reduced row echelon](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to find our eigen space spans:

![[Pasted image 20260902213034.png]]

Which leaves with the final eigen spaces of:

$E_5 = Span(\begin{bmatrix} \frac{1}{2} \\ 1 \end{bmatrix}) \hspace{1em} E_{-1} = Span(\begin{bmatrix} -1 \\ 1 \end{bmatrix})$

Which when we try to visualize it, you'll see the two vectors which after a transformation will only impact they're scaling:
![[Pasted image 20260902213338.png]]


### Example 3x3

#### Find eigen values
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/eigen-everything/v/linear-algebra-eigenvalues-of-a-3x3-matrix)

If we have a $3 \times 3$ matrix $A$ and we want to find its eigen values then like the $2 \times 2$ case we must find the determinant of $\lambda I_n - A$

$A = \begin{bmatrix} -1 & 2 & 2 \\ 2 & 2 & -1 \\ 2 & -1 & 2 \end{bmatrix}$

So we start by find the matrix we have find the determinant which just simplifying $\lambda I_n - A$ into 1 matrix:

![[Pasted image 20260903134503.png]]

giving us the final result of:

$det( \begin{bmatrix} \lambda + 1 & -2 & -2 \\ -2 & \lambda - 2 & 1 \\ -2 & 1 & \lambda - 2 \end{bmatrix})$

From here we then find the [determinant](Determinant%20Matrices) of our new matrix which will result in a characteristic polynomial:

![[Pasted image 20260903134816.png]]

which from here we find attempt to find what number can substituted into the $\lambda$ and will produce the overall result of $0$ which can be found by going through the cofactors of a stand alone number in the polynomial which in this case is $27$:
![[Pasted image 20260903134945.png]]

which results in $3$ which then we can factorize the polynomial to find our final eigen values which are $\lambda = 3 \; OR \; \lambda = -3$
![[Pasted image 20260903135156.png]]

#### Finding the eigen vectors and spaces 3x3
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/eigen-everything/v/linear-algebra-eigenvectors-and-eigenspaces-for-a-3x3-matrix)

Now that we have our eigen values for matrix $C$ we are able to find our eigen vectors and space:

$C = \begin{bmatrix} \lambda + 1 & -2 & -2 \\ -2 & \lambda - 2 & 1 \\ -2 & 1 & \lambda - 2 \end{bmatrix} \hspace{1em} \lambda = 3 \hspace{1em} OR \hspace{1em} \lambda = -3$

from here we can substitute in each lambda and figure out our eigen spaces by once again finding the [null space](Null%20space) of our eigen values using the [reduced row echelon](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to which then it will result in our spans that each eigen value spans:
![[Pasted image 20260903162042.png|700]]

which when visualizing it, you'll see that all the vectors are orthogonal to each other:
![[Pasted image 20260903162203.png]]