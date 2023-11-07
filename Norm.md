###### Normed Linear Spaces ######
## Norm ##

**Definition**: Let $(V,F)$ be a vector space. A [[norm]] on $V$ is a function  

$\| \cdot \| : V  \rightarrow \mathbb{R} \geq 0$

such that for all $x,y \in V$ and $c \in F$ the following axioms hold:

- (P1) $\|x\| \geq 0$ and $\|x\| = 0$ iff $x=0_v$ (positive definiteness)  
- (P2) $\|cx\| = |c| \|x\|$  $\space \space \space\forall c \in \mathbb{R}$ (homogeneity)  
- (P3) $\|x+y\| \leq \|x\| + \|y\|$ (triangle inequality)

The triplet $(V,F,\| \cdot \|)$ is called a [[normed linear space]].


> **Remark**: Perhaps the most important property of a norm is that it induces a metric on the vector space. Hence we can quantify the [[distance]] between two vectors in a vector space. Namely, the distance between two vectors $x$ and $y$ $\in V$ is the norm of the vector $x-y$ or $y-x$ $: \|(y-x)\|$. Since the norm is always positive, the distance is also positive. The distance between two vectors is zero iff the vectors are the same. $x=x-0$, the norm of $x$ is the distance of $x$ to the origin. With a proper distance definition (norm), one can begin studying the geometry of the space.

> **Remark**: We can define a "sphere" in $V$ using the norm concept. The sphere is the set of all vectors in $V$ with a fixed norm. For example, in $\mathbb{R}^2$, the sphere with radius $r$ is the set of all vectors with norm $r$.

$S = {v \in V | \|v-v_0\| \leq r}$

------------------------------------------------------------------------------------------
<ins>Example</ins>: Let $V = \mathbb{R}^2$, $F = R$, and let $x =$ $\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$ 

i. $\|x\|_1 := |\alpha_1|+|\alpha_2|$,  is $\|x\|_1$ a norm?  

- (P1) Let $x = \begin{bmatrix} c_1 \\ c_2 \end{bmatrix}$,  
    * then $\|x\|_1 = |c_1|+|c_2| \geq 0$ and $\|x\|_1 = 0$ iff $c_1 = c_2 = 0$ (forwards direction)  
    * $\|x\|_1 = 0$ iff $c_1 = c_2 = 0$ implies $\|x\|_1 = |c_1|+|c_2| \geq 0$ (backwards direction)

   
- (P2) Let $c \in \mathbb{R}$, then $\|cx\|_1 = |c_1c|+|c_2c| = |c|(|c_1|+|c_2|) = |c|\|x\|_1$  

- (P3) Let $y = \begin{bmatrix} y_1 \\ y_2 \end{bmatrix}$,  
    then $\|x+y\|_1 = |x_1+y_1|+|x_2+y_2| \leq |x_1|+|y_1|+|x_2|+|y_2| = \|x\|_1 + \|y\|_1$  
         

ii. $\|x\|_2 := \sqrt{x_1^2+x_2^2}$,  is $\|x\|_2$ a norm?  
- (P1) $\|x\|_2 = \sqrt{x_1^2+x_2^2} \geq 0$ and $\|x\|_2 = 0$ iff $x_1 = x_2 = 0$ (forwards direction) 
    $\|x\|_2 = 0$ iff $x_1 = x_2 = 0$ implies $\|x\|_2 = \sqrt{x_1^2+x_2^2} \geq 0$ (backwards direction)   
- (P2) Let $c \in \mathbb{R}$, then $\|cx\|_2 = \sqrt{(cx_1)^2+(cx_2)^2} = |c|\sqrt{x_1^2+x_2^2} = |c|\|x\|_2$  
- (P3) Let $y = \begin{bmatrix} y_1 \\ y_2 \end{bmatrix}$,  
    then $\|x+y\|_2 = \sqrt{(x_1+y_1)^2+(x_2+y_2)^2} \leq \sqrt{x_1^2+y_1^2}+\sqrt{x_2^2+y_2^2} = \|x\|_2 + \|y\|_2$  

iii.

All these norms can be generalized into what is called the $p$-norm.  
$$\|x\|_p = \left( \sum_{i=1}^n |x_i|^p \right)^{1/p}$$
where $p \geq 1$ and $x = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$

