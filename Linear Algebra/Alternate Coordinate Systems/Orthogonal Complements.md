[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/othogonal-complements/v/linear-algebra-orthogonal-complements)

Orthogonal complements are any subset of a vectors that is perpendicular or orthogonal to other vector [subsets or subspaces](Linear%20Subspaces). This is generally represented as

$\vec{v}^\perp = (\vec{x} \; \epsilon \; R^n \; | \; \vec{x} \cdot \vec{v} = 0 \; for \; every \; \vec{v} \; \epsilon \; V)$

Basically, any vector that is an orthogonal complement will produce a $\vec{0}$ when the [dot product](Vector%20Dot%20Product%20and%20Length) is applied to a subset or subspace of vectors 

This also extends to the [null space]() where the null space of a matrix is an orthogonal complement of the [row space]() of a matrix 

$N(A) = (C(A^T))^\perp$ 

**OR**

Where the [left null space](Null%20Space#Left%20Null%20Space) of a matrix is an orthogonal complement of the [column space](Column%20Space) of a matrix

$N(A^T) = C(A)^\perp$

which looks like
![[Pasted image 20260817111830.png]]

The reason why its this and not $N(A) = C(A)$ and vice versa is because, when we multiply a matrix by a vector the null space is all the row vectors of the matrix being multiplied by a vector to give the $N(A)$ which is equivalent to $C(A^T)$

$A = \begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & 2 & 3 & 4 \\ 4 & 3 & 2 & 1 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$

and if we transpose $A$

$A^T = \begin{bmatrix} 1 & 1 & 4 \\ 1 & 2 & 3 \\ 1 & 3 & 2 \\ 1 & 4 & 1 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$

You see that to get the $N(A^T)$ we must multiply the rows of the matrix with the vector, the linear combinations are made of the column vectors in $A$ before transposed which is equivalent to $C(A)$

![[Pasted image 20260817114402.png]]


## Dimension Of Orthogonal Complement
[khan acad vid](http://khanacademy.org/math/linear-algebra/alternate-bases/othogonal-complements/v/linear-algebra-dim-v-dim-orthogonal-complement-of-v-n)

the dimension of the orthogonal complement is the equivalent to the dimension of a matrix's [nullity](Null%20space) 

$dim(V^\perp) = dim(N(A^T))$ 

![[Pasted image 20260817161658.png]]

As mentioned earlier, the orthogonal complement is equivalent to the null space of a matrix because when the dot product is applied to a vector the result will be $\vec{0}$ indicating the vector is perpendicular to the vector its being multiplied against

So because of this, the result from the nullity is also the orthogonal complement when we add the $dim(V)$ with the $dim(V^\perp)$ it will produce $n$ columns that define a matrix

$dim(V) + dim(V^\perp) = n \; columns \; in \; matrix$

Considering that the dimension of the column space in rank and dimension of null space is a nullity then the equation is equivalent to the [rank](Column%20Space) plus the [nullity](Null%20space) equals $n$ columns in a set matrix

$Rank(V) + Nullity(V) = n$

![[Pasted image 20260817161648.png]]

## Representing Vectors in $R^n$ using subspace members
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/othogonal-complements/v/lin-alg-representing-vectors-in-rn-using-subspace-members)

If we have basis vectors for a subspace of $V$ and basis vectors for subspace of $V^\perp$ then we can use linear combinations of those basis vectors to find any vector in a space of $R^n$
![[Pasted image 20260818090548.png]]


$\vec{a} = c_1\vec{v_1} + c_2\vec{v_2} + ... + c_k\vec{v_k} + d_1\vec{w_1} + d_2\vec{w_2} + ... + d_{n-k}\vec{w_{n-k}}$

$\vec{a} = \vec{v} + \vec{x} \;\;\;\;\;\; \vec{x} \; \epsilon \; V \;\;\; \vec{v} \; \epsilon \; V^\perp$

This only works when each subset in a subspace is [linearly independent](Linear%20Independence) meaning that the $\vec{0}$ is the only vector in the null space and therefore, the coordinate vectors that will linearly combined with the basis vectors must be the $\vec{0}$

![[Pasted image 20260818093042.png]]

So then the only subspace that can achieve this result is the orthogonal complement of the subspace $V$ within the space of $R^n$

An example is that the basis vectors $x$ $\begin{bmatrix} 1 \\ 0 \end{bmatrix}$ and $y$ $\begin{bmatrix} 0 \\ 1 \end{bmatrix}$ in $R^2$ can create any vector $\vec{a}$ from the linear combinations of $\vec{x}$ and $\vec{y}$ or more specifically

$\vec{a} = c_1\vec{x}_1 + c_2 \vec{x}_2 + d_1\vec{y}_1 + d_2\vec{y}_2$

and because $\vec{x}$ is a orthogonal complement of $\vec{y}$  vice versa and are linearly independent so we can create any vector within the space $R^2$


## Orthogonal Complement of the orthogonal complement 
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/othogonal-complements/v/lin-alg-orthogonal-complement-of-the-orthogonal-complement), [khan acad vid - ortho complement of nullspace](https://www.khanacademy.org/math/linear-algebra/alternate-bases/othogonal-complements/v/lin-alg-orthogonal-complement-of-the-nullspace)

The orthogonal complement of the orthogonal complement is just a vector from the original subspace 

$(V^\perp)^\perp = V$ 

If we take $\vec{x} = \vec{v} + \vec{w}$ where $\vec{v} \; \epsilon \; V$ and $\vec{w} \; \epsilon \; V^\perp$ we know that if we take $\vec{x} \cdot \vec{w}$ it will equal $\vec{0}$ because anything that is the orthogonal complement has to equal the $\vec{0}$ 

$(\vec{v} + \vec{w}) \vec{w} = \vec{v} \cdot \vec{w} + \vec{w} \cdot \vec{w} = ||\vec{w}||^2$

if we expand out the equation, we'll see that from the expansion we know that $\vec{v} \cdot \vec{w}$ is $0$ so the final result becomes the [magnitude](Magnitude) of $\vec{w}$ and the only to make $\vec{x} \cdot \vec{w} = \vec{0}$ true is if $\vec{w}$ is $\vec{0}$ considering that all the vectors are linearly independent

then we know the value of $\vec{w} = \vec{0}$

Which if we substitute in the original equation $\vec{x} = \vec{v} + \vec{0}$

$\vec{x} = \vec{v}$

So therefore, if a vector is a member of the orthogonal complement of the orthogonal complement then that same vector has to be a member of the original subspace

$\vec{x} \; \epsilon \; (V^\perp)^\perp = \vec{x} \; \epsilon \; V$

The orthogonal complement of the orthogonal complement is any vector from the original subspace 

$\vec{x} \; \epsilon \; V$

![[Pasted image 20260818122925.png]]


### Orthogonal Complement of the null space
So now with this rule, we can find the orthogonal complement of the [null space and left null space](Null%20space) of a matrix

Where we know $C(A^T)^\perp = N(A)$

but if we want to find the $N(A)^\perp$ (the orthogonal complement of the orthogonal complement) then following the rule 

$N(A)^\perp = (C(A^T)^\perp)^\perp = C(A^T)$

And likewise with the left null space

$N(A^T)^\perp = (C(A)^\perp)^\perp = C(A)$

## Unique Row space to solution $A\vec{x} = \vec{b}$
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/othogonal-complements/v/lin-alg-unique-rowspace-solution-to-ax-b), [khan acad vid example](https://www.khanacademy.org/math/linear-algebra/alternate-bases/othogonal-complements/v/linear-alg-rowspace-solution-to-ax-b-example)


if you have matrix $A$ being $m \times n$

$A = \begin{bmatrix} | & | & & & & | \\ \vec{a}_1 & \vec{a}_2 & . & .& . & \vec{a}_n \\ | & | & & & & | \end{bmatrix}$

and a $\vec{b}$ is a member of the column space of $A$ meaning that $\vec{b}$ is a [linear combination](Linear%20Combination%20and%20span) of all the column vectors in $A$

$\vec{b} \; \epsilon \; C(A)$

$\vec{b} = x_1\vec{a}_1 + x_2\vec{a}_2 + ... + x_n\vec{a}_n$

$\begin{bmatrix} | & | & & & & | \\ \vec{a}_1 & \vec{a}_2 & . & .& . & \vec{a}_n \\ | & | & & & & | \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_n \end{bmatrix} = \vec{b}$

$A\vec{x} = \vec{b}$

Given a space in $R^n$ with a null space and orthogonal complement of null space with matrix $A$

![[Pasted image 20260818151625.png]]

If $\vec{b} \; \epsilon \; C(A)$ then **there exists** a unique solution involving $\vec{r}_0 \; \epsilon \; C(A^T)$ such that

$\vec{r}_0$ is a solution to $A\vec{x} = \vec{b}$  **AND** no other solution can have a smaller length

This is because as mentioned previously, any solution involving $\vec{x} \; \epsilon \; R^n$ to $A\vec{x} = \vec{b}$ can be written as a vector in the [null space](Null%20space) of $A$ ($\vec{n}_0$) plus a vector in the orthogonal complement of matrix's $A$ null space being the [row space](Row%20space) ($\vec{r}_0$)

$\vec{x} = \vec{r}_0 + \vec{n}_0$

and if we find $||\vec{x}||^2$ and expand out the equation
![[Pasted image 20260818153339.png]]

The final simplified equation will be 

$||\vec{x}||^2 = ||\vec{r}_0||^2 + ||\vec{n}_0||^2$

which then we know that because $||\vec{n}_0||^2$ will be at least positive number $\ge 0$ then we can determine that 

$||\vec{x}||^2 \ge ||\vec{r}_0||^2$

$||\vec{x}|| \ge ||\vec{r}_0||$

To visualize this notion say we have matrix $A$ and $\vec{b}$

$A = \begin{bmatrix} 3 & -2 \\ 6 & -4 \end{bmatrix} \;\;\;\;\; \vec{b} = \begin{bmatrix} 9 \\ 18 \end{bmatrix}$

To properly visualize this, we need the null space, row space and solution to $A\vec{x} = \vec{b}$

For the [null space](Null%20space) of $A$ we simply apply the reduced row echelon form of $A$

![[Pasted image 20260818182230.png]]

![[Pasted image 20260819104106.png]]

To get the solution to $A\vec{x} = \vec{b}$, we need to put matrix $A$ and $\vec{b}$ into an augmented matrix to represent the equation

$\begin{bmatrix} 3 & -2 & | & 9 \\ 6 & -4 & | & 18 \end{bmatrix}$

which then we put the augmented matrix into reduced row echelon form giving us
![[Pasted image 20260819105428.png]]

and lastly the row space which is $C(A^T)$ 
![[Pasted image 20260819105829.png]]

So now if we graph each one it looks like
![[Pasted image 20260819105905.png]]

As you can see, the row space goes directly orthogonal the null space and the solution of $A\vec{x} = \vec{b}$ which also creates the unique solution onto $A\vec{x} = \vec{b}$ being the vector $\vec{r}$ which can be represented with the equation

$\vec{r} = c\begin{bmatrix} 3 \\ -2 \end{bmatrix}$

we can find the value of $\vec{r}$ by doing algebra to find $c$ 

![[Pasted image 20260819112428.png]]

which now tells us that $\vec{r}$ is $\begin{bmatrix} {27 \over 13} \\ -{18 \over 13} \end{bmatrix}$

This calculation can be simplified to just using [projections](Projections) to figure out $\vec{r}$ 