[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/vectors/v/real-coordinate-spaces)

When working with coordinate spaces, generally mathmeticians represent a space with $R^n$ 

This symbol represents all possible real-values within **n-tuples**

So $R^2$ means we're working with real-numbers in 2-tuples which is a **2-dimensional space** which means vectors are represented like:

$\begin{bmatrix} x \\ y \end{bmatrix}$

![[Pasted image 20260611155223.png]]

we can represent the vector through a few symbols:

$\overrightarrow{x} = \begin{bmatrix} 3 \\ 1 \\ 8 \end{bmatrix}$

tuple $x$ can be represented:

$\overrightarrow{x}\epsilon R^3$ 

Which means that $\overrightarrow{x}$ is a coordinate set for 3-dimensional spaces

#### 2D Cartesian Coordinate Space 
[game math - cartesian space](https://gamemath.com/book/cartesianspace.html)

2D Cartesian Coordinate Space defines location within a 2-dimensional space.
![[Pasted image 20260611161837.png]]

it is defined using a 2D cartesian plane which is always defined by two factors:
- The plane an **origin point** which defines the starting point
- The plane has a vertical and horizontal line which are defined as the **x- and y-axis**
The orientation of the plane does matter as long as it can be rotated to the normal orientation which is where the **$x$-axis faces to the right** and the **$y$-axis faces up** 

To represent each location in a 2D space, we use points formatted like $(x, y)$ as generally, it defines the order of how we read positions:

we move across the $x$-axis first before moving up/down on the $y$-axis

![[Pasted image 20260611163257.png]]

#### 3D Cartesian Space

3-dimensional space just an extra dimension, which is the **$z$-axis**, where each axis is perpendicular to each other axis 
![[Pasted image 20260611165647.png]]

Each location in 3-dimensional space is represented with with 3 numbers:

$R^3 = \begin{bmatrix} x \\ y \\ z \end{bmatrix}$

Earlier in 2D spaces, it doesnt matter what orientation we set it too as we can always rotate it back to the normal orientation. 

However, this can't be achieved with 3D spaces, as if we flip the z-axis and try to line it up to its normal orientation, all 3 axis' will never be aligned to its normal orientation. which brings us to the sub-types of 3D space which is **left-handed coordinate** and **right-hand coordinate**


| Coordinate Type       | Example                              | Normal Orientation                                                                      |
| --------------------- | ------------------------------------ | --------------------------------------------------------------------------------------- |
| Left-hand coordinate  | ![[Pasted image 20260611171528.png]] | $\Large{\begin{aligned} +x = right \\[2em] +y = up \\[2em] +z = forward \end{aligned}}$ |
| Right-hand Coordinate | ![[Pasted image 20260611171545.png]] | $\Large{\begin{aligned} +x = left \\[2em] +y = up \\[2em] +z = forward \end{aligned}}$  |
As shown above, the normal orientation of a 3D space is dependent on the handedness of the coordinate. This is also for rotations when defining which way should be **negative** and **positive** rotations


| Left-hand rule                                  | Right-hand rule                                     |
| ----------------------------------------------- | --------------------------------------------------- |
| ![[Pasted image 20260611173407.png]]            | ![[Pasted image 20260611173419.png]]                |
| Denotes positive rotations happen **Clockwise** | Denote positive rotations happen **Anti-clockwise** |

The table below showcases different cycles of left- and right-handed rules and how it affects each axis'

| When looking  <br>towards the origin  from… | Positive Rotation<br>                                              | Negative Rotation                                                  |
| ------------------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
|                                             | Left-handed: **Clockwise**<br><br>Right-handed: **Anti-clockwise** | Left-handed: **Anti-clockwise**<br><br>Right-handed: **Clockwise** |
| $+x$                                        | $+y \rightarrow +z \rightarrow -y \rightarrow -z \rightarrow +y$   | $+y \rightarrow -z \rightarrow -y \rightarrow +z \rightarrow +y$   |
| $+y$                                        | $+z \rightarrow +x \rightarrow -z \rightarrow -x \rightarrow +z$   | $+z \rightarrow -x \rightarrow -z \rightarrow +x \rightarrow +z$   |
| $+z$                                        | $+x \rightarrow +y \rightarrow -x \rightarrow -y \rightarrow +x$   | $+x \rightarrow -y \rightarrow -x \rightarrow +y \rightarrow +x$   |


For instance, the Unity game engine uses a **left-hand coordinate space** when developing 3D games 


### Defining a plane in R3 with point and normal vector
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/defining-a-plane-in-r3-with-a-point-and-normal-vector)

