[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/subspace-basis/v/linear-subspaces)

### Subset of vectors
A subset is any group of vectors within n-dimension that belong to a larger set of vectors (like all of $R^n$) which can include shapes (triangle, circles etc), a specific rule or even a line:

$subset = Span(\vec{x}) \; \epsilon \; R^2 \;|\; x_1 \ge 10$

$subset = Span(\begin{bmatrix} 12 \\ 0 \end{bmatrix} \; \begin{bmatrix} 21 \\ 7 \end{bmatrix}\; \begin{bmatrix} 13 \\ 2 \end{bmatrix})$

#### What is a linear subspace
A subset of vectors within $R^n$ which must fulfill three condition properties to be considered a **linear subspace**. This can also be portrayed as it is a subset of vectors that fulfill the rules of a subspace definition and can still follow any additional restrictive rule its been set

$Subspace = Span(\vec{x_1}, \vec{x_2}, ... \vec{x_n}) \; \epsilon \; R^2$

$Subspace = Span(\begin{bmatrix} 1 \\ 2 \end{bmatrix} \; \begin{bmatrix} 13 \\ 2 \end{bmatrix}\; \begin{bmatrix} 3 \\ 10 \end{bmatrix})$

| Condition Property                  | Meaning                                                                                                 | Example                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Contain Zero Vector                 | Does the subset have a $0$ vector. In other words, if the subset is multiplied by $0$ will it equal $0$ | $\begin{aligned} V = (\vec{v_1}, \vec{v_2}, \vec{v_3}) \\[1em] 0 \cdot (\vec{v_1}, \vec{v_2}, \vec{v_3})) = 0 \end{aligned}$                                                                                                                                                                                                                                                                                                                                              |
| Closure under scalar multiplication | Can the subset be multiplied by **any scalar value** and still follow vector subset rules               | Not a subspace:<br>$U = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} \epsilon R^2 \| x_1 \ge 0$ <br><br>$-1 \cdot \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} -x_1 \\ -x_2 \end{bmatrix}$ <br><br>A subspace:<br>$U = Span(\begin{bmatrix} 1 \\ 1 \end{bmatrix})$<br>$-3 \cdot \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} -3 \\ -3 \end{bmatrix}$<br><br>$5 \cdot \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 5 \\ 5 \end{bmatrix}$<br> |
| Closure under addition              | Can the subset still follow the set rules when adding each vector within the subset                     | $\begin{aligned} V = (\vec{v_1}, \vec{v_2}, \vec{v_3}) \\[1em] C_1v_1 + C_2v_2 + C_3v_3\end{aligned}$                                                                                                                                                                                                                                                                                                                                                                     |
Technically speaking, if the subset fulfills the scalar multiplication rule then it will fulfill the zero vector rule as its just multiplying the vectors by $0$ to get the $\vec{0}$

So, if all the conditions are satisfied then the subset of vectors are **within a linear space**

It can be illustrated in the picture below:
![[Pasted image 20260612175301.png]]

## Basis of a Subspace - Basis Vectors
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/subspace-basis/v/linear-algebra-basis-of-a-subspace), [game math chp 3.3.3](https://gamemath.com/book/multiplespaces.html#basis_vectors)

A **basis of a subspace** is the minimum set of vectors (that are linearly independent) that spans the subspace 

for instance take:

$\begin{aligned} \vec{p} = (1,0,0) \\[1em] \vec{q} = (0,1,0) \\[1em] \vec{r} = (0,0,1) \end{aligned}$

These are considered **basis vectors** because they are linearly independent of each other. However, basis vectors do not need to be perpendicular of each other, they just need to be linearly dependent of each other allowing any other vector to be created from the basis vectors: 
![[Pasted image 20260706172353.png]]

When the basis vectors are mutually perpendicular, they are defined as an **orthogonal basis** where the coordinates are uncoupled meaning any given component from a vector $\vec{v}$ can be determined solely from $\vec{v}$. 
These can be tested using the [dot product](Vector%20Dot%20Product%20and%20Length) to determine if the vectors are mutually perpendicular as well as the [cross product](Cross%20Product) to generate the supposed vector that is perpendicular to the other two.

Additionally when orthogonal basis vectors have a unit vector value of $1$ then its redefined as a **orthonormal basis**  
## Proof of subspace basis
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/proof-any-subspace-basis-has-same-number-of-elements)

this invokes the idea that all subspace basis have the **same number of elements** which creates the **dimension**:

$Dim(V) = NO.\; of\; elements \; of \; any\; basis\; of\; V$
