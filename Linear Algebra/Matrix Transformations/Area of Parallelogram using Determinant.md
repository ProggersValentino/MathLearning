[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/determinant-depth/v/linear-algebra-determinant-and-area-of-a-parallelogram)

Determinants can be used to find the area of a parallelogram, how?

If we take a matrix

$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$

and put it in its vector form

$\vec{v_1} = \begin{bmatrix} a \\ c \end{bmatrix} \;\;\; \vec{v_2} = \begin{bmatrix} b \\ d \end{bmatrix}$

Given the two vectors, they span together to create a parallelogram because the vector addition is [communitive](Vector%20Properties):

![[Vector Addition & Subtraction#^parallelogramRule]]

![[Pasted image 20260803150610.png|700]]

To find the area of a parallelogram, it follows the formular of 

$A = B \cdot H$

Given $H$ is a orthogonal vector, we can apply Pythagorean theorem where $a^2 = b^2 + c^2$ which $H = b$ so therefore

$H^2 = ||\vec{v_2}||^2 - B^2$

To get $B$, it is the $||\vec{v_1}||$ to where it intersects on the line $H$. which is [the projection](Projections) of $\vec{v_2}$ the onto a line which is $\vec{v_1}$ simplifying the equation to:

$H^2 = ||\vec{v_2}||^2 - (Proj_L\vec{v_2})^2$

$L = Span(\begin{bmatrix} a \\ c \end{bmatrix})$

Which when expanded becomes

$H^2 = \vec{v_2} \cdot \vec{v_2} - \Large{||{\vec{v_2} \cdot \vec{v_1} \over \vec{v_1} \cdot \vec{v_1}} \vec{v_1}||}^2$

We can expand and simplify this further by applying algebraic conventions to eventually end with:

$(Area)^2 = (ad-bc)^2$

![[Pasted image 20260803155412.png|700]]

The final equation is the formula to solve a [determinant](Determinant%20Matrices) of matrix squared which evaluates to the area of a parallelogram equaling the absolute value of the determinant of a matrix: 

$Area \; of \; Parallelogram = |det(A)|$
