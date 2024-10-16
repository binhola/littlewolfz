---
title: Linear Algebra
tags:
  - maths
---

> *A mathematician, like a painter or poet, is a maker of patterns. If his patterns are more permanent than theirs, it is because they are made with ideas* - Godfrey Hardy 
## Vector 

Vectors are defined by *length* and *direction*.
### Addition and scalar multiplication

Define a vector in 2D Cartesian coordinate space.
$$
\mathbf{a} = \begin{pmatrix} a_1 \\ a_2 \end{pmatrix} = a_1\begin{pmatrix} 1 \\0 \end{pmatrix} + a_2\begin{pmatrix} 0 \\1 \end{pmatrix} = a_1 \mathbf{i} + a_2 \mathbf{j}
$$
$i$ and $j$ are *unit coordinate vectors*.
]
- Any vector can be written as *linear combination of unit coordinate vectors*
- In other words, in this case, two unit coordinate vectors *span* the 2D space 

#### Laws of vector addition and scalar multiplication
- $\mathbf{a} + \mathbf{b} = \mathbf{b} + \mathbf{a}$ (commutative)
- $\mathbf{a} + (\mathbf{b} + \mathbf{c}) = (\mathbf{a} + \mathbf{b}) + \mathbf{c}$ (associative)
- $\mathbf{a} + 0 = \mathbf{a}$ (identity)
- $\mathbf{a} + (\mathbf{-a}) = 0$ (inverse)
- $\alpha(\mathbf{a} + \mathbf{b}) = \alpha \mathbf{a} + \alpha \mathbf{b}$ (distributive)
- $(\alpha + \beta) \mathbf{a} = \alpha \mathbf{a} + \beta \mathbf{b}$ distributive
- $\alpha(\beta \mathbf{a}) = (\alpha \beta) \mathbf{a}$ (associative)
- $1 \mathbf{a} = \mathbf{a}$ (identity)

## Dot product

#### Definition
$\mathbf{a}$, $\mathbf{b} \in$ 3D space : $\mathbf{a} = (a_1, \, a_2, \, a_3)^\top$ and $\mathbf{b} = (b_1, \, b_2, \, b_3)^\top$. Dot product between them is defined as
$$
\mathbf{a} \cdot \mathbf{b} = a_1 b_1 + a_2 b_2 + a_3 b_3
$$

#### Length
Consider a special case when $\mathbf{b} = \mathbf{a}$, we have 
$$\mathbf{a} \cdot \mathbf{a} = a_1^2 + a_2^2 + a_3^2$$
which is the square of length of $\mathbf{a}$. So the dot product gives the length of a vector, defined by
$$
||\mathbf{a}|| = \sqrt{\mathbf{a} \cdot \mathbf{a}}
$$
#### Geometric interpretation
$$
\mathbf{a} \cdot \mathbf{b} = ||\mathbf{a}|| \, || \mathbf{b} || \cos(\mathbf{a},\mathbf{b}) = ||\mathbf{a}|| \, || \mathbf{b} || \cos(\theta)
$$
Proof: use the law of cosine

When $\theta = \pi/2 \Leftrightarrow \mathbf{a} \cdot \mathbf{b} = 0$, two vectors are orthogonal to each other if their dot product is 0. For example, in case of unit vectors $\mathbf{i}$, $\mathbf{j}$, $\mathbf{k}$ : $\mathbf{i} \cdot \mathbf{j} = \mathbf{i} \cdot \mathbf{k} = \mathbf{j} \cdot \mathbf{k} = 0$. 

Normalizing a vector:
$$
\mathbf{\hat v} = \dfrac{\mathbf{v}}{|| \mathbf{v} ||}
$$
This is a unit vector with length 1.

