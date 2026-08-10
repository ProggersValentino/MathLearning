[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/lin-trans-examples/v/linear-transformation-examples-rotations-in-r2)

Rotational linear transformations, in mathematics, is the rotation of any $\vec{x}$ in a **counter-clockwise direction** by $\theta$ **degrees** which follows the notation of 

$Rot\theta(\vec{x})$

In [handedness ruling](Coordinate%20Spaces), the mathematics follows a **right-handed coordinate** as the positive rotations happen counter-clockwise. If a rotational linear transformation was happening in a left handed coordinate space then the positive rotation would be happening in a clockwise direction

![[Linear Algebra/Vectors & spaces/Coordinate Spaces#^angleHandednessRule]]

Rotational linear transformations are linear transformations as they [satisfy the two rules](Function) that all linear transformation must follow. 

If we take $Rot\theta(\vec{x} + \vec{y}) = Rot\theta(\vec{x}) + Rot\theta(\vec{y})$ and apply we see that the statement remains true: 
![[Pasted image 20260716190404.png]]

likewise if we try $Rot\theta(c \; \vec{x}) = c \; Rot\theta(\vec{x})$ we'll see that this statement is also true:
![[Pasted image 20260716190643.png]]

So now its confirmed that rotational linear transformations are indeed linear transformations, we know that they can be represented as [matrix vector products](Matrix%20vector%20products) which means we can represent the transformation as:

$Rot\theta(\vec{x}) = A \cdot \vec{x}$

## Rotations in $R^2$

If we want to map any vector to a rotation in $R^2$

$Rot\theta \; : \; R^2 \rightarrow R^2$

Then we need to find the image of $I_2$ under the rotation transformation which extends to finding the images of the basis vectors within the columns of $I_2$:

$I_2 = [\vec{e_1}, \vec{e_2}]$

Which all boils down to the trigonometry identities
![[Pasted image 20260716202621.png]]

In the image above, we are graphing $I_2 = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$ which to help solve, we can break down the result of the image by splitting each column vector into its own rotation transformation:
![[Pasted image 20260716202959.png]]

And when we apply a rotation transformation to each vector, as mentioned earlier, its counter-clockwise. Because we are dealing with unit vectors, when rotating, all hypotenuses will equal $1$. 

To solve $\vec{e_1}$, we can create a right-angled triangle by connecting a line from the head of the vector to $x$-axis base which will be the $opposite$. 

We need to figure out the $x$ and $y$ components which for $x$ component we can see that its $adjacent$ to the angle, which is the $cos\theta$ as ${a \over 1} = Cos\theta$ so that means our $x$ component is $cos\theta$.

For our $y$ component, we can see that the $opposite$ goes in the same direction as our $y$ which ${o \over 1} = Sin\theta$ our $y$ component is $sin\theta$ making the final image for $\vec{e_1}$:
![[Pasted image 20260716204455.png]]

For $\vec{e_2}$ is follows similar direction except now the $adjacent$ and $opposite$ have switched making the final image for $\vec{e_2}$:
![[Pasted image 20260716204603.png]]

Which finally, the image of $I_2$ under the rotation transformation is:

$Rot_{\theta}(\vec{x}) = \begin{bmatrix} cos\theta & -sin\theta \\ sin\theta & cos\theta \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$

So now any angle we want substitute in for $\theta$ we evaluate all the sines and cosines which then are multiplied against each vector within a subset

## Rotation in $R^3$
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/lin-trans-examples/v/rotation-in-r3-around-the-x-axis)

Rotation in $R^3$ becomes a lot complicated as now we have to combine 3 separate rotations on the $x,y,z$ axis to find the rotation:

$3\; Rot\theta \; : \; R^3 \rightarrow R^3$

To find out the rotation result for each vector, we'll need to find the image of $I_3$ under the $3Rot\theta$. 

The process to finding the image is the same as if were to do it in $R^2$ except the image depends on what axis is being rotated.

How the rotation of axis works is whatever axis you want to rotate on, its direction stays the same and the other two axis change based on the rotation. 

So if we want to rotate on the $x$-axis then the $y$ and $z$-axis vector directions will change

To figure out the image for rotating on the $x$-axis, we'll do what we did previously by taking $I_3$ and breaking it into $3$ different transformations to make it easier to figure out:  
![[Pasted image 20260717123800.png]]

so then because we're figuring out rotation on the $x$-axis, $\vec{e_1}$ and the $x$ components in the other axis do not change so the matrix will already look like:

$A = \begin{bmatrix} 1 & 0 & 0 \\ 0 & - & - \\ 0 & - & - \end{bmatrix}$

Which now we can figure out the $y$ and $z$ directions. 
![[Pasted image 20260717124619.png]]

So then we apply our rotations being counter-clockwise because we're dealing in right-handed coordinate space, and apply the same process we did in $R^2$ where we figure out whether the $y$ and $z$ components are $sine$ or $cosine$ which then the final result will look like:
![[Pasted image 20260717124920.png]]

So now any vector we want to rotate on the $x$-axis, we apply this image under the $3Rot\theta$ transformation

