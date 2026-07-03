[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/proof-of-the-cauchy-schwarz-inequality)

say we have:

$\vec{x}, \vec{y} \epsilon R^n = non-zero$ 

Schwarz defines that we can the absolute value from the product of two vectors that is less than or equal to the lengths of each vector:
![[Pasted image 20260618110642.png]]


$\begin{aligned} |\vec{x} \cdot \vec{y}| \le ||\vec{x}||||\vec{y}|| \\[1em] |\vec{x} \cdot \vec{y}| = ||\vec{x}||||\vec{y}|| \longleftrightarrow \vec{x} = c \cdot \vec{y} \end{aligned}$

better yet the only time where the dot product of $\vec{x}$ and $\vec{y}$ **can be equal** to their lengths is when either vector is multiplied by a scalar with the other vector which defines our **inequality** as shown below:
![[Pasted image 20260618110741.png]]


#### Vector Triangle Inequality
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/linear-algebra-vector-triangle-inequality)

The vector triangle inequality follows off from the Cachy-Schwarz inequality equations where if we have a vector length of $||\vec{x} + \vec{y}||$ then it will be **less than or equal to** the $||\vec{x}||+||\vec{y}||$ :
$||\vec{x} + \vec{y}|| \le ||\vec{x}|| + ||\vec{y}||$

which is shown like this:
![[Pasted image 20260618113924.png]]

which the reason why is if we have two vectors and add them together then they will form a triangle and the final side of the triangle (the new vector from $\vec{x} + \vec{y}$) will always be less or equal to that equation:
![[Pasted image 20260618114701.png]]

And of course in the extreme case, if $\vec{x} \vec{y}$ are **co-linear** then the resulting vector length will be equal to $||\vec{x}||$ and $||\vec{y}||$


