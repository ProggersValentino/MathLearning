[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/linear-combinations/v/linear-combinations-and-span), [game math chp 3.3.3](https://gamemath.com/book/multiplespaces.html#basis_vectors)


Linear Combinations denotes a combination of **scalar multiplication** and **vector addition** to create a new vector which is known as a linear combination which can be represented as follows:

$\vec{v} = (x \; \vec{p}) + (y \; \vec{q}) + (z \; \vec{r})$

The $x,y,z$ is a **coordinate vector** (where all of its components represent scalars) and vectors $\vec{p}, \vec{q}, \vec{r}$ are our [basis vectors](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FLinear%20Subspaces) which define each direction in a given $R^n$, in the above formula, we are working in $R^3$. The resulting new vector is then a combination of its basis vectors expanded by the coordinate vector. 

A linear combination can also be described as given the basis vectors $p,q,r$, I want to move to a new point of $n$ by $\vec{c} = (x,y,z)$ 

for instance take:
$\begin{aligned} \vec{a} = \begin{bmatrix} 1 \\ 2 \end{bmatrix} \\[1em] \vec{b} = \begin{bmatrix} 0 \\ 3 \end{bmatrix} \end{aligned}$

if we multiply $\vec{a}$ and $\vec{b}$ by $C$ scalar then we can get any set of numbers within $R^2$ if the vectors $\vec{a}$ and $\vec{b}$ are [linearly independent](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FLinear%20Independence). 
$C = [2, 1]$

$2 \cdot \vec{a} + 1 \cdot \vec{b} = [c_1, c_2]$

![[Pasted image 20260612123631.png]]
so then we can say that the **span** of $\vec{a}$ and $\vec{b}$ can equal of all $R_2$

A **span** confirms whether linear combinations from a set of vectors can represent all real-values within $R^n$ or only a particular set of vectors which is represented:

$Span(\vec{a}, \vec{b}) = R^2$ 

Which that means all linear combinations using $\vec{a}$ and $\vec{b}$ can equal to all real-values within the 2-dimensional space. 

However, not all linear combinations from certain vector pairs can equal to all of $R^n$

for instance,

$\begin{aligned} \vec{c} = \begin{bmatrix} 4 \\ 4 \end{bmatrix} \\[1em] \vec{d} = \begin{bmatrix} -4 \\ -4 \end{bmatrix} \end{aligned}$

![[Pasted image 20260612124318.png]]

if we apply any set of scalars, we'll get a linear combination that is **constrained to the directions** of $\vec{c}$ and $\vec{d}$ :

$2 \cdot \vec{c} + {1 \over 4} \cdot \vec{d} = [7,7]$

which then we are unable to get to $\vec{f}$

So then the **span** of $\vec{c}$ and $\vec{d}$ cannot produce all real-values within $R^2$ but rather $[2, 2]$

$Span(\vec{c}, \vec{d}) = [2, 2]$

