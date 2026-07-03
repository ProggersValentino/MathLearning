[khan acad video](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-multiplying-matrices-by-matrices/v/matrix-multiplication-intro), [khan acad lesson](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-multiplying-matrices-by-matrices/a/multiplying-matrices)

multiplication in matricies is very different to [scalar multiplication](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FMatrices%20Basic%20Math%20Operations%20(Addition%2C%20Subtraction%2C%20Scalar%20multiplication)) as to get the product, we must multiply and add a **row x column**. 

## dot product
to better understand matrix multiplication we need to understand **dot product** and n tuples (which is an ordered pair of numbers like (3, 4, 8)).

**Ordered n tuples** are indicated with the arrow over the symbol:  $\overrightarrow{a}$  

which then if we let:
$\overrightarrow{a}  \cdot  \overrightarrow{b} = (11, 7, 9) \cdot (-3, 8, 4)$ 

The dot product can be found between the two n tuples by multiplying the first and second set of coordinates:
![[Pasted image 20260528110456.png]]

To which then we are left with a single number no matter how big the n-tuples are.

## Matrices and n-tuples
Going back to matrices, when multiplying them we can think of each row and column as a n-tuple: 
![[Pasted image 20260528111029.png]]

so then we can denote that row 1 and 2 are: 
$\overrightarrow{r1} = (11, 7)$
$\overrightarrow{r2} = (10, 4)$

and columns 1 and 2 are:
$\overrightarrow{c1} = (11, 10)$
$\overrightarrow{c2} = (7, 4)$


## Matrix Multiplication

So now lets do some multiplication.

Given $A = \begin{bmatrix} 11 & 7 \\ 10 & 4 \end{bmatrix}$ and $B = \begin{bmatrix} -3 & 8 \\ 15 & 7 \end{bmatrix}$ find the new multiplied matrix $C$

![[Pasted image 20260528111911.png]]

As you can see each entry, like for instance $C_{1,2} = (11, 7) \cdot (-3, 15)$, is just an n-tuple which then we just need to find the dot product of them which:
![[Pasted image 20260528112910.png]]

so now when we apply that to the rest of the matrix we get a final matrix of:
![[Pasted image 20260528113306.png]]

## Valid Multiplication
Now that there's an understand of how to multiply, we need to understand when to multiply and what the outcome will be.

for instance take:
![[Pasted image 20260528115159.png]]

looking at it first it logically makes sense that these two matrices fulfil the [closure property of multiplication](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FProperties%20of%20Matrices) meaning they can be multiplied together

However, this equation results in **UNDEFINED** for the overall result because the second matrix doesn't match how we multiply as if we try to multiply these two, when we do **row x column** notice how we'll end up with a n-tuple sizes when trying to find the dot product. 

For instance take row $A_1 = (2, 4, 10)$ and column $B_1 = (9, 1)$ 

when we try to find the dot product, we can do the first two numbers but we end up with an outlier that cant multiply to anything which in our case is the $10$ 

So now it turns out this is an undefined.

To make this equation a valid matrix multiplication we need to change the format of the second matrix to fit the matrix multiplication method which becomes a $3 \times 2$ matrix:
![[Pasted image 20260528120011.png]]

now when multiplying the two we can see that both row and column n-tuples will have a valid number to multiply against and get the **dot product of**.

Now the result of this equation is actually not a $2 \times 3$ or a $3 \times 2$ but rather a $2 \times 2$. this is because we have **2** rows and **2** columns meaning that when finding the dot product we can only do it **2 times** leaving us with an overall product of $2 \times 2$ matrix:
![[Pasted image 20260528121321.png|685]]
![[Pasted image 20260528121720.png]]

A trick to easily determine when and what to multiply matrices is by comparing the two sizes:
![[Pasted image 20260528121934.png]]

The two middle numbers indicate if the two matrices can be multiplied together so if their the same then it can be done:
![[Pasted image 20260528122105.png]]

next to determine what the result will be, the two outside numbers determine what the product of the two matrices will be:
![[Pasted image 20260528122246.png]]

Do note that **order does matter** in matrix multiplication making it non communicative  
## Summary

| Matrix Multiplication | Explaination                                                                                   | Example                              |
| --------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------ |
| How                   | by following the rule of<br>$\overrightarrow{row} \times \overrightarrow{column}$              | ![[Pasted image 20260528122750.png]] |
| When                  | The **column size** in $A$ matches the **row size** in $B$ like:<br>$2 \times 3$  $3 \times 2$ | ![[Pasted image 20260528123212.png]] |
| What                  | Determined by **row size** in $A$ and **column size** in $B$:<br>$2 \times 3$  $3 \times 2$    | ![[Pasted image 20260528123504.png]] |

