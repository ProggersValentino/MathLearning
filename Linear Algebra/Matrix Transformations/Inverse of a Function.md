[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-transformations/v/linear-algebra-introduction-to-the-inverse-of-a-function)

As mentioned previously, a [function](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FFunction) is a relation from a set of numbers to another 

$f(x) = y$
$f: \; X \rightarrow Y$


Functions are invertible when there is some inverse function where it reverses the relation of a number set:

$f^{-1}: \; Y \rightarrow X$

Where it's only invertible if $f$ is both [surjective and injective](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FSurjective%20and%20Injective) and fulfills two rulesets of [composition](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FComposition%20of%20Linear%20Transformations)

| Rule                   | Meaning                                                                      |
| ---------------------- | ---------------------------------------------------------------------------- |
| $f^{-1} \circ f = I_x$ | The composition of $f^{-1}$ with $f$ must equal the Identity function of $x$ |
| $f \circ f^{-1} = I_y$ | The composition of $f$ with $f^{-1}$ must equal the identity function of $y$ |
Which means that the domain and co-domain must be within the same space and if each rule is fulfilled, then the function is considered invertible. 
 
![[Pasted image 20260722161414.png]]


When a function is considered invertible then it implies that there is a **unique solution** within the equation $f(x) = y$ for any $y$ that's in the co-domain of the function.

This means that inverse functions must be **[Injective](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FMatrix%20Transformations%2FSurjective%20and%20Injective)** or One-to-One

This comes down to applying the two composition rules where if we take the inverse ($f^{-1}$) of our function ($f(x)$) then we will get the identity function ($I_x$) which then just gives us the domain of the function and vice versa if we want to get the identity of the codomain ($I_y$) 

for instance:

$f(x) = y$

$f^{-1}(f(x)) = f^{-1}(y)$

$f^{-1}(f(x)) = I_x(x) = x$

$x = f^{-1}(y)$


## Is Inverse functions a linear transformation
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-transformations/v/linear-algebra-showing-that-inverses-are-linear)

Inverse functions are a linear as they fulfill the two rules needed to be a linear transformation:

![[Function#^LinearTransformationRules]]

![[Pasted image 20260727170116.png]]

So then if $T$ is a linear transformation and is **invertible** then $T^{-1}$ is also a linear transformation which means that $T^{-1}$ can be represented as a matrix

$T^{-1}(\vec{x}) = A^{-1}\vec{x}$

which then if we apply the composition of $T$ with $T^{-1}$ then we will get the identity matrix of $R^n$ 

$T \circ T^{-1} = I_{R^n}$

and if combined in a linear transformation of

$(T \circ T^{-1})(\vec{x}) = A \; A^{-1}\vec{x} = I_n$

Which proves that any matrix multiplied against its [inverse matrix](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FInverse%20Matrices) will equal the identity matrix

