[game math 6.4](https://gamemath.com/book/matrixmore.html#homogeneous_matrices)

4D vectors that work in 3 dimensional space have four components which the first 3 are the standard $x, y, z$ and then a fourth one $w$ which is generally referred as the homogeneous coordinate.

To better understand, we'll explain using homogeneous coordinates in 2D. If we have homogeneous coordinates in 2D, it can be represented as $(x, y, w)$ where $w = 1$ meaning that any point in 2D $(x, y)$ can be represented in the homogeneous space of $(x,y,1)$.

Any point that is not on the $(x,y)$ plane can be projected onto the plane $w=1$ by dividing by $w$ mapping the homogeneous coordinate to physical 2D point $(x/w, y/w)$ 

![[Pasted image 20260907124118.png]]

Any given 2D physical point has an infinite number of corresponding points in homogeneous space given the form of $(kx, ky, k)$ where $k \ne 0$ which form a line through the homogeneous origin. 

if $w = 0$ then the point cannot be mapped as a physical 2D point but is left undefined. however, this is generally referred the point to infinity within the 2D homogenous space defining direction instead of specific location.

This provides the elaborate distinction where **points** are any homogeneous coordinate where $w \ne 0$ and **vectors** are any homogeneous coordinate where $w = 0$

The same idea applies to 3D physical space and 4D homogeneous space where physical points lie on the hyperplane in $w = 1$ and any 4D homogeneous point can be projected onto the hyperplane by dividing by $w$ giving the equation: $(x/w, y/w, z/w)$. Therefore, any 4D homogeneous point that has $w = 0$ is a representation of direction. 

4D space unlocks the ability to perform affine transformations which involves being to perform translation of an object and other linear transformations simultaneously. 

## 4 x 4 Translation Matrices

As you know, the standard $3 \times 3$ transformation matrices represent [linear transformation](Matrix%20vector%20products) but cannot do translation because translation is an affine transformation. So then we use $4 \times 4$ matrices to apply translation to linear transformations which adds $\vec{w}$ to the matrix, which for now $w = 1$:

$\begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix} \Rightarrow \begin{bmatrix} a_{11} & a_{12} & a_{13} & 0 \\ a_{21} & a_{22} & a_{23} & 0 \\ a_{31} & a_{32} & a_{33} & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix}$

so now if we apply a 4D vector $(x,y,z,1)$ by the $4 \times 4$ matrix, the result will be same as the standard $3\times3$ matrix multiplication with just the extra coordinate $w$:

$A\vec{x} = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} \hspace{1em} \Leftrightarrow \hspace{1em} \begin{bmatrix} a_{11} & a_{12} & a_{13} & 0 \\ a_{21} & a_{22} & a_{23} & 0 \\ a_{31} & a_{32} & a_{33} & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ 1 \end{bmatrix}$

$= [a_{11}x_1+a_{12}x_2+a_{13}x_3+0, \;\;\;\;\;\;\;a_{21}x_1+a_{22}x_2+a_{23}x_3+0, \;\;\;\;\;\;\;a_{31}x_1+a_{32}x_2+a_{33}x_3+0, \;\;\;\;\;\;\;1]$


This unlocks the ability to apply translation within a 3 dimensional space where the last column ($\vec{w}$) pertains the translation vector so that if we multiply it by a vector, it will apply the linear transformation **plus** translation:

$T\vec{x} = \begin{bmatrix} 1 & 0 & 0 & \triangle x \\ 0 & 1 & 0 & \triangle y \\ 0 & 0 & 1 & \triangle z \\ 0 & 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ 1 \end{bmatrix} = \begin{bmatrix} x_1\cdot 1 + x_2\cdot 0 + x_3\cdot 0 + 1 \cdot \triangle x \\ x_1\cdot 0 + x_2\cdot 1 + x_3\cdot 0 + 1 \cdot \triangle y \\ x_1\cdot 0 + x_2\cdot 0 + x_3\cdot 1 + 1 \cdot  \triangle z \\ x_1 \cdot 0 + x_2 \cdot 0 + x_3 \cdot 0 + 1 \cdot 1 \end{bmatrix} = \begin{bmatrix} x_1 + \triangle x \\ x_2\ + \triangle y \\ x_3 + \triangle z \\  1 \end{bmatrix} = T\vec{x} + \vec{t}$

This matrix multiplication is still a [linear transformation](Matrix%20vector%20products) as the transformation is just applying a shearing action in 4D space to displace the points in the 3D physical space and still pass through the origin. 

The $w$ component of the 4D can be used as a selective way to switch on/off translation, so if our coordinate vector we're applying to the matrix has a $w$ component of $w = 0$ then the result will be just the linear transformation and no translation applied, this is otherwise known as our direction vector

$\begin{bmatrix} 1 & 0 & 0 & \triangle x \\ 0 & 1 & 0 & \triangle y \\ 0 & 0 & 1 & \triangle z \\ 0 & 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ 0 \end{bmatrix} = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\  0 \end{bmatrix}$

And vice versa, if the $w$ component $w = 1$ then the result will be a linear transformation with a translation being applied otherwise known as our destination points:

$\begin{bmatrix} 1 & 0 & 0 & \triangle x \\ 0 & 1 & 0 & \triangle y \\ 0 & 0 & 1 & \triangle z \\ 0 & 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ 1 \end{bmatrix} = \begin{bmatrix} x_1 + \triangle x \\ x_2\ + \triangle y \\ x_3 + \triangle z \\  1 \end{bmatrix}$


## General Affine Transformations

With the $4 \times 4$ matrices, we are now able to perform all linear transformations into affine transformations where the axis does not pass through the origin which includes:
- Rotation
- Scale
- Reflection
- Orthographic projection

The process follows with:

1.  Moving the transformation's local space back to the origin of the world space ($T^{-1}$)
2. Apply the set linear transformation/s to the target transformations (rotation, scale, reflection etc) ($R \rightarrow linear \; transformation$)
3. Translate the transformation's local space back to its original location in the world space ($T$)

So then the overall [composition of transformations](Composition%20of%20Linear%20Transformations) looks like:

$T \circ R \circ T^{-1} = TRT^{-1}\vec{x} = T(R(T^{-1}(\vec{x})))$

$T = \begin{bmatrix} 1 & 0 & 0 & -\triangle x \\ 0 & 1 & 0 & -\triangle y \\ 0 & 0 & 1 & -\triangle z \\ 0 & 0 & 0 & 1 \end{bmatrix} \hspace{1em} R_{4\times4} = \begin{bmatrix} a_{11} & a_{12} & a_{13} & 0 \\ a_{21} & a_{22} & a_{23} & 0 \\ a_{31} & a_{32} & a_{33} & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix} \hspace{1em} T^{-1} = \begin{bmatrix} 1 & 0 & 0 & \triangle x \\ 0 & 1 & 0 & \triangle y \\ 0 & 0 & 1 & \triangle z \\ 0 & 0 & 0 & 1 \end{bmatrix}$

Which as you can see, the linear transformation always happens in the middle of composition while the translations will be the first and last set of transformations that transform an object.

This is because, the [inverse](Inverse%20Matrices) of our translation will "center" the transformation back to the world origin and then the appropriate linear transformation is applied which then the final translation moves the transformation back to its original location in world space



