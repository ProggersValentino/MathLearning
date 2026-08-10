h[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/linear-algebra-cross-product-introduction), [game math 2.12](https://gamemath.com/book/vectors.html), [khan acad triple product](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/vector-triple-product-expansion-very-optional)

#### What is the Vector Cross Product? 
The cross product is a multiplication calculation done with input vectors which **yields** a vector **orthogonal** to the original inputted vectors, this can only be done in a **3-dimensional space**:

$\begin{bmatrix} x_1 \\ y_1 \\ z_1 \end{bmatrix} \times \begin{bmatrix} x_2 \\ y_2 \\ z_2 \end{bmatrix} = \begin{bmatrix} (y_1 \cdot z_2) - (z_1 \cdot y_2) \\ (z_1 \cdot x_2) - (x_1 \cdot z_2) \\ (x_1 \cdot y_2) - (y_1 \cdot x_2) \end{bmatrix}$

For instance:
$\begin{bmatrix} 1 \\ 3 \\ 4 \end{bmatrix} \times \begin{bmatrix} -2 \\ 7 \\ 3 \end{bmatrix} = \begin{bmatrix} (3 \cdot 3) - (4 \cdot 7) \\ (4 \cdot -2) - (1 \cdot 3) \\ (1 \cdot 7) - (3 \cdot -2) \end{bmatrix} = \begin{bmatrix} (9) - (28) \\ (-8) - (3) \\ (7) - (-6) \end{bmatrix} = \begin{bmatrix} -19 \\ -13 \\ 11 \end{bmatrix}$


Furthermore, when combining with the **dot product**, the prioritization goes to the cross product **first** and then solving the dot product **second**

$\vec{a} \cdot \vec{b} \times \vec{c} = \vec{a} \cdot (\vec{b} \times \vec{c})$

As mentioned earlier, the cross product yields an orthogonal vector from the two vectors:
![[Pasted image 20260623100150.png]]

which to find the length of $\vec{a} \times \vec{b}$:

$||\vec{a} \times \vec{b}|| = ||\vec{a}||||\vec{b}||sin\theta$

If the product of $\vec{a} \times \vec{b}$ is **equal to $0$** then vectors $\vec{a}$ and $\vec{b}$ are parallel from each other.

While we know the result of a **cross product** is **perpendicular** to the inputted vectors, there's still a need to determine which direction that product will go. 

This is dependent on the [coordinate system](Coordinate%20Spaces) that is being used as if it determines if we should do a **clockwise** or **counter-clockwise** turn from the vectors:


|                              | Clockwise Turn<br>![[Pasted image 20260623105300.png]] | Counter-clockwise turn<br>![[Pasted image 20260623105317.png]] |
| ---------------------------- | ------------------------------------------------------ | -------------------------------------------------------------- |
| Left-hand Coordinate System  | $\vec{a} \times \vec{b}$ points towards you            | $\vec{a} \times \vec{b}$ point away from you                   |
| Right-hand Coordinate System | $\vec{a} \times \vec{b}$ point away from you           | $\vec{a} \times \vec{b}$ points towards you                    |

Generally to determine the angle between the vectors we have the vectors touching **tail-to-tail** whereas to determine which way it rotates the vectors need to be touching **head-to-tail**
