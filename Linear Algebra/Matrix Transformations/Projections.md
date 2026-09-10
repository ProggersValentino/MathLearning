[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/lin-trans-examples/v/introduction-to-projections)

A projection is a calculation used to determine a vector on a specific [subspace](Linear%20Subspaces) given a vector not on the subspace creating a shadow like result, thus also reduces the overall $R$-space. 

The projection vector, if minus against the input vector, creates an orthogonal vector to the subspace its being projected onto which is otherwise known as the [orthogonal complement](Orthogonal%20Complements) of the subspace.

$\vec{x} - Proj_V(\vec{x}) = V^\perp$

Projection's behaviour can be described as a dimension-space reducing operation   

![[Pasted image 20260717163654.png]]

The formal definition of a projection is as follows:
$Proj_L(\vec{x}) = (\Large{\vec{x} \cdot \vec{v} \over \vec{v} \cdot \vec{v}}) \; \vec{v}$

However, this definition can be further simplified by transforming the $\vec{v} \over {\vec{v} \cdot \vec{v}}$ to $\hat{u}$ due to the definition of a [unit vector](Unit%20Vectors) where the dot product of two vectors are equivalent to $||\vec{v}||^2$ which if you square root it you get $||\vec{v}||$ being the magnitude. Which if you divide the original vector by its magnitude you will get a unit vector. 

Thus the Projection definition can be simplified to:
$Proj_L(\vec{x}) = (\vec{x} \cdot \hat{u}) \; \hat{u}$
^projectionRuleDef

Which is one of the geometric definitions of the [dot product](Vector%20Dot%20Product%20and%20Length) where its used to determine the relative direction of a vector from a set line

For instance, if we have a line and a vector:

$\begin{aligned} L = c \begin{bmatrix} 1 \\ 2 \end{bmatrix} \; | \; c \; \epsilon \; R^2 \\[1em] \vec{x} = \begin{bmatrix} 2 \\ 3 \end{bmatrix} \end{aligned}$
we can find the projection vector by applying the rule definition:
![[Pasted image 20260717165646.png]]


### Computer graphics definition


To solve a projection in computer graphics, the formal equation shifts to a bit 

$Proj_V(\vec{x}) = A(A^TA)^{-1}A^T\vec{x}$

which is explained [below](Projections#Projections%20on%20a%20subspace#Is%20it%20a%20linear%20transformation?)


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

To figure out how, we can grab the [identity matrix](Identity%20Matrix) in the given $R^n$ space and apply the projection rule definition to each vectors in the columns of the identity matrix, so it would look like this for this solution:
![[Pasted image 20260717210515.png]]

so now anytime we want to find the projection of a vector projected on a line, we apply this matrix to it. For instance if we have:

$L = \begin{bmatrix} 2 \\ 1 \end{bmatrix}$

we first find its unit vector value and then we can create our image of $I_2$ under $T$ which leaves us with:
![[Pasted image 20260720140409.png]]


## Projections on a subspace
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/linear-algebra-projections-onto-subspaces), [khan acad visualizations](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/linear-alg-visualizing-a-projection-onto-a-plane)

Projections can be expanded to a generalized case of [subspaces](Linear%20Subspaces) where instead of finding the projection onto just a line, we can find the projection on any subspace that includes a lines but also planes 

![[Pasted image 20260819160529.png]]

This would be most relevant to $R^3$ where the vector gets projected onto $V$ which creates $\vec{v}$ and then to create $\vec{w}$ we just need to apply

$\vec{w} = \vec{x} - \vec{v}$ 

as because $\vec{w}$ is a member of an orthogonal complement of $V$ ($V^\perp$) (defined basis vectors for the space) then any vector can be [found within the space](Orthogonal%20Complements#Representing%20Vectors%20in%20$R^n$%20using%20subspace%20members) by $\vec{x} = \vec{v} + \vec{w}$, so naturally if we want to find $\vec{w}$ we just apply the equation above which when we expand out $\vec{v}$ the equation above is really 

$\vec{w} = \vec{x} - Proj_V(\vec{x})$

### Is it a linear transformation?
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/lin-alg-a-projection-onto-a-subspace-is-a-linear-transforma)

Projections onto subspaces are considered a linear transformation, but how? 

Well if we have a subspace within $R^n$ with basis vectors which span the subspace

$V = subspace \; \epsilon \; R^n \;\;\;\;\; (\vec{b}_1, \vec{b}_2, ... \vec{b}_k) \; basis \; for \; V$ 