> **Remark**: Note that $lim_{p \rightarrow \infty} \|x\|_p = \|x\|_{\infty} = max_i |x_i|$  

Geometric visualization of the $p$-norms in $\mathbb{R}^2$ is given below. 
 
<p align="center">
  <img rotate ="90" 
  style="filter: invert(88%);"
  src="Lecture Notes/figures/vector-p-norms.svg" />
</p>

<ins>Example</ins>: Let $\|x\|_{\frac{1}{2}} = ({|\alpha_1|^{1/2}+|\alpha_2|^{1/2})}^2$ where, $x=\begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix}$ is $\|x\|_{\frac{1}{2}}$ a norm ?  
- Show a counter example for (P3),  
    Let $x = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$ and $y = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$  
    then $\|x+y\|_{\frac{1}{2}} = ({|1|^{1/2}+|1|^{1/2})}^2 = 4$  
    but $\|x\|_{\frac{1}{2}} + \|y\|_{\frac{1}{2}} = ({|1|^{1/2}+|0|^{1/2})}^2 + ({|0|^{1/2}+|1|^{1/2})}^2 = 2$  
    hence $\|x+y\|_{\frac{1}{2}} \nleq \|x\|_{\frac{1}{2}} + \|y\|_{\frac{1}{2}}$  

------------------------------------------------------------------------------------------
<ins>Example</ins>: Norms on function spaces. $V:\{f(.) | f[0,1] \rightarrow \mathbb{R} \textrm{ s.t. }  \int_0^1 f(t)^p dt < \infty , 1 \leq p < \infty \}$  

- $\| f \|_p= (\int_0^1|f(t)|^pdt)^{\frac{1}{p}}$ (p-norm)  
- $\| f \|_{\infty} = max_{t \in [0,1]} |f(t)|$ (infinity-norm)


## Matrix Norms ##

**Definition**: Let $A \in \mathbb{R}^{m \times n}$ be a matrix. A [[matrix norm]] is a function that maps matrices to non-negative real numbers. A matrix norm must satisfy the norm axioms. A norm on matrices can be defined as,

$$\|A\| = \max_{ij}|a_{ij}|$$

where $a_{ij}$ is the element of $A$ at the $i$ th row and $j$ th column.

------------------------------------------------------------------------------------------
<ins>**Example**</ins>: Let $V = \mathbb{R}^{n \times m}$ and $A = [a_{ij}]$

$$\|A\|_1 = \max_{1 \leq j \leq m} \sum_{i=1}^n |a_{ij}|  \  \ \text{(absolute sum of rows)}$$

Another norm definition is _Frobenuis norm_:

$$\|A\|_F = (\sum_{i=1}^n \sum_{j=1}^m |a_{ij}|^p)^{\frac{1}{p}}$$
    
$$\text{where } 1 \leq p \leq \infty$$ 

## Induced Norm ##
**Definition**: $A: \mathbb{R}^n \rightarrow \mathbb{R}^m$ be an $m \times n$ matrix. Let $\| \cdot \|_{\mathbb{R}^n}$ be a norm on $\mathbb{R}^n$ and $\| \cdot \|_{\mathbb{R}^m}$ be a norm on $\mathbb{R}^m$. The norm of $A$ induced by these norms is defined as,

$$\|A\| := \max_{x \in \mathbb{R}^n} \frac{\|Ax\|_{\mathbb{R}^m}}{\|x\|_{\mathbb{R}^n}}$$

> **Remark**: The induced [[matrix]] norm is defined in terms of vector norms. An equivalent definition is given below:

$$\|A\| := \max_{\|x\|_{\mathbb{R}^n} = 1} \|Ax\|_{\mathbb{R}^m}$$

> **Remark**: The induced norm of a matrix is the maximum amplification of the norm of a vector under the action of the matrix. In other words, the induced norm of a matrix is the maximum amount by which the matrix can stretch a vector.

A nice visualization of the induced norm is given below.

<p align="center">
  <img rotate ="90" 
  style="filter: invert(88.4%);"
  src="Lecture Notes/figures/induced-norm.png"
/>

------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]