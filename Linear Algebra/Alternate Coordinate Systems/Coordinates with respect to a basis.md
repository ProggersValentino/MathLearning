[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/linear-algebra-coordinates-with-respect-to-a-basis)

 Coordinate vectors are vectors that represent scalar coefficients or weightings for how much each [basis vector](Linear%20Subspaces#Basis%20of%20a%20Subspace%20-%20Basis%20Vectors) should scale by. Therefore, creating a new vector from the [linear combination](Linear%20Combination%20and%20span) of the coordinates and the basis vectors.

For instance if we have a subspace $V$ within $R^n$ which its basis 

$B = (\vec{v}_1, \vec{v}_2 ..... \vec{v}_k) \;\;\;\;\;\;\; \vec{a} \; \epsilon \; V$

which then if we want to get $\vec{a}$ we do a linear combination: 

$\vec{a} = c_1\vec{v}_1 + c_2\vec{v}_2 + ... + c_k\vec{v}_k$

which within the equation, our constants are the components of our coordinate vector:

$coordinate \; vector = \begin{bmatrix} c_1 \\ c_2 \\ . \\. \\. \\ c_k \end{bmatrix}$

Coordinate vectors with respect to a basis specifies, the coordinate coefficients that will be linearly combined with basis vectors to create a new vector:
$[\vec{a}]_B = \begin{bmatrix} c_1 \\ c_2 \\ . \\ . \\ . \\ c_k \end{bmatrix}$

#### Standard and Non-standard basis
Within the basis, you have standard and non-standard basis.

The standard basis is the default basis consisting of vectors with value of $1$ which spans for each component or rows that the vector spans to. Which then the coordinate vector is the resulting vector because each weight is multiplied by only $1$  

for instance the standard basis for $R^2$ is $[\begin{bmatrix} 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 1 \end{bmatrix}]$ 
As you can see, each vector only has a $1$ within it and it spans across the $R^n$ space so if we have the coordinate vector:

$[\vec{a}]_B = \begin{bmatrix} 4 \\ 9 \end{bmatrix}$ then the resulting $\vec{a}$ will be $\begin{bmatrix} 4 \\ 9 \end{bmatrix}$ 

Non-standard basis vectors consist of [linearly independent](Linear%20Independence) vectors are are not part of the standard basis but can still linearly combine any coordinate vectors to produce any vector spanning the $R$ space 

For instance if we have two vectors which form the basis for $R^2$

$\vec{v}_1 = \begin{bmatrix} 2 \\ 1 \end{bmatrix} \;\;\;\;\;\;\;\;\; \vec{v}_2 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$

$B = (\vec{v}_1, \vec{v}_2) \; basis \; for \; R^2$

```desmos-graph
left=-2;right=10;top=10;bottom=-2
---
v_1 = (2t, 1t) | 0 <= t <= 1
v_2 = (1t, 2t) | 0 <= t <= 1 | GREEN
```

We know that because, they are a basis we can create any vector. So if we apply the equation

$\vec{a} = 3\vec{v_1} + 2\vec{v}_2 = \begin{bmatrix} 8 \\ 7 \end{bmatrix}$

Then the coordinates with respect to the basis will be:

$\Large{[\vec{a}]_B = \begin{bmatrix} 3 \\ 2 \end{bmatrix}}$

Which means that the linear combination of the coordinate weights $\begin{bmatrix} 3 \\ 2 \end{bmatrix}$ and the basis vectors of $R^2$ $\vec{v}_1 \; and \; \vec{v}_2$ create the new vector $\vec{a}$
```desmos-graph
left=-2;right=9;top=9;bottom=-2
---
q=3
s=2
(2qt, 1qt) | -3 <= t <= 1 | red | label: v1 scaled by 3
(2q+1st,1q+2st)\left\{0<=t<=1\right\} | 

3(2,1)t + 2(1,2)t | 0 <= t <= 1

3(2,1) + 2(1,2) | label: vector a


```

which as you can see $\vec{v}_1$ is scaled 3 times and $\vec{v}_2$ is scaled $2$ times to get the final vector $\vec{a} = \begin{bmatrix} 8\\ 7 \end{bmatrix}$

```desmos-graph
left=-2;right=9;top=9;bottom=-2
---
q=3
s=2
(2qt, 1qt) | -3 <= t <= 1 | red | label: v1 scaled by 3
(2q+1st,1q+2st)\left\{0<=t<=1\right\} | 

v_1 = (2,1) | label: 1 | #ffc9c9

p_2 = 2v_1 | label: 2 | #ffc9c9

p_3 = 3v_1 | label: 3 | #ffc9c9

v_2 = (2q+1,1q+2) | label: 1 | #b2f2bb
p_4 = (2q+1s,1q+2s) | label: 2 | #b2f2bb
```


## Change of basis matrix
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/linear-algebra-change-of-basis-matrix)

