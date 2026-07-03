[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/defining-a-plane-in-r3-with-a-point-and-normal-vector)

The equation of a plane defines a plane and states that given a point $p = (x, y, z)$ multiplied by the components of the normal vector which define the plane's orientation $\vec{n} = (A, B, C)$ will determine if the point is on the plane:

$Ax + By + Cz = D$
^equationOfPlane

which means every $x, y, z$ applied by this equation will determine whether that point is on the plane by outputting either the same constant number defined in the equation or different. 

This can be simplified further by taking a **normal vector** perpendicular to the plane (which defines the orientation of the plane) and a point using the [dot product](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FVector%20Dot%20Product%20%26%20Length) against them:

$\begin{aligned} \vec{n} = a\hat{i} + b\hat{j} + c\hat{k} \\[1em] \vec{a} = (x, y, z) \\[1em] \vec{n} \cdot \vec{a} = D \end{aligned}$

![[Pasted image 20260619161803.png]]

If we have a **normal vector that is perpendicular** to the new vector calculated from the dot product of $\vec{x_0}$ and $\vec{x}$ which means their dot product will equal $0$ where the individual vectors $\vec{x_0} \; \vec{x}$ do not necessarily begin on the plane but rather only a point on the plane whereas the vector they create a vector of $\vec{\vec{x} - \vec{x_0}}$ which will lie on the plan:
![[Pasted image 20260619161816.png]]

which is shown: 
![[Pasted image 20260619161838.png]]


## Find Normal Vector from plane equation
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/normal-vector-from-plane-equation)

So now that we know that any point can be found on a plane given the equation:

![[Equation of a Plane#^equationOfPlane]]

The normal vector can be represented as:

$\vec{n} = A\hat{i} + B\hat{j} + C\hat{k}$

![[Pasted image 20260626133402.png]]


and because its a normal vector it will be perpendicular to the plane. Furthermore, we are able to convert an equation of a plane to a normal vector by substituting the $x, y, z$ for $\hat{i}, \hat{j}, \hat{k}$:
![[Pasted image 20260626134809.png]]

By doing this the plane's orientation is now defined by the normal vector read from the equation. 
## Point Distance to Plane
[khan acd vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/point-distance-to-plane)

If we have a point that starts on the plane but ends off the plane, how do we effectively measure the distance that point is from the plane? 

![[Pasted image 20260629105442.png]]

Well, we can figure out the magnitude of $\vec{f}$ which will give the length of the **hypotenuse** but we still need to figure out the **distance to plane**. 

If we then add an angle in between our hypotenuse and distance to plane then it allows us to use trionometry:

$cos\theta = {adj \over |\vec{f}|}$

or simply

$adj = |\vec{f}| \; cos\theta$

but because we don't what theta is we can't fully figure out but the angle will be the same as **the normal vector ($\vec{n}$)** because its going in the same direction so we can substitute in the normal vector:
![[Pasted image 20260629111224.png]]

which now its clear that the equation is just the dot product between $\vec{f}$ and $\vec{n}$ because ![[Defining the angle between vectors#^angleBetweenVectors]]
so therefore it can be simplified to:
$distance \; to \; plane = \Large{\vec{f} \cdot \vec{n} \over ||\vec{n}||}$

which now the shortest distance from the point to the plane can be calculated:
![[Pasted image 20260629111832.png]]


## Distance Between planes
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/distance-between-planes)

We can apply the same concept to finding the distance between **two parallel planes** (where the planes don't intersect)
![[Pasted image 20260629160456.png]]
![[Pasted image 20260629160346.png]]

so to get the distance between the planes we need to get the **normal vector** of the second plane which we have 2 points. but we need 3 to allow us to generate two unique vectors to apply the cross product. 

We can achieve this by taking one of the equations and substituting numbers into the $(x,y,z)$ to get the point to equal $(1, 1, 1)$:

$\begin{aligned} {x - 1 \over 1} = {y - 2 \over 2} = {z - 3 \over 3} \\[1em] {2 - 1 \over 1} = {4 - 2 \over 2} = {6 - 3 \over 3} \\[1em] p_1 = (1,2,3) \\[1em] p_2 = (2, 4, 6) \\[1em] p_3 = (3, 1, 5) \end{aligned}$

which now that we have our 3 points we can figure out $\vec{a}$ and $\vec{b}$ and find the cross product:
![[Pasted image 20260629155641.png]]


Next, we need to find the **equation of the plane** for the second plane to determine if the plane is parallel which is doing the **dot product** of $\vec{n}$ and any point on the plane:
![[Pasted image 20260629155939.png]]

which finalizes our equation to: $7x + 4y - 5z = D$

and then to find the distance, like earlier we do:

$distance = \Large{\vec{n} \cdot \vec{a} - d \over ||\vec{n}||}$

![[Pasted image 20260629160409.png]]