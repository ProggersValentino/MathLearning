[khan acad](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-elementary-matrix-row-operations/a/matrix-row-operations), [[Algebra/Matrices/Drawings/matrix row operations]], [khan acad vid](https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/matrices-elimination/v/matrices-reduced-row-echelon-form-1)

Within matrices there are **three elementary matrix row operations** which include:

| Row Operation                            | Symbol             | Example                              |
| ---------------------------------------- | ------------------ | ------------------------------------ |
| Switch any <br>two rows                  | $R_1 <-> R_2$      | ![[Pasted image 20260603172917.png]] |
| Multiply a row by a nonzero <br>constant | $xR_1$             | ![[Pasted image 20260603173028.png]] |
| Add one row to another                   | $R_1 + R_2 -> R_2$ | ![[Pasted image 20260603173152.png]] |
^rowOperationTable

### Row switching 
**Example:** Perform the row operation *R_1 <--> R_2* on the following matrix.
![[Pasted image 20260519155519.png | 300]]

**solution**
given the symbol *<-->* means to interchange and we want to apply it to rows 1 and 2, the new matrix will be:
![[Pasted image 20260519155641.png | 300]]

which the overall solution is represented:
![[Pasted image 20260519160014.png]]

showing that the symbol ![[Pasted image 20260519160035.png | center | 100 ]] indicates that row 1 and 2 interchanged positions

### Multiply a row by a nonzero constant
**Example:**
Perform the row operation 3R_2 --> R_2 on the following matrix.
![[Pasted image 20260519160828.png | 300]]

**solution**
Given the symbol *3R_2 --> R_2* indicates that the second row should be multiplied at a constant of **3** to which then the matrix becomes:
![[Pasted image 20260519161616.png | 700]]

making the final outcome be:
![[Pasted image 20260519161701.png | 300]]

### Add one row to another

**Example:**
Perform the row operation *R_1+R_2 --> R_2* on the following matrix.
![[Pasted image 20260519162104.png | 300]]

**Solution**
Given the notation *R1 + R2 --> R2* indicates that we need to add row 1 and 2 together which then the result will replace row 2 which means:
![[Pasted image 20260519162442.png]]

which then the result of the matrix will be: 
![[Pasted image 20260519162518.png | 300]]

which as stated before the result of adding rows 1 and 2 replace row 2

### Systems of equations and matrix row operations
[khan acad](https://www.khanacademy.org/math/algebra-home/alg-matrices/alg-row-echelon-and-gaussian-elimination/v/matrices-reduced-row-echelon-form-2)
going back to [augmented matrices](obsidian://open?vault=MathLearning&file=Algebra%2FMatrices%2FLinear%20Systems%20%2B%20Matrices) where each row represents a set equation in order of variables (x, y, z) are first followed by the constants
![[Pasted image 20260519174551.png]]

We can use any of the row operations to make a new augmented matrix from the given one created from the linear equations 

#### Augmented Matrices switch rows
![[Pasted image 20260519175459.png]]
We can do this because it doesn't matter what order the equations are in 

#### Augmented Matrices Multiplication by constant
![[Pasted image 20260519180222.png]]

We can multiply both sides of an equation by the **same nonzero constant** to obtain a new equation

When we are solving for systems of equations, its an often practice to eliminate a variable. This is because the two equations are equivalent as well as the two systems are also equivalent

#### Augmented Matrices add a row to another
It is known we can **add two equal quantities to both sides** of an equation to obtain an equivalent equation as for instance: 

***A = B & C = D***
therefore,
***A + C = B + D***

this is commonly done to solve any systems of equations like say if we take: 

***-2x - 6y = -10***
***2x - 5y = 6***

adding them together we would get the result:
***-y = -4***

so when applying addition to either equation you create an equivalent system of equations:
![[Pasted image 20260519182156.png]]

so now if we apply all the operations we can solve the x and y of the current system:
***2y + 6x = 16***
***6y + 11x = 32***

**solution:**
![[Pasted image 20260520141800.png | 500]]