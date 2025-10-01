---
title: Principle Component Analysis
tags:
  - maths
  - PCA
---
## Statistics

##### Consider $X$ as a random variable of $N$ entries

Mean of $X$ 

$$
\bar x = \dfrac{1}{N} \sum_{i=0}^N x_i
$$
Variance of $X$

$$
V_X = \sigma_x^2 = \sqrt{\dfrac{1}{N-1} \sum_i (x_i - \bar x)^2}
$$
Centering

$$
X_i^c = x_i - \bar x \implies \bar x^c = 0
$$

Reduction

$$
x_i^r = \dfrac{x_i}{\sigma_x} \implies \sigma_{x}^r = 1
$$
Standardization
$$
x_i^s = \dfrac{x_i - \bar x}{\sigma_x}
$$

##### Consider 2 random variables $X$ and $Y$
Covariance 

$$
\sigma_{xy} = \dfrac{1}{n-1} \sum_i (x_i - \bar x)(y_i - \bar y)
$$
high covariance $\implies \sigma$ large 

Linear correlation coefficient
$$
P_{xy} = \dfrac{\sigma_{xy}}{\sigma_x \sigma_y} \quad {\rm where} \quad P_{xy} \in [-1, 1]
$$

##### Consider m random variables
Data can be put into a matrix $X$ of $n$ rows and $m$ columns

Standardization
$$
X_j^c = (X_j - \bar X_j)/\sigma_{X_j} \implies \sum_j{X_j}^c =0
$$
Correlation 
$$
V = \dfrac{X^tX}{n-1}
$$
where 
- $V_{jj} = 1$
- $V_{jk} = \dfrac{\sigma_{jk}}{\sigma_j \sigma_k} = P_{jk}$
## PCA 
### Information
- high information means precise knowledge of position
- positive
- addictive
- simple and easy to handle
Knowing that large $\sigma$ corresponding to larger information 
We can define $I_{x_j} = V_{x_j}$

Percentage of information

$$
\dfrac{I_{x_j}}{X_{tot}} \times 100 
$$
Find the principal matrix 
Projection of $\vec{x_i}$ on unit vector $\vec{e}$ can be written as 
$$
p_i = \vec{x}_i \cdot \vec{e} = \vec{x}_i^t \vec{e} 
$$
where
- $||\vec{e}|| = 1 \implies \sum_j e_j^2 = 1$
- $e^t e =1$
Thus,
$$
P = Xe
$$
Information holds by $P$
$$
I_p = \dfrac{1}{n-1} \sum_i p_i^2 = \dfrac{P^tP}{n-1}
$$
Therefore,
$$
I_p = \dfrac{e^t X^t X e}{n-1} = e^t \dfrac{X^tX}{n-1} e = e^t Ve
$$
We want $e$ such that the information held by $P$ is extremum

With a constraint, we introduce the Lagrange multiplier for $k$ constraint $C_k(x_1, x_2, ...) = 0$
$$
\dfrac{\partial (f(x_1, x_2, ...) - \sum_k \lambda_k C_k(x_1, x_2, ...))}{\partial x} = 0
$$
In our case 
$$
C(e_1, e_2, ...) = e^te - 1 = 0
$$
Therefore,
$$
\dfrac{\partial I_p(e) - \lambda(e^te-1)}{\partial e} = 0
$$
If $A$ square and $x$ column, so that $\dfrac{\partial x^t A x}{\partial x}=2Ax$. Then,
$$
\dfrac{\partial e^t V e - \lambda(e^te-1)}{\partial e} = 2Ve - 2I\lambda e= 0
$$
Thus,
$$Ve = \lambda e = I_p e$$
Because,
$$
e^tVe = e^t\lambda e = e^t e \lambda = \lambda = I_p
$$
#### Diagonalization
$$V  = E D E^{-1}$$
$V$ is real, symmetric, square matrix and $E^{t}E = 1$. So, $E^{-1} = E^t$ 

### Compression
We want compressed $P' = X E'$ so that $X = P'E'^{t}$ (decompression)

### Visualization
Representing the PCA in normed space, take the normed by dividing all column by $\dfrac{1}{\sqrt{\lambda_j}}$
$$
P = XED^{-1/2}
$$
Unit vector
$$A = ED^{1/2}$$
## CA

Hands $n_{i+}$ and feet $n_{+j}$ . Total $n_{++}$
Create a $U$ matrix with $X_0$ hypothesis that there is no correlation, where the entries are
$$
u_{ij} = \dfrac{n_{i+} n_{+j}}{n_{++}} 
$$
Compare to $n_{ij}$
$$
\chi_{ij}^2 = \left( \dfrac{u_{ij} - n_{ij}}{\sqrt{ij}} \right)^2
$$
By definition, $|u_{ij} - n_{ij}| = \sigma$ on average, so $\chi_{ij}^2 = 1$ if there is no correlation
Total correlation in column
$$
\chi_j^2 = \dfrac{1}{n-1} \sum_i \left( \dfrac{u_{ij} - n_{ij}}{\sqrt{u_{ij}}}\right)^2
$$
We want to project the data on axes such that $\chi^2$ is maximized

With an matrix $X$ such that $x_{ij} = \dfrac{u_{ij} - n_{ij}}{\sqrt{u_{ij}}}$ 
Information $I = \dfrac{1}{n-1} \sum_i x_{ij}^2$ 
### Statistical fluctuation
If $n \gtrsim 30$ is the expected number then the distribution of the seen $n_{seen}$ is a Gaussian $G(n, \sqrt{n})$ 

$$\alpha = \dfrac{|n_{seen} - n_{exp}|}{\sqrt{n}}$$
On average $\alpha = 1$
## LDA 
Define the best axis to separate group

$$
I_{inter} = \dfrac{n_1}{n} g_1^2 + \dfrac{n_2}{n} g_2^2
$$
$$
I_{intra} = \dfrac{n_1}{n} \sigma_1^2 + \dfrac{n_2}{n} \sigma_2^2
$$
$$I = I_{inter} + I_{intra}$$
Discriminating power
$$
\lambda = \dfrac{I_{inter}}{I_{intra}} \in [0,1]
$$


