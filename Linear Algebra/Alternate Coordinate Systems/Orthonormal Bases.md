[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/linear-algebra-introduction-to-orthonormal-bases)

Orthonormal basis is where a basis ($B$) contains a set of vectors which are:

1. [normalized to a magnitude of 1](Unit%20Vectors) 
		$||\vec{v}_i|| = \vec{v}_i \cdot \vec{v}_i = 1$
2. Are all [orthogonal](Orthogonal%20Complements) to each other
		$\vec{v}_i \cdot \vec{v}_j = 0$

$B = [\vec{v}_1, \vec{v}_2, ... ,\vec{v}_k]$

These characteristics imply the basis is [linear independent](Linear%20Independence) because if they weren't then that would mean they a vector within the basis can be created from the linear combination of a coordinate vector and another vector from the basis 

$\vec{v}_i, \vec{v}_j \; \epsilon \; B$

$\vec{v}_i \; is \; linearly \; dependent = \vec{v}_i = C \; \vec{v}_j$

Which therefore breaks the 2nd rule that defines an orthonormal basis where $\vec{v}_i$ cannot be orthogonal to $\vec{v}_j$ because it is not linear independent

$\vec{v}_i \cdot \vec{v}_j \ne 0$

A common example is the [standard basis](Coordinates%20with%20respect%20to%20a%20basis#Standard%20and%20Non-standard%20basis) for any $R$-space like $R^3$

$I_3 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$ 

Because, each vector within the matrix has a [magnitude](Magnitude) of $1$ and is orthogonal to each other

A lot of complex calculations like [projections](Projections#Projections%20onto%20subspaces%20with%20orthonormal%20bases) and [coordinates with respect to an arbitrary basis](Coordinates%20with%20respect%20to%20a%20basis#Coordinates%20with%20respect%20to%20orthonormal%20bases) are significantly simplified when an orthonormal basis is used. 

### Example

If we have two vectors in $R^3$ which form a basis:

$\vec{v}_1 = \begin{bmatrix} \frac{1}{3} \\ \frac{2}{3} \\ \frac{2}{3} \end{bmatrix} \hspace{1em} \vec{v}_2 = \begin{bmatrix} \frac{2}{3} \\ \frac{1}{3} \\ -\frac{2}{3} \end{bmatrix} \hspace{2em} B = [\vec{v}_1, \vec{v_2}]$

To determine if they are orthonormal basis, we can apply the two rules
#### 1. Each Vector is Normalized to a magnitude of 1

$||\vec{v}_1||^2 = \vec{v}_1 \cdot \vec{v}_1 = \frac{1}{9} + \frac{4}{9} + \frac{4}{9} = 1$

$||\vec{v}_1|| = 1$

$||\vec{v}_2||^2 = \vec{v}_2 \cdot \vec{v}_2 = \frac{4}{9} + \frac{1}{9} + \frac{4}{9} = 1$

$||\vec{v}_2|| = 1$

#### 2. Orthogonal To each other

$orthogonal = \vec{v}_1 \cdot \vec{v}_2 = (\frac{1}{3} \cdot \frac{2}{3}) + (\frac{2}{3} \cdot \frac{1}{3}) + (\frac{2}{3} \cdot -\frac{2}{3}) = 0$

Therefore, we can determine that $B$ is an orthonormal basis

