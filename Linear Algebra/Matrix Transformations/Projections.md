[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/lin-trans-examples/v/introduction-to-projections)

A projection is a calculation used to determine a vector on a line based off another vector not on the line creating a shadow like result. 
The projection vector, if minus against the vector off the line, should create a vector orthogonal to the projection.

![[Pasted image 20260717163654.png]]

The formal definition of a projection is as follows:
$Proj_L(\vec{x}) = (\Large{\vec{x} \cdot \vec{v} \over \vec{v} \cdot \vec{v}}) \; \vec{v}$

However, this definition can be further simplified by transforming the $\vec{v} \over {\vec{v} \cdot \vec{v}}$ to $\hat{u}$ due to the definition of a [unit vector](obsidian://open?vault=MathLearning&file=Algebra%2FVectors%2FUnit%20Vectors) where the dot product of two vectors are equivalent to $||\vec{v}||^2$ which if you square root it you get $||\vec{v}||$ being the magnitude. Which if you divide the original vector by its magnitude you will get a unit vector. 

Thus the Projection definition can be simplified to:
$Proj_L(\vec{x}) = (\vec{x} \cdot \hat{u}) \; \hat{u}$
^projectionRuleDef


Which is one of the geometric definitions of the [dot product](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FVector%20Dot%20Product%20%26%20Length) where its used to determine the relative direction of a vector from a set line

For instance, if we have a line and a vector:

$\begin{aligned} L = c \begin{bmatrix} 1 \\ 2 \end{bmatrix} \; | \; c \; \epsilon \; R^2 \\[1em] \vec{x} = \begin{bmatrix} 2 \\ 3 \end{bmatrix} \end{aligned}$
we can find the projection vector by applying the rule definition:
![[Pasted image 20260717165646.png]]


## Is it a Linear Transformation?
Projections are considered a linear transformation as they fulfill the two necessary rules that make a valid linear transformation being:
![[Function#^LinearTransformationRules]]

Therefore, any projection where $Proj_l(\vec{a} + \vec{b})$ distributes to $Proj_L(\vec{a}) + Proj_L(\vec{b})$
![[Pasted image 20260717181631.png]]

And any projection where $Proj_L(c\vec{a})$ can be distributed to $c \; Proj_L(\vec{a})$
![[Pasted image 20260717181731.png]]

## Matrix Vector Product Representation
With the confirmation that a projection is a linear transformation, we can represent all projection transformations in matrix vector products.

$Proj_L \; : \; R^2 \rightarrow R^2$

To figure out how, we can grab the [identity matrix](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FIdentity%20Matrix) in the given $R^n$ space and apply the projection rule definition to each vectors in the columns of the identity matrix, so it would look like this for this solution:
![[Pasted image 20260717210515.png]]

so now anytime we want to find the projection of a vector projected on a line, we apply this matrix to it. For instance if we have:

$L = \begin{bmatrix} 2 \\ 1 \end{bmatrix}$

we first find its unit vector value and then we can create our image of $I_2$ under $T$ which leaves us with:
![[Pasted image 20260720140409.png]]

