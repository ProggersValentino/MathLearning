[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/composition-of-transformations/v/compositions-of-linear-transformations-1), [khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/composition-of-transformations/v/compositions-of-linear-transformations-2)

## What is a Composition?
Composition of linear transformations is a process of applying one linear transformation with another linear transformation. This results in a single linear transformation that can generate a transformation from one subset to any desired one which is generally represented as:

$T \circ S: \; X \rightarrow Z$

Which is referred to as the composition of a linear transformation ($T$) with another linear transformation ($S$)

For instance, if we have vector spaces of $X, Y, Z$ where each create a linear transformation to the next space but we want find the linear transformation of subset $X$ to subset $Z$ 
![[Pasted image 20260722105343.png]]

Then we need to do the linear transformation of $X \rightarrow Y$ to then $Y \rightarrow Z$ in one linear transformation which its definition can be represented as a composition: 

$T \circ S: \; X \rightarrow Z$

And because this is a linear transformation where it fulfills the two necessary rules:
![[Function#^LinearTransformationRules]]

Compositions can be represented in [matrix vector product](Matrix%20vector%20products) form:

$T \circ S = B(A\vec{x}) = C\vec{x}$

With this we are able to create an image of $I_n$ from the composition of $T$ with $S$ where we substitute in each column vector of $I_n$ into the linear transformation. 

![[Pasted image 20260722112531.png]]

Fortunately, this process can be completed faster by just applying [matrix multiplication](Matrix%20Multiplication) of each transformation matrix to find the linear transformation between vector space $X$ and $Z$ when applying any vector in the space of $X$:

$BA$