The change of basis matrix is a combination of all the basis vectors in matrix form. For instance, take matrix $C$ it represents all basis of $B$ within a singular matrix

$B = [\vec{v}_1, \vec{v}_2, ... , \vec{v}_k] \;\;\;\;\;\;\;\; C = \begin{bmatrix} | & | & & & & | \\ \vec{v}_1 & \vec{v}_2 & . & . & . & \vec{v}_n \\  | & | & & & & |\end{bmatrix}$

$[\vec{a}]_B = \begin{bmatrix} c_1 \\ c_2 \\ . \\. \\. \\ c_k \end{bmatrix}$
which makes the process of finding $\vec{a}$ a lot easier due to [matrix multiplication](Matrix%20Multiplication) which is possible because its just another way to do a linear combination where each constant is applied to the correct vector its scaling all throughout linear combination 

$C[\vec{a}]_B = \begin{bmatrix} | & | & & & & | \\ \vec{v}_1 & \vec{v}_2 & . & . & . & \vec{v}_n \\  | & | & & & & |\end{bmatrix} \begin{bmatrix} c_1 \\ c_2 \\ . \\. \\. \\ c_k \end{bmatrix} = \vec{a}$
For instance take the vectors $\vec{v}_1$ and $\vec{v}_2$ which are make up basis $B$

$\vec{v}_1 = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} \hspace{1em} \vec{v}_2 = \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix} \hspace{2em} B = [\vec{v}_1, \vec{v}_2]$

which is visually represented:

```desmos-graph-3d
width=700;height=700
---
2x + 2y - 2z = d | #9775fa
d=0

(1t, 2t, 3t) | 0 <= t <= 1 | #ffa94d
(1t, 0t, 1t) | 0 <= t <= 1 | #4dabf7

```

And are represented in matrix $C$

$C = \begin{bmatrix} 1 & 1\\ 2 & 0 \\ 3 & 1 \end{bmatrix}$

And the vector $\vec{a}$ is the linear combination of $B$ at the respective coefficients $7$ and $-4$

$[\vec{a}]_B = \begin{bmatrix} 7 \\ -4 \end{bmatrix}$

which then we can apply matrix multiplication to $C[\vec{a}]_B$ to find $\vec{a}$

$\begin{aligned} C[\vec{a}]_B = \begin{bmatrix} 1 & 1\\ 2 & 0 \\ 3 & 1 \end{bmatrix} \begin{bmatrix} 7 \\ -4 \end{bmatrix} = \begin{bmatrix} 3 \\ 14 \\ 19 \end{bmatrix} \\[1em] (1 \cdot 7 + 1 \cdot -4), (2 \cdot 7 + 0 \cdot -4), (3 \cdot 7 + 1 \cdot -4) = (3, 14, 19) \end{aligned}$

as you can see, each coordinate coefficient multiplies a column from the change of basis matrix which when graphed, vector $\vec{a}$ is created within the subspace of the basis $B$ and is the linear combination of the change of basis matrix ($C$) and its coordinate vector ($[\vec{a}]_B$)

