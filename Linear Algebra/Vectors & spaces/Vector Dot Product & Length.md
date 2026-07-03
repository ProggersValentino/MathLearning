[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/vector-dot-product-and-vector-length)

#### What is the Vector Dot Product
The dot product is multiplying two vectors which results in a **single scalar value** where it defines the product of the **lengths of vectors moving in the same direction**:
$\begin{aligned} \vec{a} \cdot \vec{b} = scalar \\[1em] \begin{bmatrix} a_1 \\ a_2 \\ . \\ . \\ a_n \end{bmatrix} \cdot \begin{bmatrix} b_1 \\ b_2 \\ . \\ . \\ b_n \end{bmatrix} \end{aligned} = (a_1 \cdot b_1) + (a_2 \cdot b_2) ... + (a_n \cdot b_n)$

for instance:
![[Pasted image 20260615135843.png]]
#### What is a Vector Length
Vector Length in vector math is the definition of [vector magnitude](obsidian://open?vault=MathLearning&file=Algebra%2FVectors%2FMagnitude)

$||\vec{a}|| = \sqrt{a_1^2 + a_2^2 + a_3^2 ... + a_n^2}$


The relationship that the vector length and dot product have is if we do 

$\vec{a} \cdot \vec{a} = (a_1 \cdot a_1) + (a_2 + a_2) \; ... \; (a_n \cdot a_n)$

the **dot product result** is the same as $a_1^2 + a_2^2$ so getting $||\vec{a}||$ can be simplified to: 

$||\vec{a}|| = \sqrt{\vec{a} \cdot \vec{a}}$


#### Geometric Definition
[game math chp 2.11](https://gamemath.com/book/vectors.html), [khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products/v/dot-and-cross-product-comparison-intuition)
##### Projection
One geometric definitions concerns the dot product performing a projection:

The dot product $\vec{a} \cdot \vec{b}$ is equal to the signed length of the projection of $b$ onto any line parallel to $a$ , multiplied by the length of $a$.
^dotprodGeometricDef1

if we have $\hat{a}$ and $\vec{b}$ of any direction and magnitude then if we get the **dot product** we will get its projection and if $\vec{b}$ goes in a negative direction to $\hat{a}$ then the dot product will be negative

However, if $\vec{b}$ goes **perpendicular** to $\hat{a}$ then the result will be $0$:

![[Pasted image 20260615145220.png]]

So with this we can work out a **rough relative direction** of the two vectors when we have any vector which is perpendicular to $\hat{a}$ allowing us to determine which half space the vector lies in:
![[Pasted image 20260615150243.png]]


##### Intercepted Angles
The second geometric definition of the dot product has to do with Intercepted Angles:

The dot product of two vectors **is equal** to the $cos\theta$ between the vectors, multiplied by the lengths of the vectors (see [Figure 2.26](https://gamemath.com/book/vectors.html#dot_product)). Stated formally,
$\vec{a} \cdot \vec{b} = ||\vec{a}||\,||\vec{b}|| \; cos\theta$
![[Pasted image 20260615152824.png]]
^dotprodGeometricdef2

To get $cos\theta$ we to do $adj \over hyp$ if have a unit vector $\hat{b}$ then we know that 

$hyp = 1$

And to get the $adj$ length we just need to get the project length of $\hat{b}$ which is:

$\hat{a} \cdot \hat{b} = adj$

so then the equation turns to be :

$cos\theta = {\hat{a} \cdot \hat{b} \over 1} = \hat{a} \cdot \hat{b}$
![[Pasted image 20260615160433.png]]

this means that if vectors are placed on the same plane (where each of their **tails** start) then the angle can be measured between the two when applying the **2nd geometric definition**.
![[Pasted image 20260615161248.png]]
this is however not the case if the vectors are parallel from each other, which denotes that they are on different planes thus the angle cannot be calculated:
![[Pasted image 20260615161152.png]]

So then to find the angle if the two vectors lie on the same plane we can apply this equation:

$\Large{\theta = cos^{-1}({\vec{a} \cdot \vec{b} \over ||\vec{a}||||\vec{b}||})}$

which if both vectors are unit vectors then it can be simplified to:

$\Large{\theta = cos^{-1}({\hat{a} \cdot \hat{b}})}$


