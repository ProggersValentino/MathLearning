[khan acad](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-representing-systems-with-matrices/a/representing-systems-with-matrices)


You can use matrices to represent **system of equations** within them which is called an **augmented matrix** which is used to both **solve** and **represent equations** in a short hand way
![[Pasted image 20260519115917.png]]

A more complex situation is if we have equations like this:
![[Pasted image 20260519120847.png | 500]]
**How do we effectively turn those in to a uniform matrix?**

First, lets rewrite the equations to look like this:
![[Pasted image 20260519121004.png| 500]]

this is a lot more digestible to work with which now our matrix will be:
![[Pasted image 20260519121042.png]]

Each column corresponds with each variables (x, y, z) and constants

**NOTE**: be sure before converting a system to a augmented matrix that all variables are in order **FOR EACH EQUATION** AND constant terms are **isolated** on one side.

for instance:
![[Pasted image 20260519122023.png]]

## Representing through Inverses
[khan acad vid p1](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-solving-equations-with-inverse-matrices/v/matrix-equations-systems)

##### Linear System matrix equations

Say we have:

$\begin{aligned} 2s - 5t = 7 \\[1em] -2s + 4t = -6 \end{aligned}$

we can substitute the linear system into a matrix equation where:

$\begin{aligned} \begin{bmatrix} 2 & 5 \\ -2 & 4 \end{bmatrix} \cdot \begin{bmatrix} s \\ t \end{bmatrix} = \begin{bmatrix} 7 \\ -6 \end{bmatrix} \\[1em] A \; \cdot \;  \overrightarrow{x}\; = \; \overrightarrow{b} \end{aligned}$

and if we follow through on the [matrix multiplication](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FMatrix%20Multiplication) then we will get the linear system we originally started with.

##### Solving with inverses

to solve $A \; \cdot \;  \overrightarrow{x}\; = \; \overrightarrow{b}$  we'll need to **first nullify** the $A$ matrix and to do that we'll need to multiply it by its inverse as ![[Algebra/Matrices/Inverse Matrices#^inverseToIdentity]]
so because of this we know we need to multiply $A$ by $A^{-1}$ which becomes:

$A^{-1} \cdot A \; \cdot \;  \overrightarrow{x}\; = \; A^{-1} \cdot \overrightarrow{b}$

which will give:
$I \; \cdot \;  \overrightarrow{x}\; = \; A^{-1} \overrightarrow{b}$

So now we need to find the **inverse** of $A$ which is done by:
![[Inverse Matrices#^gettingInverse2x2]]

then if we use the inverse and multiply it against $\begin{bmatrix} 7 \\ -6 \end{bmatrix}$
we'll get the answer.
![[Pasted image 20260608122941.png]]