```desmos-graph-3d
width=700;height=700;
---
2x + 2y - 2z = d | #9775fa
d=0

q = 7
s = -4
(1qt, 2qt, 3qt) | 0 <= t <= 1 | #ffa94d
(1q + 1st, 2q + 0st, 3q + 1st) | 0 <= t <= 1 | #4dabf7

(3t,14t,17t) | 0 <= t <=1 | #38d9a9

(3,14,17) | label: vector a | #38d9a9
```


### Solving for the coordinate vector with respect to a basis
We can also figure out the coordinate vector with respect to the basis if we have our Basis and result vector by applying the  [reduced row echelon](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) on an augmented matrix. For instance if we have our result vector $\vec{d}$ and our basis $B$:

$\vec{d} = \begin{bmatrix} 8 \\ -6 \\ 2 \end{bmatrix} \hspace{1em} \vec{v}_1 = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} \hspace{1em} \vec{v}_2 = \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix} \hspace{1em} B = [\vec{v}_1, \vec{v}_2] \hspace{2em} C = \begin{bmatrix} 1 & 1\\ 2 & 0 \\ 3 & 1 \end{bmatrix}$


but we don't know what our coordinate vector within respect to our basis $B$ which leaves us with the current equation:

$\begin{bmatrix} 1 & 1\\ 2 & 0 \\ 3 & 1 \end{bmatrix} [\vec{d}]_B = \begin{bmatrix} 8 \\ -6 \\ 2 \end{bmatrix}$

From here we can put $C$ and $\vec{d}$ into an augment matrix and apply the reduced row echelon to figure out our coordinate vector within respect to our basis $B$ ($[\vec{d}]_B$)
![[Pasted image 20260826214855.png]]

leaving us with:

$[\vec{d}]_B = \begin{bmatrix} -3 \\ 11 \end{bmatrix}$

which when substituted into the equation, it will produce $\vec{d}$:

$\begin{bmatrix} 1 & 1\\ 2 & 0 \\ 3 & 1 \end{bmatrix} \begin{bmatrix} -3 \\ 11 \end{bmatrix} = \begin{bmatrix} 8 \\ -6 \\ 2 \end{bmatrix}$

## Invertible Change of basis matrix
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/lin-alg-invertible-change-of-basis-matrix)

Like all other matrices, the change of basis matrix is invertible only if its [injective and surjective](Surjective%20and%20Injective%20Functions) meaning that the matrix must be a squared matrix and its column vectors are [linearly independent](Linear%20Independence)

Or another to frame it is if the span of $B$ is $R^n$ then $C$ is invertible. This is useful for if we want an easier way to find the Coordinates to a vector with respect to a basis ($[\vec{a}]_B$)

so if we have

$B = [\vec{v}_1, \vec{v}_2, ... \vec{v}_k] \hspace{2em} C = \begin{bmatrix} | & | & & & & | \\ \vec{v}_1 & \vec{v}_2 & . & . & . & \vec{v}_n \\  | & | & & & & |\end{bmatrix}$

$C[\vec{a}]_B = \vec{a}$

And if we want to find $[\vec{a}]_B$ then we would have to go through the process of finding the reduced row echelon of some augmented matrix but if we apply simple algebra and $C^{-1}$ to the equation then it works out

$\begin{aligned} C^{-1}C[\vec{a}]_B = C^{-1}\vec{a} \\[1em] I_n[\vec{a}]_B = C^{-1}\vec{a} \\[1em] [\vec{a}]_B = C^{-1}\vec{a} \end{aligned}$


so as you can see, the $C^{-1}C$ cancel out to $I_n$ because any inverse multiplied against its original matrix equals the [identity matrix](Identity%20Matrix). which then simplifies to the equation $[\vec{a}]_B = C^{-1}\vec{a}$ meaning that if we want to find the $[\vec{a}]_B$ then we just have to multiply $\vec{a}$ with the inverse of $C$ ($C^{-1}$)


### Example

Given the vectors which form the basis of $R^2$ and form matrix $C$