#### Laws of dot product
- $\mathbf{a} \cdot \mathbf{b} = \mathbf{b} \cdot \mathbf{a}$
- $\mathbf{a} \cdot (\mathbf{b} + \mathbf{c}) = \mathbf{a} \cdot \mathbf{b} + \mathbf{a} \cdot \mathbf{c}$
- $(\alpha \mathbf{a}) \cdot \mathbf{b} = \alpha (\mathbf{a} \cdot \mathbf{b})= \mathbf{a} \cdot (\alpha\mathbf{b})$
- $\mathbf{a} \cdot \mathbf{a} \geq 0$ 
#### Triangle inequality

$$|| \mathbf{a} + \mathbf{b}|| \leq ||\mathbf{a}|| + ||\mathbf{b}||$$

Proof: use Cauchy-Schwarz inequality 
### Line and plane 

We can define equations of lines in 2D by using normal vector $\mathbf{n} = (a,b)$ and a point $P_0(x_0, y_0)$. Consider an arbitrary $P(x, y)$ and the fact that $PP_0$ perpendicular to $\mathbf{n}$, the equation of line can be written as:
$$
\mathbf{n} \cdot \vec{PP_0} = 0
$$
Or
$$
\begin{aligned}
&a(x-x_0) + b(y-y_0) = 0 \\
\Leftrightarrow \quad & y = -\dfrac{a}{b}x + \dfrac{by_0+ax_0}{b} \\
\end{aligned}
$$
Similar to the case of plane

### Projections

Denote $\mathbf{p}$ as the projection of $\mathbf{v}$ on $\mathbf{u}$ 
![[Pasted image 20241006131951.png]]

We have 
$$
\mathbf{p}=OB \dfrac{\mathbf{u}}{||\mathbf{u}||} = ||\mathbf{v}||\cos \theta \dfrac{\mathbf{u}}{||\mathbf{u}||} = ||\mathbf{v}|| \dfrac{\mathbf{u}\cdot \mathbf{v}}{||\mathbf{u} || \, || \mathbf{v} ||} \dfrac{\mathbf{u}}{||\mathbf{u}||} = \left( \dfrac{\mathbf{u}\cdot \mathbf{v}}{\mathbf{u} \cdot \mathbf{u}} \right) \mathbf{u}
$$
Length of projection

$$
||\mathbf{p}|| = \dfrac{|\mathbf{u}\cdot \mathbf{v}|}{||\mathbf{u}||}
$$
*Find a distance from a point to a 2D line*
![[Pasted image 20241006134152.png]]

Line: $ax + by = c$ 
$$
d = \dfrac{ax_0 + by_0 - c}{\sqrt{a^2+b^2}}
$$

## Cross product 

![[Pasted image 20241006135844.png]]

Cross product appears naturally in rotational motion.
Work done by a force $\vec{F} = (F_x, F_y)$

$$
\Delta W = F_x \Delta x + F_y \Delta y = F_x (-r \Delta \theta \sin \theta) + F_y (r \Delta \theta \cos \theta) = (F_y x - F_x y) \Delta \theta
$$
Generalizing for 3D, $\mathbf{r} = (x,y,z)$ and $\mathbf{F} = (F_x, F_y, F_z)$ 
$$
 \mathbf{r} \times \mathbf{F} = 
\begin{pmatrix} 
F_z y - F_y z \\ 
F_x z - F_z x \\
F_y x - F_x y
\end{pmatrix} 
$$

From definition:
$$
\mathbf{a} \times \mathbf{b} = -\mathbf{b} \times \mathbf{a}
$$
$$
|| \mathbf{a} \times \mathbf{b} ||^2 = || \mathbf{a} || \, || \mathbf{b} || \sin(\mathbf{a} , \mathbf{b})
$$
### Geometric interpretation
Cross product tell us when two vector are parallel with each other.

The area of the triangle formed by two vectors is
$$
A = \dfrac{1}{2} \det 
\begin{pmatrix} 
1 & 1 & 1 \\
a_1 & a_2 & a_3 \\
b_1 & b_2 & b_3 \\
\end{pmatrix}
$$
![[Pasted image 20241006142022.png]]