We know that any [linear combination](Linear%20Combination%20and%20span) of the coefficient vector ($\vec{c}$) with our basis vectors of the subspace will create a resulting vector that is a member of the subspace $V$ 

$\vec{a} = c_1\vec{b}_1 + c_2\vec{b}_2 + ... + c_k\vec{b}_k => \vec{a} \; \epsilon \; V$

which can be represented by multiplying a matrix of $n \times k$ by the coefficient vectors resulting in a vector ($\vec{a}$) that is a member of $V$ through the equation $A\vec{c} = \vec{a}$
:
$A = \begin{bmatrix} | & | & & & & | \\ \vec{b}_1 & \vec{b}_2 & . & . & . & \vec{b}_k \\ | & | & & & & | \end{bmatrix} \begin{bmatrix} c_1 \\ c_2 \\ . \\ . \\ . \\ c_k \end{bmatrix} =  c_1\vec{b}_1 + c_2\vec{b}_2 + ... + c_k\vec{b}_k$

And if we have a vector ($\vec{x}$) that is a member of $R^n$ and want to find its projection on to the subspace $V$ then that will produce a vector within the subspace of $V$

$\vec{x} \; \epsilon \; R^n$
$Proj_V(\vec{x}) = \vec{v} \; \epsilon \; V$

And because it produces a vector which is member of the subspace $V$ then $A\vec{c} = \vec{a}$ is an equivalent equation that can be substituted in for the projection

$Proj_V(\vec{x}) = A\vec{c} = \vec{v} \;\;\;\;\;\; \vec{v} \; \epsilon \; V$

To get the vector $\vec{x}$ it follows the equation $\vec{x} = \vec{v} + \vec{w}$  where vector $\vec{w}$ is the [orthogonal complement](Orthogonal%20Complements) of the subspace $V$

$\;\;\; \vec{v} \; \epsilon \; V \;\;\;\; and \;\;\;\;\; \vec{w} \; \epsilon \; V^\perp = \vec{w} \; \epsilon \; N(A^T)$

And the orthogonal complement we're solving for is the [left null space](Null%20space#Left%20Null%20Space ) of $A$ as we are using the column space ($C(A)$) which is the span of our basis vectors and therefore [its orthogonal complement is the left null space](Orthogonal%20Complements)

$C(A) =  Span(\vec{b}_1, \vec{b}_2, ... \vec{b}_k)$


As shown earlier, $\vec{v}$ just expands to the projection of the subspace $V$ 

$\vec{x} = Proj_V(\vec{x}) + \vec{w}$ 

And to solve for the orthogonal complement ($\vec{w}$) we can apply some basic algebra to reorder the equation to find $\vec{w}$ which is really solving for the left null space of $A$

$\vec{w} = \vec{x} - Proj_V(\vec{x}) \;\;\;\;\;\;\;\;\; \vec{x} - Proj_V(\vec{x}) \; \epsilon \; N(A^T)$ 

We create a similar equation to $A\vec{c} = \vec{a}$ by substituting in the our $\vec{w}$ equation to solve for our left null space, as $\vec{x} - Proj_V(\vec{x})$ is a member of the left null space. The initial goal of this is to find the solution to $\vec{c}$ where if we don't know $\vec{c}$ then we can find it by applying the equation: 

$A^T(\vec{x} - Proj_V(\vec{x})) = \vec{0}$ 

$A^T(\vec{x} - A\vec{x}) = \vec{0}$

and then if we distribute the $A^T$ our equation will look like 

$A^T\vec{x} - (A^TA)\vec{c} = \vec{0}$

We can then isolate the second half of the equation by adding $(A^TA)\vec{c}$ to both sides which will move the half of the equation to the other side

$A^T\vec{x} = (A^TA)\vec{c}$