$\vec{v}_1 = \begin{bmatrix} 1 \\ 3 \end{bmatrix} \hspace{1em} \vec{v}_2 = \begin{bmatrix} 2 \\ 1 \end{bmatrix} \hspace{1em} B = [\vec{v}_1, \vec{v}_2] \hspace{1em} B \; \epsilon \; R^2 \hspace{2em} C = \begin{bmatrix} 1 & 2 \\ 3 & 1 \end{bmatrix}$ 

which visually looks like
```desmos-graph
left=-2;right=9;top=9;bottom=-2
---
(1t,3t) | 0 <= t <= 1 | green
(2t,1t) | 0 <= t <= 1 | red

```

and if we have $\vec{a} = \begin{bmatrix} 7 \\ 2 \end{bmatrix}$ but we don't know its coordinate with respect to the basis $B$ ($[\vec{a}]_B$) 

Because $C$ is a square matrix and its column vectors $\vec{v}_1$ and $\vec{v}_2$ are linearly independent then we can solve for $[\vec{a}]_B$ by applying the new formula

$[\vec{a}]_B = C^{-1}\vec{a}$

![[Pasted image 20260827164933.png]]

which will give the coordinate of $\vec{a}$ with respect to $B$

$[\vec{a}]_B = -\frac{1}{5} \begin{bmatrix} 3 \\ -19 \end{bmatrix}$

which if we substitute into the equation we'll get $\vec{a}$

$\begin{bmatrix} 1 & 2 \\ 3 & 1 \end{bmatrix}\begin{bmatrix} -\frac{3}{5} \\ \frac{19}{5} \end{bmatrix} = \begin{bmatrix} 7 \\ 2 \end{bmatrix}$

which visually looks like:

```desmos-graph
left=-2;right=9;top=9;bottom=-2
---
q = \frac{19}{5}
s = -\frac{3}{5}


(2qt,1qt) | 0 <= t <= 1 | red
(2q + 1st,1q + 3st) | 0 <= t <= 1 | green
((2q + 1s)t,(1q + 3s)t) | 0 <= t <= 1 | #4dabf7
(7,2) | #a5d8ff | label: a = (7,2)
```


## Transformation Matrix with respect to basis
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/lin-alg-transformation-matrix-with-respect-to-a-basis)

The mapping of a vector $\vec{x}$ to its codomain will remain the same no matter the coordinate system its whether its standard or non-standard. This can be represented with the equation:

$D[\vec{x}]_B = C^{-1}AC[\vec{x}]_B$ 

Given the transformation: $T:R^n \rightarrow R^n$ 

we know that if we apply $T$ to any $\vec{x}$ then we produce a vector within the codomain of the transformation, which can also be [represented as the transformation matrix](Matrix%20vector%20products) $A$ multiplied by $\vec{x}$

$T(\vec{x}) = A\vec{x}$

Where $A$ is the transformation matrix for $T$ with respect to **the standard basis** 
![[Pasted image 20260828114234.png]]

And if we have another coordinate system of a **non-standard basis** $B$ for $R^n$ which now $\vec{x}$ is the same but its now within respect to the basis $B$

$B = [\vec{v}_1, \vec{v}_2, ... \vec{v}_n] \hspace{2em} C = \begin{bmatrix} | & | & & & & | \\ \vec{v}_1 & \vec{v}_2 & . & . & . & \vec{v}_n \\  | & | & & & & |\end{bmatrix}$

To then get $[T(\vec{x})]_B$ it would be with the transformation matrix $D$ multiplied with $[\vec{x}]_B$ where $D$ is the transformation matrix for $T$ with respect to the non-standard basis $B$ 

$[T(\vec{x})]_B = D[\vec{x}]_B = [A\vec{x}]_B$

This is also equivalent to the matrix $A$ multiplied by $\vec{x}$ within respect to the basis $B$ but we're unsure what $D$ which now can be solved

$C[\vec{x}]_B$ produces the result $\vec{x}$ and granted that $C$ is a square matrix we can find the coordinate vector within respect to basis $B$ by multiplying $C$ by its inverse matrix $C^{-1}$ which gives us:

