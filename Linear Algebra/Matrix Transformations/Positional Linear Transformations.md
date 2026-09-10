[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/lin-trans-examples/v/linear-transformation-examples-scaling-and-reflections)

Previously, it was seen that [identity matrices](Identity%20Matrix), when a linear transformation is applied to it, create an [image](Image%20of%20a%20subset%20under%20a%20transformation) under that transformation consisting the new basis vectors which when [linearly combined](Linear%20Combination%20and%20span) with any subset of vectors transforms the image based of the subset.
## Diagonal Matrices
Diagonal matrices are matrices where only the positions from the top left to diagonally bottom right are filled with numbers and the rest are $0$s:

$Diagonal \; Matrix = \begin{bmatrix} -1 & 0\\ 0 & 2 \end{bmatrix}$

These matrices are used for various positional transformations like reflection and stretching  
### Reflection
Reflection is where a subset of vectors are flipped creating an image reflecting on either the $x$ or $y$-axis from the original positions of the subset. 

In diagonal matrix form, it is represented with a scalar of $-1$ as when a vector is multiplied it will flip to either negative or positive signage depending on its original state:

$Reflection = \begin{bmatrix} -1 & 0\\ 0 & -1 \end{bmatrix}$
![[Pasted image 20260716144202.png]]

If we want to reflect on an arbitrary axis $\hat{n}$ then we can substitute in $-1$ within $k$ of the scaling formula so then

$S(\hat{n}, -1) = \begin{bmatrix} 1 + (-1 - 1)n_x^2 & (-1 - 1)n_yn_x \\ (-1 - 1)n_xn_y & 1 + (1 - 1)n_y^2 \end{bmatrix}$
$S = \begin{bmatrix} 1 - 2n_x^2 & -2n_yn_x \\ -2n_xn_y & 1 - 2n_y^2 \end{bmatrix}$

This works as this is technically scaling the object in the opposite direction with the negative signage thus creating a reflection image with the subset of vectors.
### Stretching - Scaling

stretching is where a subset of vectors are scaled on either axis' creating larger or smaller scaled image under the transformation. There are two types of stretching that can be done to an object


| Scale type        | Meaning                                                                                                                                      | Example                                                                            |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Uniform Scale     | The object is scaled evenly preserving its angles and proportions                                                                            | $T(\begin{bmatrix} x \\ y \end{bmatrix}) = \begin{bmatrix} 2x \\ 2y \end{bmatrix}$ |
| non-uniform Scale | The object is scaled unevenly where the object's angles and proportions are not preserved creating a stretched and warped look to the object | $T(\begin{bmatrix} x \\ y \end{bmatrix}) = \begin{bmatrix} x \\ 2y \end{bmatrix}$  |

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

### Scaling on Arbitrary Direction 
[game math chpt 5.2.2](https://gamemath.com/book/matrixtransforms.html#scale_arbitrary_axis)

To scale vectors within an arbitrary direction $\hat{n}$, the arbitrary direction must be defined by directly going parallel to the scaling direction we want to set. 

So if we want the vector to be scaled in the direction $T(\begin{bmatrix} x \\ y \end{bmatrix}) = \begin{bmatrix} x \\ 2y \end{bmatrix}$ then $\hat{n}$ will be a unit vector parallel to the direction $\begin{bmatrix} x \\ 2y \end{bmatrix}$ 
![[Pasted image 20260813140809.png]]

We'll also have $k$ being the coefficient that the vector is getting scaled in the direction of 

Now, we must break down the vector we're finding its scaled form to the vector combination that makes up $\vec{v}$ from the linear slope which can be denoted as

$\vec{v} = \vec{v}_\parallel + \vec{v}_\perp$ 

The vector parallel ($\vec{v}_\parallel$) is parallel to $\hat{n}$ or is a member of the transformation $\begin{bmatrix} x \\ 2y \end{bmatrix}$ which is solved by applying the [projection formula](Projections) against the axis being
![[Linear Algebra/Matrix Transformations/Projections#^projectionRuleDef|Projections]]

$Proj_\hat{n}(\vec{v}) = (\vec{v} \cdot \hat{n})\hat{n}$

Vector perpendicular ($\vec{v}_\perp$) is perpendicular to $\vec{v}_\parallel$ which is solved simply by the initial vector minus the projection of $\vec{v}$

$\vec{v}_\perp = \vec{v} - Proj_\hat{n}(\vec{v})$

$\vec{v}_\perp = \vec{v} - (\vec{v} \cdot \hat{n})\hat{n}$

So then to get our final scaled vector $\vec{v}\;'$ we'll just need to apply the formula to get $\vec{v}$ scaled by $k$

$\begin{aligned} \vec{v}\;' = k(\vec{v}_\parallel) + \vec{v}_\perp \\[1em] \vec{v}\;' = k((\vec{v} \cdot \hat{n})\hat{n}) + \vec{v} - (\vec{v} \cdot \hat{n})\hat{n} \\[1em] \vec{v}\;' = (k\vec{v} \cdot k\hat{n})k\hat{n} + \vec{v} - (\vec{v} \cdot \hat{n})\hat{n} \\[1em] \vec{v}\;' = \vec{v} + (k - 1)(\vec{v} \cdot \hat{n})\hat{n})\end{aligned}$

So now that we have our simplified equation, we can setup out transformation matrix to represent this scale

![[Pasted image 20260813151427.png]]
![[Pasted image 20260813151433.png]]

Leaving us with a final transformation matrix 

$S = \begin{bmatrix} 1 + (k - 1)n_x^2 & (k - 1)n_yn_x \\ (k - 1)n_xn_y & 1 + (k - 1)n_y^2 \end{bmatrix}$

$\begin{bmatrix} 1 + (k - 1)n_x^2 & (k - 1)n_yn_x \\ (k - 1)n_xn_y & 1 + (k - 1)n_y^2 \end{bmatrix} \begin{bmatrix} v_x \\ v_y \end{bmatrix} = S\vec{v}$

This can also be applied in 3D where to create the transformation, we just need substitute in the basis vectors for an $R^3$ space

## Shearing 
[game math chapt 5.5](https://gamemath.com/book/matrixtransforms.html#shearing)

Shearing is a nonuniform scaling transformation that "skews" the coordinate space the object is in which means angles are not preserved but its areas and volumes are preserved as it creates a parallelogram which its area is equal to a rectangle. 

Shearing is known as a seldom-used transformation where the combination of shearing and scaling (uniform or nonuniform) creates a transformation that is exactly the same as if you were to apply a transformation of rotation and nonuniform scale

The idea behind shearing is that you add a coefficient ($s$) to a coordinate making other axis skew based on the amount of $s$ 
![[Pasted image 20260814141138.png]]

$H_x(s) = \begin{bmatrix} 1 & 0 \\ s & 1 \end{bmatrix}$

$H_y(s) = \begin{bmatrix} 1 & s \\ 0 & 1 \end{bmatrix}$

To shear in $R^3$ you must substitute in scalar multiples in the axis that is not getting sheared. for instance, if you want to shear $H_{xy}$ then you'll need to substitute coefficients into the $z$-axis basis vector that are $0$


$H_{xy}(s, t) = \begin{bmatrix} 1 & 0 & s \\ 0 & 1 & t \\ 0 & 0 & 1 \end{bmatrix}$

$H_{xz}(s, t) = \begin{bmatrix} 1 & s & 0 \\ 0 & 1 & 0 \\ 0 & t & 1 \end{bmatrix}$

$H_{yz}(s, t) = \begin{bmatrix} 1 & 0 & 0 \\ s & 1 & 0 \\ t & 0 & 1 \end{bmatrix}$

