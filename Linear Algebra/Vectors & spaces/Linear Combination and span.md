[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/linear-combinations/v/linear-combinations-and-span)


Linear Combinations denotes a combination of **scalar multiplication** and **vector addition** to create a new vector which is known as a linear combination.

for instance take:
$\begin{aligned} \vec{a} = \begin{bmatrix} 1 \\ 2 \end{bmatrix} \\[1em] \vec{b} = \begin{bmatrix} 0 \\ 3 \end{bmatrix} \end{aligned}$

if we multiply $\vec{a}$ and $\vec{b}$ by $C$ scalar then we can get any set of numbers within $R^2$ 

$2 \cdot \vec{a} + 1 \cdot \vec{b} = [c_1, c_2]$

![[Pasted image 20260612123631.png]]
so then we can say that the **span** of $\vec{a}$ and $\vec{b}$ can equal of all $R_2$

A **span** confirms whether linear combinations from a set of vectors can represent all real-values within $R^n$ or only a particular set of vectors which is represented:

$Span(\vec{a}, \vec{b}) = R^2$ 

Which that means all linear combinations using $\vec{a}$ and $\vec{b}$ can equal to all real-values within the 2-dimensional space. 

However, not all linear combinations from certain vector pairs can equal to all of $R^n$

for instance,

$\begin{aligned} \vec{c} = \begin{bmatrix} 4 \\ 4 \end{bmatrix} \\[1em] \vec{d} = \begin{bmatrix} -4 \\ -4 \end{bmatrix} \end{aligned}$

![[Pasted image 20260612124318.png]]

if we apply any set of scalars, we'll get a linear combination that is **constrained to the directions** of $\vec{c}$ and $\vec{d}$ :

$2 \cdot \vec{c} + {1 \over 4} \cdot \vec{d} = [7,7]$

which then we are unable to get to $\vec{f}$

So then the **span** of $\vec{c}$ and $\vec{d}$ cannot produce all real-values within $R^2$ but rather $[2, 2]$

$Span(\vec{c}, \vec{d}) = [2, 2]$