This produces and interesting result where matrix $A$ is multiplying against matrix $A^T$ ($A^TA$). So when multiplied together, will [produce a product matrix that can be invertible](Transposing#Can%20the%20transpose%20be%20invertible?) which means that no matter what size of matrix we get, it will always have an inverse when multiplying against its transpose.

If we apply the inverse to both sides we'll find

$(A^TA)^{-1}A^T\vec{x} = (A^TA)^{-1}(A^TA)\vec{c}$

$(A^TA)^{-1}A^T\vec{x} = I_k \; \vec{c}$

$(A^TA)^{-1}A^T\vec{x} = \vec{c}$

so then we have finally figured out, that if we don't know our $\vec{c}$ value then we solve for with

$\vec{c} = (A^TA)^{-1}A^T\vec{x}$

Which now we can combine it with the whole equation of $A\vec{c} = \vec{a}$ which will finally look

$Proj_V(\vec{x}) = A(A^TA)^{-1}A^T\vec{x}$

This equation is very useful for solving projects using computer graphics 

As you see its just a [composition](Composition%20of%20Linear%20Transformations) of matrices against the vector you want to find the projection for in the set linear subspace ($\vec{x}$). Therefore, this proves that the projections of a linear subspaces are a linear transformation because anything that can turned into a matrix product IS a linear transformation

![[Matrix vector products#^linearTwithMatrices]]


### Example 
[khan acad vid example](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/linear-algebra-subspace-projection-matrix-example), [khan acad alternative example](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/lin-alg-another-example-of-a-projection-matrix)

For instance, if we have a subspace $V$ which spans across two vector:

$V = span(\begin{bmatrix} 1 \\ 0 \\ 0 \\ 1 \end{bmatrix}, \begin{bmatrix} 1 \\ 0 \\ 1 \\ 0 \end{bmatrix})$
and if we have any vector within the $R^4$ then we can find the projection of that vector onto the subspace:

$\vec{x} \; \epsilon \; R^4$

$Proj_V(\vec{x}) = A(A^TA)^{-1}A^T\vec{x}$

We can find the projection transformation matrix by applying the definition above:
![[Pasted image 20260824094524.png|642]]

Figuring out the projection through this definition using the column space of the matrix can be tedious, so an alternative is to find the orthogonal complement of the subspace

For instance if we're working in $R^3$ and we have our subspace $V$

$V = (all \; the \; \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} \; that \; satisfy \; x_1 + x_2 + x_3 = 0)$

which if we work through, we'll find that its just our null space 
![[Pasted image 20260824101617.png]]

$V = span(\begin{bmatrix} -1 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} -1 \\ 0 \\ 1 \end{bmatrix})$
which combines into matrix $A$

$A = \begin{bmatrix} -1 & -1 \\ 1 & 0 \\ 0 & 1 \end{bmatrix}$

We could work out the projection of $\vec{x}$ onto $V$ through the our definition of $Proj_V(\vec{x}) = A(A^TA)^{-1}A^T\vec{x}$  but we also know that we can find the projection of $\vec{x}$ onto the orthogonal complement ($V^\perp$) and minus that against the identity matrix to find our projection onto $V$ 

![[Pasted image 20260824102336.png]]


To determine our orthogonal complement, we must find the matrix that fulfills subspace $V$ which can only be the matrix $\begin{bmatrix} 1 & 1 & 1 \end{bmatrix}$ which is part our null space. So then we need to find the orthogonal complement which in this case is the column space:
![[Pasted image 20260824103314.png]]

so then we just apply the same equation but our orthogonal complement to find our projection matrix:
![[Pasted image 20260824103400.png]]
## Orthographic Projection 
[game math chapt 5.3](https://gamemath.com/book/matrixtransforms.html#orthographic_projection)

Another way to achieve projection is scaling a direction by $0$ which projects all the points onto a surface depending on the $R$ space. For $R^2$ all the points are projected on a perpendicular axis (a line) and within $R^3$ all the points are projected onto a plane.

This is known as a orthographic projection or parallel projection as its projected points are parallel to its original set of points

![[Pasted image 20260813174517.png]]

To achieve this effect we can just simply disregard a perpendicular axis by scaling it by $0$ which will produce a projection on the other perpendicular axis' that have not been disregarded. 

For instance, if we want to project an object in $R^3$ onto a 2D plane on the $x$ and $y$-axis then we'll need to scale the $z$-axis by $0$ collapsing all points onto a plane along the $x$ and $y$-axis 

$\begin{aligned} P_x = S(\begin{bmatrix} 0 \\ 1 \end{bmatrix}, 0) = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \\[1em] P_y = S(\begin{bmatrix} 1 \\ 0 \end{bmatrix}, 0) = \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix} \\[1em] P_{xy} = S(\begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}, 0) = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{bmatrix} \\[1em] P_{xz} = S(\begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}, 0) = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix} \\[1em] P_{yz} = S(\begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}, 0) = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \end{aligned}$

as you can see, the transformation defines the axis it will scale and then applies the $0$ scalar to zero off the axis and transform the basis vectors into a projection matrix for the set axis'

### Projecting onto an Arbitrary line or plane

We can also calculate the projection for an arbitrary line or plane which is defined by a unit vector $\hat{n}$ to represent the arbitrary line or plane we want to project onto. 

