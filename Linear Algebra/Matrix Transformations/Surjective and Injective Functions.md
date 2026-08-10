[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-transformations/v/surjective-onto-and-injective-one-to-one-functions)

## Surjective (onto)
Surjective functions are function where every element within the domain ($x\; \epsilon X$) has **at least** one element in the co-domain ($y \;  \epsilon \; Y$) that it maps to
![[Pasted image 20260724112810.png]]

A function removes its surjective-ness when there is an element that has no mapping to it from the domain:

| Surjective                           | Not Surjective                       |
| ------------------------------------ | ------------------------------------ |
| ![[Pasted image 20260724114951.png]] | ![[Pasted image 20260724115001.png]] |


The [image](Image%20of%20a%20subset%20under%20a%20transformation) of a function is surjective as it takes a set and maps each element in the domain to an element in the co-domain

### Is a transformation surjective?
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/inverse-transformations/v/determining-whether-a-transformation-is-onto)

A linear transformation is surjective only if its [rank](Column%20Space) equals the space its co-domain is in which is otherwise known as a **full rank**.

For instance, if a matrix's rank is $3$ and its co-domain is $R^3$ then the linear transformation is surjective. 

This is because, the key trait with surjective-ness is that every element in the co-domain must be mapped to from the domain, and so if there's an element in the co-domain that does not get mapped then it is not surjective.

Which, in correlation with rank, means that the pivot vectors are not enough to cover all of the linear combinations in a space. 

For instance, if we have:

$A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \\ 5 & 6 \end{bmatrix}$

And $A$ is the linear transformation where $T : \; R^2 \rightarrow R^3$

so then if we get the rank by putting A in [reduced row echelon form](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) ($rref(A)$) 
![[Pasted image 20260724140231.png]]
Then the $Rank(A) = 2$ but because the co-domain is $R^3$ we need the rank of $A$ to equal $3$ to achieve full rank in the co-domain and thus the linear transformation of $A$ is not surjective. 

So then because it's not surjective, the matrix $A$ cannot have an [inverse](Inverse%20of%20a%20Function) 
## Injective (One to one)

Injective functions are functions where for any element in the domain ($x \; \epsilon \; X$) there is **only one element** or a **unique solution** in the co-domain it maps to
![[Pasted image 20260724115246.png]]

When more than one element is being mapped to a single element in the co-domain ($y \; \epsilon \; Y$) then the function is no longer injective but can still be considered to be **surjective**
![[Pasted image 20260724115418.png]]

## Is a transformation injective?

A linear transformation can only be injective if the matrix's null space is trivial and only contains the $\vec{0}$

$N(A) = span(\vec{0})$

Which if that's the case then all the column vectors within the matrix are [linearly independent](Null%20space) thus when figuring out the [rank](Column%20Space) of the matrix, it must be a **full rank** where the matrix's rank must equal the space it's codomain is in

$Rank(A) = R^n$  

Where $T: \; R^n \rightarrow R^m$

This is because, for a function to be injective, it must only have one mapping for each value in the **domain** 

if there are other vectors within the null space that can be used to map to the $\vec{0}$ then those vectors can also be used to map to column vectors within matrix $A$ breaking the rule of injective

And thus cannot be invertible