$[\vec{x}]_B = C^{-1}\vec{x}$

So then we can apply it to find our $[A\vec{x}]_B$ which when expanded equals:

$[A\vec{x}]_B = C^{-1}A\vec{x}$ 

$\vec{x}$ can further be expanded to formula $C[\vec{x}]_B$ as that is the formula to find $\vec{x}$ given a coordinate system, which then leaves us with the final equation:

$D[\vec{x}]_B = C^{-1}AC[\vec{x}]_B$

Therefore, matrix $D$ can be found by the [composition](Composition%20of%20Linear%20Transformations) of $C^{-1}AC$ 

Where $D$ is the transformation matrix for $T$ within respect for the non-standard basis $B$

& $C$ is the change of basis matrix for $B$

& $A$ is the transformation matrix for $T$ within respect for the standard basis 

This formula allows us to find the mapping of $\vec{x}$ to the same codomain using any non-standard basis to produce the same result as the standard basis would 

### Example
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/lin-alg-alternate-basis-tranformation-matrix-example), [khan acad vid application](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/lin-alg-alternate-basis-tranformation-matrix-example-part-2)

For instance, if we have the transformation going from $R^2$ to $R^2$ with transformation matrix $A$ within the standard basis

$T: R^2 \rightarrow R^2 \hspace{1em} T(\vec{x}) = A\vec{x} = \begin{bmatrix} 3 & -2 \\ 2 & -2 \end{bmatrix}\vec{x}$

And we have an alternate $R^2$ non-standard basis $B$

$B = [\begin{bmatrix} 1 \\ 2 \end{bmatrix}, \begin{bmatrix} 2 \\ 1 \end{bmatrix}]$ 

Then if we want to map $\vec{x}$ to the codomain within the non-standard basis $B$ ($[T(\vec{x}]_B$) then we'll need to follow the equation:

$D[\vec{x}]_B = [T(\vec{x})]_B$ 

But because we don't know what $D$ is we'll figure it out using the new equation discovered:

$D = C^{-1}AC$ 
![[Pasted image 20260828132957.png]]
Which when applied outputs the final matrix:

$D = \begin{bmatrix} -1 & 0 \\ 0 & 2 \end{bmatrix}$

So then with that new found matrix, we are able to map $\vec{x}$ to it codomain with respect to the non-standard basis of $B$

![[Pasted image 20260828150256.png]]

this process can be very important as with Linear Algebra, its mostly the art in choosing the **right** basis as that may help reduce the computation time to calculate the transformation for a vector multiple times

## Changing Coordinate Systems to help find a transformation matrix
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/lin-alg-changing-coordinate-systems-to-help-find-a-transformation-matrix)

If we want to apply a transformation across an arbitrary axis (non-standard basis) then solving for the transformation matrix is a bit difficult in standard basis form, therefore, it might be easier to find to the transformation matrix ($D$) across the arbitrary axis to then convert to the standard basis to find the final transformation matrix in our standard basis 

For instance, if we have a line and its [orthogonal complement](Orthogonal%20Complements) which is defined:

$L = [t\begin{bmatrix} 1 \\ 2 \end{bmatrix}] \; where \; t \; \epsilon \; R$

$L^\perp = \vec{v}_1 = \begin{bmatrix} 2 \\ -1 \end{bmatrix}$

Which $L$ and $L^\perp$ creates its own basis:

$B = [\begin{bmatrix} 2 \\ -1 \end{bmatrix}, \begin{bmatrix} 1 \\ 2 \end{bmatrix}]$

And we have $\vec{x}$ which we want to apply a reflection transformation over $L$ from $R^2$ to $R^2$ 

![[Pasted image 20260830173513.png]]

While we can find the transformation in standard basis form ($T(\vec{x})$), it might be easier to find the coordinate system with respect to $B$ ($[T(\vec{x})]_B$) which we can find using the equation to find the transformation matrix ($D$) with respect to an arbitrary basis:

$D = C^{-1}AC$ 