### Rules of cross products
$$
\begin{aligned}
    \mathbf{a} \times \mathbf{b} &= -\mathbf{b} \times \mathbf{a} \\
    \mathbf{a} \times \mathbf{a} &= 0 \\
    (\alpha \mathbf{a}) \times \mathbf{b} &= \alpha (\mathbf{a} \times \mathbf{b}) = \mathbf{a} \times (\alpha \mathbf{b}) \\
    \mathbf{a} \times (\mathbf{b} + \mathbf{c}) &= \mathbf{a} \times \mathbf{b} + \mathbf{a} \times \mathbf{c} \\
    (\mathbf{a} + \mathbf{b}) \times \mathbf{c} &= \mathbf{a} \times \mathbf{c} + \mathbf{b} \times \mathbf{c} \\
    \mathbf{a} \times (\mathbf{b} \times \mathbf{c}) &= \mathbf{b} (\mathbf{a} \cdot \mathbf{c}) - \mathbf{c} (\mathbf{a} \cdot \mathbf{b}) \\
    (\mathbf{a} \times \mathbf{b})^2 &= a^2 b^2 - (\mathbf{a} \cdot \mathbf{b})^2 \\
    \mathbf{c} \cdot (\mathbf{a} \times \mathbf{b}) &= (\mathbf{c} \times \mathbf{a}) \cdot \mathbf{b}
\end{aligned}
$$
## Matrix

### System of linear equations
Matrix comes from system of linear equations

$$
\begin{aligned}
2x - y &= 1 \\
x+ y  &= 5
\end{aligned}
$$
can be written as
$$
\begin{pmatrix} 
2 & -1 \\
1 & 1 
\end{pmatrix}
\begin{pmatrix} 
x \\ y
\end{pmatrix}
=
\begin{pmatrix} 
1 \\ 5
\end{pmatrix}
$$
or 
$$
\mathbf{A} \mathbf{x} = \mathbf{b}
$$

![[Pasted image 20241006143327.png]]

**Solutions:**
- 1 unique solution
- No solution
- Many solutions

**Elementary row operations**:
- Row swap
- Scalar multiplication
- Row sum

### Gauss-Jordan elimination method
$$
\begin{aligned}
    2x_1 + 4x_2 - 2x_3 &= 2 \\
    4x_1 + 9x_2 - 3x_3 &= 8 \\
    -2x_1 - 3x_2 + 7x_3 &= 10
\end{aligned}
$$
which can be rewritten as
$$
\mathbf{A} \mathbf{x} = \mathbf{b}, \quad
\mathbf{A} = \begin{bmatrix}
2 & 4 & -2 \\
4 & 9 & -3 \\
-2 & -3 & 7
\end{bmatrix}, \quad
\mathbf{x} = \begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix}, \quad
\mathbf{b} = \begin{bmatrix}
2 \\
8 \\
10
\end{bmatrix}
$$
After row echelon form (REF):
$$
\mathbf{U} = \begin{bmatrix}
2 & 4 & -2 \\
0 & 1 & 1 \\
0 & 0 & 4
\end{bmatrix}, \quad \mathbf{c} = \begin{bmatrix}
2 \\
4 \\
8
\end{bmatrix}
$$
$\mathbf{U}$ is an upper triangular matrix. Solving $\mathbf{U}\mathbf{x} = \mathbf{c}$ by back substitution.

