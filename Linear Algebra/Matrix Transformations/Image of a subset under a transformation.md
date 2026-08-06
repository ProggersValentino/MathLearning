[khan acad vid](https://www.khanacademy.org/math/linear-algebra/matrix-transformations/linear-transformations/v/image-of-a-subset-under-a-transformation)

The image of a subset when transformed is where a transformation takes in a a subset of vectors and creates a new image from it by transforming the vectors. 

For instance, take the vectors $\vec{x_0}, \vec{x_1}, \vec{x_2}$ in $R^2$, we can create a triangle shape from these vectors by applying $p_2 - p_1 = \vec{v_1}$ to which creates a new vector relative to the two points we're inputting:
![[Pasted image 20260713150025.png]]

And we want to apply the linear transformation of:

$T(\vec{x}) = \begin{bmatrix} 1 & -1 \\ 2 & 0 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$

So then taking in one of our line definitions, we adjust the definition to match the [rules of a linear transformation](Function#Linear Transformation) which will make it easier to discern what needs to be done, taking a line definition from:
$L_0 = {\vec{x_0} + t(\vec{x_1} - \vec{x_0} | 0 \le t \le 1)}$

to: 
$T(L_0) = T(\vec{x_0}) + t(T(\vec{x_1} - \vec{x_0})) \; |\; 0 \le t \le 1$

this is achievable because all that is being done step by step is applying the **two rules** to break down the definition into a digestible linear transformation: 
![[Pasted image 20260713153145.png]]

which now all that needs to be done is to find the transformation of each vector and apply the necessary transformed line definition to **create the new image** after being transformed:
![[Pasted image 20260713152555.png]]

So then we can say:

$T(L_0)$ is the image of $L_0$ under $T$ 
$T(L_1)$ is the image of $L_1$ under $T$ 
$T(L_2)$ is the image of $L_2$ under $T$ 

which is just saying, that this is the vector transformation under this specific linear transformation function.

but this can be summed up further by encapsulating all the vectors under a shape definition and saying:

$T(S)$ is the image of $S$ under $T$

### Image of a transformation: Im(T)
When taking all of the n-dimensional space and finding its image (generally a subspace), the terminology refers to it as the image of a transformation which is represented:

$im(T)$

The subset of a codomain when mapping all of the elements of a domain into its codomain is the **image of a transformation**

The Image of a transformation is the equivalent of the [column space](obsidian://open?vault=MathLearning&file=Linear%20Algebra%2FVectors%20%26%20spaces%2FDrawings%2Fcolumn%20sapce) of the matrix that getting represented 
![[Pasted image 20260727092916.png]]