[khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/linear-independence/v/more-on-linear-independence)

#### What is Linear dependence
Linear dependence is where a linear combination **can represent** one of the vectors within the set. Therefore, the representation isn't adding anything new to be represented in a different direction but rather is only a scaled representation of another vector

To mathematically solve whether a set of vectors are linearly dependent or not we can apply this rule:

$v_1 = C_2v_2 + C_3v_3 ... C_nv_n = 0 \Rightarrow linearly \; independent$
$v_1 = C_2v_2 + C_3v_3 ... C_nv_n \neq 0 \Rightarrow linearly \; dependent$

This means that when we take the other vectors, scale and add them together to get a vector in the set, **if it equals** $0$ then it is linearly independent

for instance:

$\begin{aligned} \vec{a} = \begin{bmatrix} 2 \\ 1 \end{bmatrix} \\[1em] \vec{b} = \begin{bmatrix} 3 \\ 2 \end{bmatrix} \end{aligned}$

![[Pasted image 20260612140842.png]]

As you can see if we apply both constants can equal $0$ from the vector set.

For a linearly dependent set lets take:

$\begin{aligned} \vec{a} = \begin{bmatrix} 2 \\ 3 \end{bmatrix} \\[1em] \vec{b} = \begin{bmatrix} 4 \\ 6 \end{bmatrix} \end{aligned}$


![[Pasted image 20260612142231.png]]