Jordan continue to eliminate until left block becomes unit block. Process is so-called reduced row echelon form (RREF):
$$
\begin{bmatrix} 2 & 4 & -2 & | & 2 \\ 4 & 9 & -3 & | & 8 \\ -2 & 3 & 7 & | & 10 \end{bmatrix} \rightarrow \begin{bmatrix} 2 & 4 & -2 & | & 2 \\ 0 & 1 & 1 & | & 4 \\ 0 & 0 & 4 & | & 8 \end{bmatrix} \rightarrow \begin{bmatrix} 1 & 0 & 0 & | & -1 \\ 0 & 1 & 0 & | & 2 \\ 0 & 0 & 1 & | & 2 \end{bmatrix}
$$
### Underdetermined systems
More unknowns than equations $\rightarrow$ matrix has more columns than rows
$$ \begin{bmatrix} 1 & -1 & -1 & 2 & | & 1 \\ 2 & -2 & -1 & 3 & | & 3 \\ -1 & 1 & -1 & 0 & | & -3 \end{bmatrix} \rightarrow \begin{bmatrix} {1} & -1 & 0 & 1 & | & 2 \\ 0 & 0 & 1 & -1 & | & 1 \\ 0 & 0 & 0 & 0 & | & 0 \end{bmatrix} $$
We have 4 unknowns but only 2 equations, so there are 2 pivots (pivot columns) and $4-2 =2$ free variables (non-pivot columns). Non-pivot columns can be written as the linear combination of pivot columns.

***Linear combination**: If $u_1​,…,u_m​$ are m vectors in $R^n$ and $\alpha_1​,…,\alpha_m​$ are m real numbers. Then, vector$$
*\alpha_1 u_1 + \alpha_2 u_2 + \cdots + \alpha_m u_m
$$is called linear combination of  $u_1​,…,u_m​$ and $\alpha_1​,…,\alpha_m​$ are the coefficients of the combination.

Select the variables associated with the non-pivot columns as the free variables, and compute other variables, called the pivot variables, in terms of the free ones:
$$
\begin{aligned} \begin{cases} x_1 + x_2 + x_4 = 2 \\ x_3 - x_4 = 1 \end{cases} \Rightarrow \begin{cases} x_1 = 2 + s - t \\ x_3 = 1 + t \end{cases} \Rightarrow \mathbf{x} = \begin{bmatrix} 2 + s - t \\ s \\ 1 + t \\ t \end{bmatrix} = \begin{bmatrix} 2 \\ 0 \\ 1 \\ 0 \end{bmatrix} + s \begin{bmatrix} 1 \\ 1 \\ 0 \\ 0 \end{bmatrix} + t \begin{bmatrix} -1 \\ 0 \\ 1 \\ 1 \end{bmatrix} \end{aligned}
$$
### Rank 
The rank of a matrix is the number of nonzero rows in its row echelon form (or its reduced REF). It is also the number of pivots.

Let $\mathbf{A}$ be the coefficient matrix of a system of linear equations with $n$ variables. If the system is solvable (or consistent), then
$$\text{number of free variables} =  n - {\rm rank} (\mathbf{A})
$$
## Homogeneous linear systems
Matrix **A** is of shape $m\times n$ 
$$
\mathbf{A} \mathbf{x} = 0
$$
1. *Why this equation called a homogenous system?* 
2. *What are the solutions?*

Ans: 
1. If $x^*$ is a solution, $cx^*$ is also a solution for any $c \in R$ 
2. Trivial solution (zero vector). Or infinite many solutions. Similar to solutions for $5x = 0$ or $0x =0$. *When do we have inifinite many solutions* 

**Remark:** If $[\mathbf{A}|0]$ is a homogeneous system of $m$ linear equations with $n$ unknowns, where $m < n$, then the system has infinitely many solutions.

## Spanning sets of vectors and linear independance

### Span
If $S = {\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k}$ is a set of vectors in $R^n$, then the set of ALL linear combinations of $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k$ is called the span of $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k$, and is denoted by span($\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k$​) or span($S$). If ${\rm span}(S)=R^n$, then $S$ is called a spanning set for $R^n$.

Ex: Show that $R^2 = {\rm span}(\{2, -1\}, \{1, 3\})$ 

