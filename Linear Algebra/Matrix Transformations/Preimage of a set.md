
In the event where we have a subset of a codomain and need to figure out the subset of a domain which is called a **Preimage of a subset** which can be represented as the inverse of a transformation ($T^{-1}(S)$):

$\vec{x} \; \epsilon \; X \; | \; T(\vec{x}) \; \epsilon \; S$
![[Pasted image 20260715104251.png]]

Now the image of the preimage, is where if taking all the vectors within the preimage, what vectors will map within the codomain. 
This does not mean all vectors within the preimage will map to the codomain subset vectors which turns into a subset within the codomain which is generally represented as:

$T(T^{-1}(S)) \; \subseteq \; S$

For instance, if we want to transform a subset of vectors from $R^2$ to $R^2$ with the respective transformation:

$T(\vec{x}) = \begin{bmatrix} 1 & 3 \\ 2 & 6 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$

And we want to find the preimage of $S$ where all vectors in the preimage, when applied against the transformation, will associate with any vector within the subset of the codomain:

$S = (\begin{bmatrix} 0 \\ 0 \end{bmatrix}\; \begin{bmatrix} 1 \\ 2 \end{bmatrix})$
$(\vec{x} \; \epsilon \; R^2 \; | \; T(\vec{x}) \; \epsilon \; S)$

![[Pasted image 20260715122147.png]]

Which will leave us with the respective transformations:

$\begin{aligned} T(\vec{x}) = \begin{bmatrix} 1 & 3 \\ 2 & 6 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix} \\[1em] T(\vec{x}) = \begin{bmatrix} 1 & 3 \\ 2 & 6 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix} \end{aligned}$

which now to we just need to apply [reduce row echelon](Reduced%20Row%20Echelon%20with%20Matrix%20Row%20Operations) to find the preimage S:
![[Pasted image 20260715122927.png]]

So then if we graph it we can visualize the two lines where if we apply any scalar value and the respective transformation to them, then we will get the **image of S under T** or $T(S)$:
![[Pasted image 20260715123343.png]]

### Kernal
The kernal of a transformation is all of the vectors in a domain where the transformation of those vectors equal 0 which is the [null space](Null%20space) of a subset:

$$