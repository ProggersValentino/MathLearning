[khan acad vid](http://khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/linear-algebra-least-squares-approximation)

Least squares approximation is finding the best solution to a vector ($\vec{b}$) that is not within a [subspace](Linear%20Subspaces) where the best solution is a coefficient vector ($\vec{x}^*$) that is a member of the subspace representing the outside vector as close as possible.

For instance take $A\vec{x} = \vec{b}$ but there is **no possible solution** to get to $\vec{b}$ meaning, that there is no [linear combination](Linear%20Combination%20and%20span) of vectors and coefficients that can equal $\vec{b}$

$\begin{bmatrix} | & | & & & & | \\ \vec{a}_1 & \vec{a}_2 & . & . & . & \vec{a}_k \\ | & | & & & & | \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ . \\ . \\ . \\ x_k \end{bmatrix} \ne \vec{b}$

which can be visualized 
![[Pasted image 20260824142221.png]]

So we need to find a coefficient vector of $\vec{x}^*$ which minimizes the distance between $\vec{b}$ where $A\vec{x}^*$ is the closest representation of $\vec{b}$ on the subspace $C(A)$ giving the us the best possible solution to represent $\vec{b}$.

The formal definition of the least squares approximation can be defined as:

$A^TA\vec{x}^* = A^T\vec{b}$
^leastsquaresFormalDef

This definition will always [generate the closest vector](Projections#Projection%20is%20the%20closest%20vector%20in%20subspace) ($\vec{v}$) within subspace to a vector ($\vec{b}$) that cannot be attained 

To get to our formal definition we need to step back. We know that $\vec{x}^*$ is the least squares vector to $\vec{b}$ and that $A\vec{x}^*$ will generate the vector on the subspace that is closest to $\vec{b}$

$A\vec{x}^*$ is a [projection](Projections) onto $C(A)$ and if we minus $\vec{b}$ from it we'll end up with the [orthogonal complement](Orthogonal%20Complements) of $C(A)$ (as shown with the orange vector above)

$A\vec{x}^* = Proj_{C(A)}(\vec{b})$

$A\vec{x}^* - \vec{b} = Proj_{C(A)}(\vec{b}) - \vec{b}$ 

$A\vec{x}^* - \vec{b} = C(A)^\perp = N(A^T) \;\;\;\;\;\;\;\; \therefore A\vec{x}^*-b \; \epsilon \; N(A^T)$

So now if we multiply $A\vec{x}^*$ by $A^T$ the result will be the [null space](Null%20space) of $A^T$

$A^T(A\vec{x}^*) = \vec{0}$

and if we distribute the $A^T$ and apply basic algebra, we'll find that it ends up equaling our formal definition:

$A^TA\vec{x}^* = A^T\vec{b}$

## Example
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/linear-algebra-least-squares-examples)

For instance, if we have $3$ equation systems

$\begin{aligned} 2x - y = 2 \\[1em] x + 2y = 1 \\[1em] x + y = 4 \end{aligned}$

If we solve for $y$ then our equations would follow this result

$\begin{aligned}  -y = -2x + 2 \rightarrow y = 2x - 2 \\[1em] 2y = -x + 1 \rightarrow y = -{1\over2}x + {1\over2}  \\[1em] y = -x + 4 \end{aligned}$

which when plotted on a graph, all the points intersect each other but there is no line that has a 3 way intersection with lines meaning that there is no solution to $y$ that is solvable within the set of systems:

```desmos-graph
y=2x-2
y=-\frac{1}{2}x + \frac{1}{2}
y=-x+4
```


putting it in matrix form 
![[Pasted image 20260824175656.png|411]]

```desmos-graph-3d
width=700;height=700;locked=true

---
v=(2t,1t,4t)|0<= t <= 1|label:vector b
-1x+-3y+5z=d|#9775fa
d=0
```

we can see that $A\vec{x} = b$ has no solution meaning that $\vec{b}$ is not within the subspace of $C(A)$ so now the best solution must be found using the least squares approximation:

$A^TA\vec{x}^* = A^T\vec{b}$ 

First, we'll need to solve for $A^TA$ and then $A^T\vec{b}$
![[Pasted image 20260824184302.png]]
![[Pasted image 20260824184313.png]]

So then if we substitute in the results of $A^TA$ and $A^T\vec{b}$ into the least squares equation

$\begin{bmatrix} 6 & 1 \\ 1 & 6 \end{bmatrix} \vec{x}^* = \begin{bmatrix} 9 \\ 4\end{bmatrix}$


From here to find our $\vec{x}^*$ we just need to put the current substituted equation into a augmented matrix and then apply the [reduced row echelon](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to it
![[Pasted image 20260824184946.png]]

which now if we graph it, the least squares solution is in between all the lines of the intersections meaning that this is the closest solution between $\vec{b} = \begin{bmatrix} 2 \\ 1 \\ 4 \end{bmatrix}$


```desmos-graph
right=9; left=-9; 
---
y=2x-2
y=-\frac{1}{2}x + \frac{1}{2}
y=-x+4
(\frac{10}{7}, \frac{3}{7})|label:closest solution
```


We can now solve the minimize distance between $A\vec{x}^*$ and $\vec{b}$ ($||A\vec{x}^* - \vec{b}||$) which is found by substituting in values and then minus $\vec{b}$:

![[Pasted image 20260824185901.png]]

which when plotted we see the vector $A\vec{x}^*-\vec{b}$ creates an orthogonal vector onto the subspace of $C(A)$

```desmos-graph-3d
width=700;height=700;locked=true

---
v=(2t,1t,4t)|0<= t <= 1|label:vector b
s=(\frac{17}{7}t,\frac{16}{7}t,\frac{13}{7}t)\left\{0<=t<=1\right\}|#69db7c
c=(2\ +\ \frac{3}{7}\ t,1+\frac{9}{7}t,4+-\frac{15}{7}t)\left\{0<=t<=1\right\}|label:orthogonal complement|#ffd43b

-1x+-3y+5z=d|#9775fa
d=0
```

## Example 2
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthogonal-projections/v/linear-algebra-another-least-squares-example)

Another example is given the points:

$\begin{aligned} (-1, 0) \\[1em] (0, 1) \\[1em] (1, 2) \\[1em] (2,1) \end{aligned}$

Turning them into functions that follow $y = f(x) = mx + b$

$\begin{aligned} f(-1) = -m + b = 0 \\[1em] f(0) = b = 1 \\[1em] f(1) = m + b = 2 \\[1em] f(2) = 2m + b = 1 \end{aligned}$

if we try to solve this, it would have no single $y$ solution that solves all the systems 

If we plot them, we can validate that not a single intersection intersects every point at once

```desmos-graph
(-1,0)
(0,1)
(1,2)
(2,1)

```


In matrix form
![[Pasted image 20260826102651.png|484]]


so from here we need to apply $A^TA\vec{x}^*=A^T\vec{b}$  which first we must find $A^TA$ and $A^T\vec{b}$ 
![[Pasted image 20260826104134.png]]
![[Pasted image 20260826104142.png]]

So then substituting in the values into the equation:

$\begin{bmatrix} 6 & 2 \\ 2 & 4 \end{bmatrix} \vec{x}^* = \begin{bmatrix} 4 \\ 4\end{bmatrix}$


and to find out $\vec{x}^*$ we'll just need to apply reduced row echelon

![[Pasted image 20260826123625.png]]

which leaves us with the final equation:
$\begin{bmatrix} 6 & 2 \\ 2 & 4 \end{bmatrix} \begin{bmatrix} \frac{2}{5} \\ \frac{4}{5} \end{bmatrix} = \begin{bmatrix} 4 \\ 4\end{bmatrix}$

which if we plot we'll see that its the best solution between all the plotted points 

```desmos-graph
(-1,0)
(0,1)
(1,2)
(2,1)

y=\frac{2}{5}x + \frac{4}{5}
```
