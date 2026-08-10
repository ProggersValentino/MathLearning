[khan acad video](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-properties-of-matrix-multiplication/v/identity-matrix), [khan acad](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-properties-of-matrix-multiplication/a/intro-to-identity-matrices)

###### What is an Identity Matrix
The $n \times n$ identity matrix which is denoted as $I_n$ is a matrix composed of 1s from the **top left** to **bottom right** and the rest is 0s 
$$\begin{aligned} I_2 = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \\[1em]
I_3 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \\[1em]
I_4 = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix} 
\end{aligned}$$

Furthermore, identity matrices must be $n \times n$  and cannot be $n \times m$ otherwise it is not a true identity matrix

## Multiplication with Identity Matrix 

When multiplying with identity matrices it should follow the [necessary rules](Matrix%20Multiplication) to determine a defined equation

![[Pasted image 20260529104515.png]]![[Pasted image 20260529104522.png]]

As you can see if you multiply a matrix by $I_n$ then it will result in the same matrix. This can be seen a apply the scalar number 1 to the matrix

## Inverses

If we grab the inverse of the matrix and multiply them together, theres a chance we'll end up getting $I_n$ 