Hint: show that this following system always has solutions for all $a$, $b \in R$.  
$$ \begin{aligned} 2x + y &= a \\ -x + 3y &= b \end{aligned} $$
### Linear independence
We have seen that in matrices, it is possible that some columns can be written in terms of others. For example, we can have
$$
\mathbf{a}_3 = -2\mathbf{a}_2 -3  \mathbf{a}_1 \quad \text{or} \quad -\mathbf{a}_3  -2\mathbf{a}_2 -3  \mathbf{a}_1 = 0
$$
In this case, we say that three vectors are *linearly dependent*.

A collection of k vectors $u_1,... u_k$ is *linearly dependent* if 
$$
\alpha_1 u_1 + \alpha_2 u_2 + ... +\alpha_k u_k = 0
$$
holds with at least one $\alpha_k \neq 0$.

Ex: Determine whether the vectors {(1, 2, 0), (1, 1, -1), (1, 4, 2)}

Hint: 
$$
\begin{bmatrix} 1 & 1 & 1 \\ 2 & 1 & 4 \\ 0 & -1 & 2 \end{bmatrix} \begin{bmatrix} \alpha_1 \\ \alpha_2 \\ \alpha_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}
$$

**Remark:** Any set of m vectors in $R^n$ is linearly dependent if *m > n*.

## Matrix Algebra
A $m\times n$ matrix
$$A = \begin{bmatrix} A_{11} & A_{12} & \cdots & A_{1n} \\ A_{21} & A_{22} & \cdots & A_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ A_{m1} & A_{m2} & \cdots & A_{mn} \end{bmatrix} \quad  \text{or} \quad A = \begin{bmatrix} \mathbf{A}_1 & \mathbf{A}_2 & \cdots & \mathbf{A}_n \end{bmatrix}$$
Denote $A_{ij}$ as entry at row $i$ and column $j$.

Identity matrix $I_{ii} = 1$
$$
\mathbf{I} = \mathbf{I}_n := \begin{bmatrix} 1 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & 1 \end{bmatrix} = \begin{bmatrix} e_1 & e_2 & \cdots & e_n \end{bmatrix}
$$
*Why we call it identity matrix?*

Ans: $\mathbf{I}\mathbf{x} = \mathbf{x}$
### Matrix operations
Addition: to add two matrices, add the entries
$$
(\mathbf{A} + \mathbf{B})_{ij} = A_{ij} + B_{ij}
$$
Scalar multiplication
$$
(c\mathbf{A})_{ij} = cA_{ij}
$$
Matrix multiplication
$$
(\mathbf{A}\mathbf{x})_i = \sum_{k=1}^{n}A_{ik}x_{k}
$$
Definition comes from $\mathbf{A}\mathbf{x} =\mathbf{b}$.
Similarly for matrix-matrix multiplication
$$
(\mathbf{A}\mathbf{B})_{ij} = \sum_{k=1}^{n}A_{ik} B_{kj}
$$
![[Pasted image 20241006155822.png]]

