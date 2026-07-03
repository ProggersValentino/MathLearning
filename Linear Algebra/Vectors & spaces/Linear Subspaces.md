[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/subspace-basis/v/linear-subspaces)
#### What is a linear subspace
A subset of vectors within $R^n$ where those subset of vectors where it must fulfill three condition properties to be considered within a **linear subspace**. This can also be portrayed as it is a subset of vectors that follow a certain rule or restriction set in place

| Condition Property                  | Meaning                                                                                                 | Example                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Contain Zero Vector                 | Does the subset have a $0$ vector. In other words, if the subset is multiplied by $0$ will it equal $0$ | $\begin{aligned} V = (\vec{v_1}, \vec{v_2}, \vec{v_3}) \\[1em] 0 \cdot (\vec{v_1}, \vec{v_2}, \vec{v_3})) = 0 \end{aligned}$                                                                                                                                                                                                                                                                                                                                              |
| Closure under scalar multiplication | Can the subset be multiplied by **any scalar value** and still follow vector subset rules               | Not a subspace:<br>$U = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} \epsilon R^2 \| x_1 \ge 0$ <br><br>$-1 \cdot \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} -x_1 \\ -x_2 \end{bmatrix}$ <br><br>A subspace:<br>$U = Span(\begin{bmatrix} 1 \\ 1 \end{bmatrix})$<br>$-3 \cdot \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} -3 \\ -3 \end{bmatrix}$<br><br>$5 \cdot \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 5 \\ 5 \end{bmatrix}$<br> |
| Closure under addition              | Can the subset still follow the set rules when adding each vector within the subset                     | $\begin{aligned} V = (\vec{v_1}, \vec{v_2}, \vec{v_3}) \\[1em] C_1v_1 + C_2v_2 + C_3v_3\end{aligned}$                                                                                                                                                                                                                                                                                                                                                                     |
If all the conditions are satisfied then the subset of vectors are **within a linear space**

It can be illustrated in the picture below:
![[Pasted image 20260612175301.png]]

## Basis of a Subspace
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/subspace-basis/v/linear-algebra-basis-of-a-subspace)

A **basis of a subspace** is the minimum set of vectors (its linearly independent) that spans the subspace 

## Proof of subspace basis
[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/null-column-space/v/proof-any-subspace-basis-has-same-number-of-elements)

this invokes the idea that all subspace basis have the **same number of elements** which creates the **dimension**:

$Dim(V) = NO.\; of\; elements \; of \; any\; basis\; of\; V$
h