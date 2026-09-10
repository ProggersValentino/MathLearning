[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/linear-algebra-the-gram-schmidt-process)

The Gram-Schmidt Process is the **recursive process** of translating any basis of vectors into an orthonormal basis. The process involves [normalizing](Unit%20Vectors) a vector from the basis and using that normalized vector to build the orthonormal basis with [projections](Projections) to translate the vectors to be orthonormal to each other 

This is useful for when we have a basis that isn't orthonormal but we want to all the benefits an [orthonormal basis](Orthonormal%20Bases) provides

For instance, it have a regular non-standard basis which forms the subspace $V$

$basis = [\vec{v}_1, \vec{v}_2, ... \vec{v}_k]$

and we want to translate it into an orthonormal basis, then we have to start with a vector and normalize, so say we want create a 1-D subspace of $V_1$ which is just the span of $\vec{v}_1$

$V_1 = span(\vec{v}_1) = basis$

To orthonormal the basis, it needs to be normalized to magnitude of $1$ and orthogonal, so we can define $\vec{u}_1$ to be orthonormal vector where first we normalize it:

$\vec{u}_1 = \frac{\vec{v}_1}{||\vec{v}_1||} \hspace{1em} ||\vec{u}_1|| = ||\frac{\vec{v}_1}{||\vec{v}_1||}|| = (\frac{1}{||\vec{v}_1||}) ||\vec{v}_1|| = 1$

because $V_1$ is only the span of the vector $\vec{v}_1$ it is already orthogonal so to speak because it has no other vectors to be compared against so therefore:

$(\vec{u}_1) \; is \; an \; Orthonormal \; basis \; for \; V_1$

Now $\vec{u}_1$ becomes the foundation of orthonormalizing every other vector within the basis

For the second vector, lets isolate it within a subspace of $V_2$ where the span is $\vec{v}_1, \vec{v}_2$ but $\vec{v}_1$ can be substituted out for $\vec{u}_1$ because $\vec{u}_1$ can make $\vec{v}_1$ with a linear combination of $\vec{v}_1$ magnitude 
 
$V_2 = span(\vec{v}_1, \vec{v}_2) = span(\vec{u}_1, \vec{v}_2)$

To visualize it, $\vec{v}_2$ is a vector outside of the subspace $V_1$ and we want to find its orthogonal complement from $V_1$ to $\vec{v}_2$ that represents $\vec{v}_2$ orthonormal ($\vec{y}_2$)

![[Pasted image 20260902103858.png]]

with that as you can see we need to find $\vec{x} + \vec{y}_2$ to orthonormalize $\vec{v}_2$ which $\vec{x}$ is just the projection of $\vec{v}_2$ onto the subspace $V_1$ 

$Proj_{V_1}(\vec{v}_2) = (\vec{v}_1 \cdot \vec{u}_1) \vec{u}_1$ 

and $\vec{y}_2$ is $\vec{v}_2 - Proj_{V_1}(\vec{v}_2)$ which is our orthogonal vector needed for the orthonormal basis

$\vec{y}_2 = \vec{v}_2 - Proj_{V_1}(\vec{v}_2)$

Now that we have orthogonalize $\vec{v}_2$ to $\vec{y}_2$ we need to normalize it for it to become an orthonormal vector ($\vec{u}_2$)

$\vec{u}_2 = \frac{\vec{y}_2}{||\vec{y}_2||}$

so now the orthonormal basis for $V_2$ can be represented as:

$V_2 = span(\vec{u}_1, \vec{u}_2)$


But if we wanted to orthonormalize a basis in $R^3$ then we'll need to repeat process again to find its orthonormal vector using $\vec{u}_1, \vec{u}_2$. Say $V_3$ is the span of $\vec{v}_1, \vec{v}_2, \vec{v}_3$ but $\vec{v}_1, \vec{v}_2$ can represented with $\vec{u}_1, \vec{u}_2$:

$V_3 = span(\vec{v}_1, \vec{v}_2, \vec{v}_3) = span(\vec{u}_1, \vec{u}_2, \vec{v}_3)$

To visualize, we have $\vec{v}_3$ which is a vector outside of the subspace $V_2$ and we want to the orthogonal vector to $V_2$ which will be $\vec{y}_3$:

![[Pasted image 20260902111747.png]]

$\vec{v}_3$ can be defined in this case that its the linear combination of $\vec{x} + \vec{y}_3$ where $\vec{x} \; \epsilon \; V_2$ and $\vec{y}_3 \; \epsilon \; V_2^\perp$

As you can see $\vec{x}$ is just the projection of $\vec{v}_3$ onto the subspace $V_2$ which is the linear combination of the projection of $\vec{v}_3$ onto $\vec{u}_1$ plus the projection of $\vec{v}_3$ onto $\vec{u}_2$

$Proj_{V_2}(\vec{v}_3) = Proj_{\vec{u}_1}(\vec{v}_3) + Proj_{\vec{u}_2}(\vec{v}_3)$