This can be found by applying the $0$ scalar to [scaling equations](Positional%20Linear%20Transformations) where 

$\begin{aligned} P_x = S(\hat{n}, 0) = \begin{bmatrix} 1 - n_x^2 & -n_yn_x \\ -n_xn_y & 1 - n_y^2 \end{bmatrix} \\[1em] = \begin{bmatrix} 1 - n_x^2 & -n_yn_x \\ -n_xn_y & 1 - n_y^2 \end{bmatrix} \end{aligned}$
so now, we are able to project any object on a line or plane based on whatever direction we feel like 

## Projection is the closest vector in subspace
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/linear-alg-projection-is-closest-vector-in-subspace)

The orthogonal vector generated from the projection of a vector ($\vec{x}$) onto a subspace $V$

$\vec{a} = \vec{x} - Proj_V(\vec{x})$

will always be the shortest vector to $\vec{x}$ compared to any other vector ($\vec{v}$) from the subspace

$||\vec{x} - Proj_V(\vec{x})|| \; \le ||\vec{x} - \vec{v}||$

![[Pasted image 20260824121456.png]]

drawing it out you can see that $\vec{a}$ has the shortest distance to $\vec{x}$ compared to $\vec{v}$ but this can also be proved mathematically.

Expanding out the vector $||\vec{x} - \vec{v}||^2$ we know that its vector combination of $||\vec{b} + \vec{a}||^2$ 

Which if we expand the equation, we'll find $\vec{b}^2 + 2\vec{a}\vec{b} + \vec{a}^2$

![[Pasted image 20260824122130.png]]

But because $\vec{a}$ is an [orthogonal complement](Orthogonal%20Complements) of the subspace $V$ and $\vec{b} \; \epsilon \; V$ then we know that $2\vec{a}\vec{b} = 0$ 

so then the final equation simplifies to 

$||\vec{x} - \vec{v}||^2 = ||\vec{b}||^2 + ||\vec{a}||^2$

which means the initial statement of the orthogonal complement generated from a projection onto $V$ will always be the shortest vector to $\vec{x}$ compared to any other vector on the subspace

![[Pasted image 20260824122706.png]]


## Projections onto subspaces with orthonormal bases
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/lin-alg-projections-onto-subspaces-with-orthonormal-bases)

[Orthonormal bases](Orthonormal%20Bases) can make projection calculation for a projection onto any subspace significantly easier by simplifying the equation from $Proj_V(\vec{x}) = A(A^TA)^{-1}A^T\vec{x}$ to:

$Proj_V(\vec{x}) = AA^T\vec{x}$

How? well first some definitions. if we have $V$ which is a subspace of $R^n$, an orthonormal basis $B$ which is the basis for $V$ and $\vec{x}$ which is a member of $R^n$ but not of the subspace

$V = subspace \; \epsilon \; R^n \hspace{1em} B = [\vec{v}_1, \vec{v}_2, ..., \vec{v}_k] \hspace{1em} V = Span(B) \hspace{2em} \vec{x} \; \epsilon \; R^n$

We know that $\vec{x}$ is the vector combination of $\vec{v}$ and $\vec{w}$ where $\vec{v}$ is a member on the subspace $V$ and $\vec{w}$ is a member of $V^\perp$ which is the equivalent to the [linear combination](Linear%20Combination%20and%20span) of any coordinate vector and the basis for the subspace $V$ which is also the projection on subspace $V$

$\vec{x} = \vec{v} + \vec{w} \hspace{1em} \vec{v} \; \epsilon \; V \; and \; \vec{w} \; \epsilon \; V^\perp$

$\vec{x} = c_1\vec{v}_1 + c_2\vec{v}_2 + ... + c_k\vec{v}_k = Proj_V(\vec{x})$

$Proj_V(\vec{x}) = A(A^TA)^{-1}A^T\vec{x}$

And if we dot $\vec{x}$ with $\vec{v}_i$ which is a member of the orthonormal basis, the equation will expand to

$\vec{v}_i \cdot \vec{x} = c_1\vec{v}_i \cdot \vec{v}_1 + c_2 \vec{v}_i \cdot \vec{v}_2 + ... + c_i\vec{v}_i \cdot \vec{v}_i + ... + c_k \vec{v}_i \cdot \vec{v}_k$

which because all the other vectors are orthogonal to each other, the result when dotting $\vec{v}_i$ against any other vector in the orthonormal basis and $\vec{w}$ will be $0$ except when $\vec{v}_i \cdot \vec{v}_i$ which will equal $1$ 

