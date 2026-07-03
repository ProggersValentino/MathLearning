[khan acad vid](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-matrices-as-transformations/v/transforming-position-vector), [khan acad](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-matrices-as-transformations/a/matrices-as-transformations)

Matrix multiplication can be used for more complex applications like transformation in digital space. each matrix dimension represents a set of space in the digital work like $2 \times 2$ is within the realm of a 2-dimensional space, $3 \times 3$ is in the realm of 3-dimensional space.

First though, how does  $1 \times 1$ matrices be in the realm of transformations in a 1-dimensional space. 

1-dimensional space can be seen as a simple line of numbers
![[Pasted image 20260601093303.png]]

When we multiply those numbers by a scalar of **2** you'll see that the numbers on the line do this:
![[Pasted image 20260601093845.png]]

As you can see (quite obviously), the numbers **scale** to **2 times the size** of the original line which we can tell because **1 has transformed to the position of 2** 

similarly if we multiply by $1 \over 2$ then we get: 
![[Pasted image 20260601094647.png]]

Each number has been **scaled** to $1 \over 2$ times the scale of the original.

This can also be seen for negative numbers, where simply by whatever scalar reverses the numbers on the scale, lets take a scalar of **-3** for instance:
![[Pasted image 20260601100305.png]]

All this is represented as "Linear Transformations of 1-dimensional space". 

When we use "transformation" its adjacent to "function": something that takes in a number and out puts a number like $f(x) = 2x$.

When using "transformation", instead of visualizing the numbers on graphs, its tend to be more orientated to **visualize an action** of an object whether its moving, stretching, squishing, rotating etc. 

So translating $f(x) = 2x$ to a transformation gives the first example shown earlier where the line is multiplied by the **scalar of 2** where it moves point 1 to where 2 starts off, moves point 2 to where 4 starts off etc.

All these transformations follow the geometric rule: The **origin must remain fixed** and **all lines must remain lines** make all transformations linear 

Take this transformation:
![](https://www.youtube.com/watch?v=XUw95PFP1RE)

Remember: 
![[Algebra/Matrices/Matrix Multiplication#Summary]] 

We can see that two vectors start off at $p1 =\begin{bmatrix} 1 \\ 0\end{bmatrix}$ and $p2 = \begin{bmatrix} 0 \\ 1\end{bmatrix}$ and ended at: 
$\begin{aligned} p1 = \begin{bmatrix} 1 \\ -2\end{bmatrix} \\ p2 = \begin{bmatrix} 3 \\ 0\end{bmatrix}\end{aligned}$

which from this we can establish that any vector transforming on the **x-axis** will result in
 $\begin{bmatrix} 1 \\ -2\end{bmatrix} \cdot \begin{bmatrix} x \\ 0\end{bmatrix} = \begin{bmatrix} 1x \\ -2\end{bmatrix}$ 
 
 and any vector transforming on the **y-axis** will result in:
$\begin{bmatrix} 3 \\ 0\end{bmatrix} \cdot \begin{bmatrix} 0 \\ y\end{bmatrix} = \begin{bmatrix} 3x \\ 0\end{bmatrix}$

allowing us now to predict practically any vector's end point after transformation.

for instance, lets take the vector $\begin{bmatrix} -1 \\ 2\end{bmatrix}$ using the pre-established scaling we can deduce that after transformation the result will be $\begin{bmatrix} 5 \\ 2\end{bmatrix}$

based off combining the x and y equations: ${\color{green}\begin{bmatrix} 1 \\ -2\end{bmatrix}} \cdot \begin{bmatrix} -1 \\ 0\end{bmatrix} + {\color{red}\begin{bmatrix} 3 \\ 0\end{bmatrix}} \cdot \begin{bmatrix} 0 \\ 2\end{bmatrix} = \begin{bmatrix} 5 \\ 2\end{bmatrix}$ 

**OR**

$-1 \cdot {\color{green}\begin{bmatrix} 1 \\ -2\end{bmatrix}} + 2 \cdot {\color{red}\begin{bmatrix} 3 \\ 0\end{bmatrix}} = \begin{bmatrix} 5 \\ 2\end{bmatrix}$

![](https://www.youtube.com/watch?v=gNMGlQ62MBY)

## Transforms in a 2-dimensional space

As was shown above, each vector $\begin{bmatrix} x \\ y \end{bmatrix}$ can be broken down to:

$x \cdot {\color{green}\begin{bmatrix} 1 \\ 0\end{bmatrix}} + y \cdot {\color{red}\begin{bmatrix} 0 \\ 1\end{bmatrix}} = \begin{bmatrix} x \\ y\end{bmatrix}$

so then expanding it to a $2 \times 2$ matrix (2-dimensional space) say we have:
$A = \begin{bmatrix} a && b \\ c && d\end{bmatrix}$ 

how do we determine what **x and y** are?

well given the broken down of $\begin{bmatrix} x \\ y\end{bmatrix}$, each matrix column will tell us where the final vector will be, so if we have $x = \color{green}\begin{bmatrix} 1 \\ 0\end{bmatrix}$ and **multiply against** the first column of $A$ being $\begin{bmatrix} a \\ c \end{bmatrix}$ we'll get $\begin{bmatrix} a{\color{green}x} \\ c{\color{green}x} \end{bmatrix}$ 
likewise if do it with $y = {\color{red}\begin{bmatrix} 0 \\ 1 \end{bmatrix}}$ to the second column of $A$ being $\begin{bmatrix} b \\ d \end{bmatrix}$ we'll get a result of $\begin{bmatrix} b{\color{red}y} \\ d{\color{red}y} \end{bmatrix}$
so $Av = \begin{bmatrix} ax + by \\ cx + dy \end{bmatrix}$