$Proj_{V_2}(\vec{v}_3) = (\vec{v}_3 \cdot \vec{u}_1) \vec{u}_1 + (\vec{v}_3 \cdot \vec{u}_2)\vec{u}_2$

and $\vec{y}_3$ is just $\vec{v}_3$ minus the projection of $\vec{v}_3$ onto the subspace $V_2$ which is our orthogonal vector we need to find:

$\vec{y}_3 = \vec{v}_3 - Proj_{V_2}(\vec{v}_3)$

Expanded out the final equation is:

$\vec{y}_3 = \vec{v}_3 - ((\vec{v}_3 \cdot \vec{u}_1) \vec{u}_1 + (\vec{v}_3 \cdot \vec{u}_2)\vec{u}_2)$

and then $\vec{y}_3$ must be normalized to be considered orthonormal ($\vec{u}_3$) which like the past two processes, follows the same equation:

$\vec{u}_3 = \frac{\vec{y}_3}{||\vec{y}_3||}$

and this process continues on until you've translated your $k$ vector within the basis 

#### Unbiased version

However, the process has bias to the order of the vectors inputted where it orthogonalizes around the first vector inputted, like $\vec{v}_1$ will not change at all compared to $\vec{v}_3$ which might change substantially to be orthogonalize around $\vec{v}_1$. 

We can make the process unbiased by introducing a fraction ($k$) in which we select and we subtract the projection from the original axis which provides a more "true" orthonormal set of vectors:
![[Pasted image 20260907113613.png]]

### Example 2 basis vectors
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/linear-algebra-gram-schmidt-process-example)

For instance, if we have a plane where $x_1 + x_2 + x_3 = 0$ and the subspace $V$ is defined by the plane:

$Plane = x_1 + x_2 + x_3 = 0 \hspace{1em} x_2 = c_1, \;\; x_3 = c_2, \;\; x_1 = -c_1 - c_2$

$V = (\begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = c_1 \begin{bmatrix} -1 \\ 1 \\ 0 \end{bmatrix} + c_2 \begin{bmatrix} -1 \\ 0 \\ 1 \end{bmatrix} \; | \; c_1,c_2 \; \epsilon \; R) \hspace{2em} V = span(\begin{bmatrix} -1 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} -1 \\ 0 \\ 1 \end{bmatrix})$

and we want to orthonormalize $V$ to be an orthonormal basis which then we apply the gram-schmidt process to find the orthonormal basis for $V$

First we must find the orthonormal for $\vec{v}_1$ which can be defined as $\vec{u}_1$:
![[Pasted image 20260902121848.png]]
![[Pasted image 20260902121839.png]]

which now we can find our $\vec{u}_2$ where we must find the orthogonal vector to the subspace $V_1$ and then normalize it:
![[Pasted image 20260902122007.png]]
![[Pasted image 20260902122014.png]]

So now the orthonormal basis of $V$ can be represented as the span of $\vec{u}_1, \vec{u}_2$:

$V = span(\frac{1}{\sqrt{2}} \begin{bmatrix} -1 \\ 1 \\ 0 \end{bmatrix}, \sqrt{\frac{2}{3}} \begin{bmatrix} -\frac{1}{2} \\ -\frac{1}{2} \\ 1 \end{bmatrix})$

### Example 3 basis vectors
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/alternate-bases/orthonormal-basis/v/linear-algebra-gram-schmidt-example-with-3-basis-vectors)

For instance, if we have a subspace $V$ in $R^4$ which its basis is defined by $\vec{v}_1, \vec{v}_2, \vec{v}_3$

$V = Span(\begin{bmatrix} 0 \\ 0 \\ 1 \\ 1 \end{bmatrix}, \begin{bmatrix} 0 \\ 1 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 1 \\ 1 \\ 0 \\ 0 \end{bmatrix})$

and we want to find the orthonormal basis for $V$ where by the end of the process we'll have an orthonormal basis where $V$ will be represented as:

$V = Span(\vec{u}_1, \vec{u}_2, \vec{u}_3)$

To do this we apply the gram-schmidt process by first finding $\vec{u}_1$:
![[Pasted image 20260902143201.png]]

After that we can use $\vec{u}_1$ to find $\vec{u}_2$:
![[Pasted image 20260902143245.png]]

and then finally we can figure out $\vec{u}_3$ with $\vec{u}_1, \vec{u}_2$:
![[Pasted image 20260902143559.png]]

Leaving with the final representation of $V$ in an orthonormal basis be:

$V = Span(\frac{1}{\sqrt{2}} \begin{bmatrix} 0 \\ 0 \\ 1 \\ 1 \end{bmatrix}, \sqrt{\frac{2}{3}} \begin{bmatrix} 0 \\ 1 \\ \frac{1}{2} \\ -\frac{1}{2} \end{bmatrix}, \sqrt{\frac{3}{4}} \begin{bmatrix} 1 \\ \frac{1}{3} \\ -\frac{1}{3} \\ \frac{1}{3} \end{bmatrix})$

meaning any transformation within the subspace can be solved using the orthonormal basis generated providing the benefits [orthonormal bases](Orthonormal%20Bases) gain when applied