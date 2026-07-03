[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/defining-the-angle-between-vectors)

To prove that a triangle can be formed from vectors, it needs to be tested against cauchy-schwarz inequality ensuring that it can prove against any reasons that may prevent the vectors from forming a triangle:
$\vec{a},\vec{b} \; \epsilon |R^n = nonZero$

![[Pasted image 20260618160854.png]]

which now that we know we can construct a triangle from the vector, we can now find its angle between two vectors using the Law of Cosines which defines the way to find an angle of all triangles that are not **right-angled**:

$C^2 = A^2 + B^2 - 2ABC \; Cos\theta$

which then from there we can work our way through to our final equation to find the angle of $\vec{a} \cdot \vec{b}$:
![[Pasted image 20260618161455.png]]

$(\vec{a} \cdot \vec{b}) = ||\vec{a}||||\vec{b}|| cos\theta$
^angleBetweenVectors
#### Perpendicular Angles definitions

A perpendicular is when vectors $\vec{a}$ and $\vec{b}$ $\theta$ is exactly $90^{\circ}$ from each other thus being perpendicular vectors 

If we then substitute the $\theta$ in the discovered equation to $90^{\circ}$:
![[Pasted image 20260618163327.png]]

which means if  $\vec{a}$ and $\vec{b}$ are **non-zero vectors** and their dot product is **equal to $0$** then $\vec{a} \; \vec{b}$ are **perpendicular vectors**

but if we only have the condition where $\vec{a} \cdot \vec{b} = 0$ then it is considered to be **orthogonal** meaning the **zero vector** is orthogonal to everything