#### Laws of matrix operations
$$
\begin{align*} 
&(a): \text{commutative law} & A + B &= B + A \\ 
&(b): \text{distributive law} & \alpha(A+B) &= \alpha A + \alpha B \\ 
&(c): \text{associative law} & A + (B+C) &= (A+B) + C \\ 
&(d): \text{associative law for ABC} & A(BC) &= (AB)C \\ 
&(e): \text{distributive law (left)} & A(B+C) &= AB + AC \\ 
&(f): \text{distributive law (right)} & (A+B)C &= AC + BC \\ 
&(g): \text{broken commutative law (multiplication)} & AB &\neq BA \end{align*}
$$
### Transpose
Considering two (column) vectors $\mathbf{x} = \begin{pmatrix} x \\ y \end{pmatrix}$ and $\mathbf{a} = \begin{pmatrix} a \\ b \end{pmatrix}$ in $\mathbb{R}^2$. Our problem is how to write the dot product $\mathbf{x} \cdot \mathbf{a} = ax + by$ using matrix notation. We cannot use $\mathbf{x} \mathbf{a}$ because matrix multiplication requires that the shapes of the matrices must be compatible. We can solve the problem if we turn the column vector $\mathbf{x}$ into a row vector, then we’re done: 
$$ \mathbf{x} \cdot \mathbf{a} = ax + by = \begin{bmatrix} x & y \end{bmatrix} \begin{bmatrix} a \\ b \end{bmatrix} = \mathbf{x}^\top \mathbf{a} \, (= \mathbf{a}^\top \mathbf{x}) $$
**Definition:** The transpose of an $m\times n$ matrix **A** is the $n\times m$ matrix $\mathbf{A}^\top$ obtained by interchanging the rows and columns of **A**.
$$
A = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \end{bmatrix} \implies A^\top = \begin{bmatrix} 1 & 2 \\ 2 & 4 \\ 3 & 6 \end{bmatrix}
$$
#### Laws of transpose matrix
$$
\begin{align*} &(a): &(\mathbf{A}^{\top})^{\top} &= \mathbf{A} \\ 
&(b): &(\mathbf{A} + \mathbf{B})^{\top} &= \mathbf{A}^{\top} + \mathbf{B}^{\top} \\ &(c): &(k\mathbf{A})^{\top} &= k\mathbf{A}^{\top} \\ 
&(d): &(\mathbf{A}\mathbf{B})^{\top} &= \mathbf{B}^{\top} \mathbf{A}^{\top} \end{align*}
$$
### Inverse 
Inverse matrices are related to inverse functions. Recall that starting with an angle $x$ and pressing the $\sin$ button on a calculator gives us $y = \sin x$. Now, to get back to where we started, i.e., $x$, we press the inverse function $\arcsin$, and we have: $\arcsin y = x$. Now, we have a square matrix $A$, a vector $\mathbf{x}$, and when $A$ acts on $\mathbf{x}$, we get a new vector $\mathbf{b}$. To get back to $\mathbf{x}$, do: $$ A \mathbf{x} = \mathbf{b} \implies \underbrace{A^{-1} A}_{\mathbb{I}} \mathbf{x} = A^{-1} \mathbf{b} \implies A^{-1} \mathbf{b} = \mathbf{x}  $$ The matrix $A^{-1}$ is called the *left inverse matrix* of $A$. There exists the *right inverse matrix* of $A$ as well: it is defined by $AA^{-1} = \mathbb{I}$. If a matrix is invertible, then its inverse, $A^{-1}$, is the matrix that inverts $A$: $$ A^{-1} A = \mathbb{I} \quad \text{and} \quad A A^{-1} = \mathbb{I}  $$
#### Law of inverse
1. If a matrix is invertible, its inverse is unique. 
2. $(AB)^{-1} = B^{-1} A^{-1}$ 
We have $$ (AB)^{-1} (AB) = (B^{-1} A^{-1}) (AB) = B^{-1} (A^{-1} A) B = B^{-1} \mathbb{I} B = B^{-1} B = \mathbb{I} $$Starting with this property for 2 matrices, we can develop the rule for three matrices, $$ (ABC)^{-1} = C^{-1} B^{-1} A^{-1} $$and then for any number of matrices that we want.

#### Finding the inverse matrix
1. Gauss-Jordan elimination method. From $\mathbf{A}\mathbf{A}^{-1} = \mathbf{I}$, we look for the solution of 
$$
\mathbf{A}\mathbf{x}_i = \mathbf{e}_i
$$
where the solution are written as
$$
[\mathbf{A}|\mathbf{I}] = [\mathbf{I}|\mathbf{A}^{-1}]
$$
2. Also the inverse matrix can be written as
$$
\mathbf{A}^{-1} = \dfrac{1}{\det(\mathbf{A})} {\rm adj}(\mathbf{A}) 
$$
adjugate of matrix $\mathbf{A}$ is the transpose of cofactor $\mathbf{C}$