Which first we must find $C^{-1}$ which then we can find matrix $D$
![[Pasted image 20260830174804.png]]

with that result we can substitute $D, C^{-1}, C$ in the equation to find $A$

$A = C^{-1}DC$

giving the our final transformation matrix in the standard basis:
![[Pasted image 20260830175007.png]]

## Coordinates with respect to orthonormal bases
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/linear-algebra-coordinates-with-respect-to-orthonormal-bases) 

[Orthonormal bases](Orthonormal%20Bases) are considered the best possible basis a coordinate can be with respect to. 

This is because the process for finding a coordinate vector coefficients with respect to an arbitrary basis is **significantly simplified** to just a simple [dot product](Vector%20Dot%20Product%20and%20Length) equation:

$\vec{v}_i \cdot \vec{x} = [\vec{x}]_B$

As if we have a the basis $B$ which is an orthonormal basis for subspace $V$ and $\vec{x}$ is a member of $V$

$B = [\vec{v}_1, \vec{v}_2, ..., \vec{v}_k] \hspace{1em} B \; is \; a \; basis \; for \; subspace \; V \hspace{2em} \vec{x} \; \epsilon \; V$

So then we know that to get $\vec{x}$ it is the linear combination of a coordinate vector's coefficients and the basis $B$:

$\vec{x} = c_1\vec{v}_1 + c_2\vec{v}_2 +...+ c_i\vec{v}_i +...+ c_k\vec{v}_k$

Say we want to find the result of $\vec{v}_i \cdot \vec{x}$ it would expand to:

$\vec{v}_i \cdot \vec{x} = c_1\vec{v}_i \cdot \vec{v}_1 + c_2\vec{v}_i \cdot\vec{v}_2 +...+ c_i\vec{v}_i \cdot \vec{v}_i +...+ c_k\vec{v}_i \cdot \vec{v}_k$

which because the basis $B$ which defines the subspace $V$ is an orthonormal basis, the result will simplify:

$\vec{v}_i \cdot \vec{x} = 0 + 0 +...+ c_i1 +...+ 0$

$\vec{v}_i \cdot \vec{x} = c_i$

because when the other vectors are dotted against $\vec{v}_i$ it will produce $0$ because they are all orthogonal to each other and the $\vec{v}_i \cdot \vec{v}_i$ will simplify to $1$ [pertaining to the characteristics that make up an orthonormal basis](Orthonormal%20Bases). leaving us with the final equation:

$\vec{v}_i \cdot \vec{x} = \begin{bmatrix} c_1 \\ c_2 \\ ... \\  c_i \\ ... \\ c_k \end{bmatrix} = \begin{bmatrix} \vec{v}_1 \cdot \vec{x} \\ \vec{v}_2 \cdot \vec{x} \\ ... \\ \vec{v}_i \cdot \vec{x} \\ ... \\ \vec{v}_k \cdot \vec{x} \end{bmatrix}$


This equation is instead of $[\vec{x}]_B = C^{-1}\vec{x}$ which requires a lot steps to solve and can only be solved if $C$ is a square matrix as shown above. thus coordinates that are with respect to orthonormal bases is the best basis

### Example

For instance, if we have two vectors that make a orthonormal basis $B$ for all of $R^2$ and an initial vector $\vec{x}$ within $R^2$:

$\vec{v}_1 = \begin{bmatrix} \frac{3}{5} \\ \frac{4}{5} \end{bmatrix} \hspace{1em} \vec{v}_1 = \begin{bmatrix} -\frac{4}{5} \\ \frac{3}{5} \end{bmatrix} \hspace{2em} B = [\vec{v}_1, \vec{v}_2]$

$\vec{x} = \begin{bmatrix} 9 \\ -2 \end{bmatrix}$

and if we want to find the coordinate that makes $\vec{x}$ with respect to basis $B$ ($[\vec{x}]_B$) instead of applying the equation which will take longer to solve: 

$[\vec{x}]_B = C^{-1}\vec{x}$ 

we can apply the simpler equation because we're working in a orthonormal basis:

