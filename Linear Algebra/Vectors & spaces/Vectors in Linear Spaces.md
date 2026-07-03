[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/vectors/v/vector-introduction-linear-algebra)

we already know that:
![[Intro To Vectors & Scalars#^whatIsAVector]]


and that there are different types that are either vector quantities or non-vector quantities:
![[Intro To Vectors & Scalars#^d77baf]]

but in Linear Algebra, Vectors are generally represented like matrices:

$\begin{bmatrix} x \\ y \end{bmatrix}$ instead of $(x, y)$ which is more associated with points 


#### What is a point?
A **point** is a set of numbers to describe a location but it does not have a direction, thickness or length **unlike a vector**

## Relationship between points and vectors
[game math chp2.4](https://gamemath.com/book/vectors.html#:~:text=with%20vector%20addition.-,2.4,Vectors%20versus%20Points,-Recall%20that%20a) 

The relationship that points share with vectors is that from the origin, if a point moves based on vector $[x, y]$ it will end up at the location described by point $(x, y)$ 

This is true because all position is relative: the position of something is defined when in relation to another know location.

For instance, if we have an origin of $(0,0,0)$ and a point $(3, 7, 2)$ then the vector will be positive with the values of $[3,7,2]$ because relative to the origin, the point moves in a positive direction.

However if we change the origin to start at $(10, 15, 6)$ then our point of $(3,7,2)$ when getting the vector will produce a negative vector of $[-7,-8,-4]$ because relative to the new origin, to displace to the point, the vector must displace in a negative direction