$\vec{v}_i \cdot \vec{x}= 0 + 0 + ... + c_i1 + ... + 0$

$c_i = \vec{v}_i \cdot \vec{x}$

which leaves us with the final result where we can solve for any coefficient ([coordinate vector](Coordinates%20with%20respect%20to%20a%20basis) component) by dotting $\vec{x}$ against any orthonormal basis vector. 

This provides us the entirety of the normal projection equation $(\vec{x} \cdot \hat{u}) \hat{u}$ as $\vec{v}_i$ is normalized so therefore is represented in unit vector form so now to solve for the projection onto a subspace we can substitute in the equation to find the coefficients that solve for the projection:

$Proj_V(\vec{x}) = (\vec{x} \cdot \vec{v}_1)\vec{v}_1 + (\vec{x} \cdot \vec{v}_2)\vec{v}_2 + ... + (\vec{x} \cdot \vec{v}_i)\vec{v}_i + ... + (\vec{x} \cdot \vec{v}_k)\vec{v}_k$

For finding the projection via a linear transformation, the original equation is:

$Proj_V(\vec{x}) = A(A^TA)^{-1}A^T\vec{x}$

which if we apply it under an orthonormal basis where matrix $A$ is the change of basis matrix for $B$:

$A = \begin{bmatrix} | & | & & & & | \\ \vec{v}_1 & \vec{v}_2 & . & . & . & \vec{v}_k \\ | & | & & & & | \end{bmatrix}$

An interesting result happens when we multiply $A^TA$
![[Pasted image 20260901110723.png]]

because $A$ is an orthonormal matrix (because its the change of basis matrix for the orthonormal basis $B$) each vector is orthogonal to each other so when we multiply $A^TA$ the result is the identity matrix for $k$ because every time we multiply a vector by itself then it will equal 1 but when we multiply a vector by another it will equal $0$ because they are orthogonal

$orthonormal \; basis = A^TA = I_k$
$(A^TA)^{-1} = (I_k)^{-1} = I_k$

which when we substitute it back into the full equation it simplifies

$Proj_V(\vec{x}) = AI_kA^T\vec{x}$

$Proj_V(\vec{x}) = AA^T\vec{x}$

### Example
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/lin-alg-finding-projection-onto-subspace-with-orthonormal-basis-example)

For instance, if we have an orthonormal basis which defines a subspace $V$ and a matrix $A$ which is composed of the column vectors of $V$:

$V = span(\begin{bmatrix} \frac{1}{3} \\ \frac{2}{3} \\ \frac{2}{3} \end{bmatrix}, \begin{bmatrix} \frac{2}{3} \\ \frac{1}{3} \\ -\frac{2}{3} \end{bmatrix}) \hspace{1em} [\vec{v}_1, \vec{v}_2] \; is \; orthonormal \; basis \; for \; V \hspace{2em} A = \begin{bmatrix} \frac{1}{3} & \frac{2}{3} \\ \frac{2}{3} & \frac{1}{3} \\ \frac{2}{3} & -\frac{2}{3} \end{bmatrix}$

which then because the basis vectors are orthonormal we can apply the simplified equation to find a projection the transformation matrix for any vector outside of $V$ to be projected onto the subspace $V$:

$Proj_V(\vec{x}) = AA^T\vec{x}$

![[Pasted image 20260901151014.png]]

So now any vector multiplied against the resulting vector will always produce a vector that's a member of the subspace $V$


## Perspective Projection
[game math 6.5](https://gamemath.com/book/matrixmore.html#matrices_and_perspective_projection)

Perspective projection isa type of projection where each projector intersects a mid point known as the center of projection before projecting its final result on the projection plane which inverts the original orientation of the object: 
![[Pasted image 20260908154330.png]]

This follows a similar behaviour to a pinhole camera where each light ray that passes through the hole of the camera gets projected onto the photograph invertedly but adds the extra benefit of showcasing the distance of an object:

![[Pasted image 20260908154518.png]]![[Pasted image 20260908154805.png]]


This is done through utilitising the $w$ component in a [4x4 homogeneous matrices](4x4%20Homogeneous%20Matrices) where any point that is outside the physical dimension space can be projected onto the space by dividing each vector component by $w$

But first we must understand how the projection plane works and its positioning. We can define the distance between the "pinhole" (origin) and the projection plane as $d$ where the $z$-axis equals negative $d$:

$z = -d$

which presents itself like this from the side:
![[Pasted image 20260908160001.png]]