$[\vec{x}]_B = \vec{v}_i \cdot \vec{x}$

which expands to:

$[\vec{x}]_B = \begin{bmatrix} (\frac{3}{5} \cdot 9) + (\frac{4}{5} \cdot -2) \\ (-\frac{4}{5} \cdot 9) + (\frac{3}{5} \cdot -2) \end{bmatrix} = \begin{bmatrix} \frac{27}{5} - \frac{8}{5} \\ -\frac{36}{5} - \frac{6}{5} \end{bmatrix}$

$[\vec{x}]_B = \begin{bmatrix} \frac{19}{5} \\ -\frac{42}{5} \end{bmatrix}$

which as you can see is a lot easier to solve 

## Orthogonal Change of basis matrix to find transformation matrix
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/lin-alg-example-using-orthogonal-change-of-basis-matrix-to-find-transformation-matrix)

Another property that an orthogonal basis provides is when we the change of basis matrix is a square orthonormal matrix then if we want to find matrix $A$ then we can use $C^T$ instead of $C^{-1}$:

$A = CDC^{-1} = CDC^T$

This is possible due to when we try to find the identity matrix, we usually follow this formula:

$I_n = C^{-1}C$

But with orthonormal bases, the same identity matrix can be solved by applying:

$I_n = C^TC$

so therefore, we can safely substitute $C^{-1}$ for $C^T$ if the change of basis matrix is a $n \times n$ and an orthonormal matrix providing the exact same result for matrix $A$

### Example

For instance, if we have $3$ vectors that span all of $R^3$ which form an orthonormal basis:

$\vec{v}_1 = \begin{bmatrix} \frac{2}{3} \\ -\frac{2}{3} \\ \frac{1}{3} \end{bmatrix} \hspace{1em} \vec{v}_2 = \begin{bmatrix} \frac{2}{3} \\ \frac{1}{3} \\ -\frac{2}{3} \end{bmatrix} \hspace{1em} \vec{v}_3 = \begin{bmatrix} \frac{1}{3} \\ \frac{2}{3} \\ \frac{2}{3} \end{bmatrix} \hspace{2em} [\vec{v}_1, \vec{v}_2, \vec{v}_3] \; form \; an \; orthonormal \; basis \; B$

$B = [\vec{v}_1, \vec{v}_2, \vec{v}_3]$

which $\vec{v}_1, \vec{v}_2$ form a subspace $V$ 

$V = span(\vec{v}_1, \vec{v}_2)$

And we want to find the [reflection transformation](Positional%20Linear%20Transformations#Diagonal%20Matrices##Reflection) over the subspace $V$

![[Pasted image 20260901205351.png]]

This could be solved within the standard basis, but becomes extremely difficult to do so, therefore, we should change the basis to the orthonormal basis $B$ to find the vector $\vec{x}$ with respect to the orthonormal basis $B$ ($[\vec{x}]_B$) and translate it over back to the standard basis, which can be done with our new simplified equation because change of basis matrix is a square matrix:

$A = CDC^T$ 

![[Pasted image 20260901205842.png]]


First we got to solve for $D$ which can be found
![[Pasted image 20260901210436.png]]
![[Pasted image 20260901210447.png]]
![[Pasted image 20260901210745.png]]

and we can also find the change of basis matrix by combining the basis $B$ into a squared matrix:
![[Pasted image 20260901210849.png]]

from here we are able to find $A$ by apply the equation $CDC^T$
![[Pasted image 20260901211101.png]]

leaving us with the final transformation matrix to reflect any vector across the subspace $V$:

$A = \frac{1}{9} \begin{bmatrix} 7 & -4 & -4 \\ -4 & 1 & -8 \\ -4 & -8 & 1 \end{bmatrix}$

$T(\vec{x}) = A\vec{x} = \frac{1}{9} \begin{bmatrix} 7 & -4 & -4 \\ -4 & 1 & -8 \\ -4 & -8 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} \hspace{1em} where \; \vec{x} \; \epsilon \; R^3$



