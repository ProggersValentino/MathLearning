
A relation of one set in relation to another set of members. 

$f(x) = y$

If you give a member of x then the function will return a member of y associated (or mapping it) with x

![[Pasted image 20260709160442.png]]


How does it relate? 

$f(x) = x^2$

the function defines where you can input an real number and in return you get a real number. 

In functions, the input value is referred to as the **domain** and a result from a function is a **co-domain** being the set that the domain is being mapped to.
![[Pasted image 20260709161028.png]]

Theres also **Range** which is a subset of the co-domain that the function actually maps to 

If the co-domain of a function deals with $R^1$ then it is considered to be a **scalar or real number function**

However any function that extends from $R^2$ and above is considered to be a **vector valued function**

## Vector Transformations
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/linear-transformations/v/vector-transformations)

Transformation is a function operating on vectors where its transforming one vector to another which the notation used is $T$

for instance: 

$T:R^3 -> R^2$

$T(x_1, x_2, x_3) = (x_1 + 2x_2, 3x_3)$

the above is just an established function but we know it involves some forms of vectors within it where its transforming a vector in $R^3$ to a vector in $R^2$ by following the 
![[Pasted image 20260709164243.png]]

## Linear Transformation
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/linear-transformations/v/linear-transformations)

A linear transformation is a function where it must follow **two rules** to be true which is:

| Rule                                                                                                               | Equation                                         |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------ |
| The sum of vectors **are equal** to the transformation of each vector summed together                              | $T(\vec{a} + \vec{b}) = T(\vec{a}) + T(\vec{b})$ |
| the transformation of any scaled vector **should equal** to the scalar multiplied the transformation of the vector | $T(c\vec{a}) = c \; T(\vec{a})$                  |
^LinearTransformationRules

For instance say we have: 

$\begin{aligned} T:R^2 \rightarrow R^2 \\[1em] T \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} x_1 + x_2 \\ 3x_3 \end{bmatrix} \end{aligned}$

![[Pasted image 20260709170939.png]]

An invalid linear transformation is where components within vector are multiplied by themselves or have exponents applied that will violate the two rules like for instance:

$T(\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}) = \begin{bmatrix} x_1^2 \\ 0 \end{bmatrix}$

applying the same vectors, we see that it violates the scalar multiplication rule where $c$ becomes $c^2$:
![[Pasted image 20260709172604.png]]

## Identity Functions

Identity functions have a special purpose in that any domain applied will map its co-domain to be the same value as its domain:

$I_x: \; X \rightarrow X$

For instance if we have a domain of $a$ then its co-domain will be $a$
$I_x(a) = a$
![[Pasted image 20260722153939.png]]

In some sense this acts as like a loop where it will just loop back and equal the same value as it's input. 

If we put this in matrix form, this behaviour is the equivalent to multiplying a matrix by a [Identity matrix](Identity%20Matrix) within the same $R^n$ space

