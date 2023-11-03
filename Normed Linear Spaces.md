## [[Norm]] ##
###### Normed Linear Spaces ######
**Definition**: Let $(V,F)$ be a vector space. A [[norm]] on $V$ is a function  

$\| \cdot \| : V  \rightarrow \mathbb{R} \geq 0$

such that for all $x,y \in V$ and $c \in F$ the following axioms hold:

&emsp;(P1) $\|x\| \geq 0$ and $\|x\| = 0$ iff $x=0_v$ (positive definiteness)  

&emsp;(P2) $\|cx\| = |c| \|x\|$  $\space \space \space\forall c \in \mathbb{R}$ (homogeneity)  

&emsp;(P3) $\|x+y\| \leq \|x\| + \|y\|$ (triangle inequality)

The triplet $(V,F,\| \cdot \|)$ is called a [[normed linear space]].


**Remark**: Perhaps the most important property of a norm is that it induces a metric on the vector space. Hence we can quantify the [[distance]] between two vectors in a vector space. Namely, the distance between two vectors $x$ and $y$ $\in V$ is the norm of the vector $x-y$ or $y-x$ $: \|(y-x)\|$. Since the norm is always positive, the distance is also positive. The distance between two vectors is zero iff the vectors are the same. $x=x-0$, the norm of $x$ is the distance of $x$ to the origin. With a proper distance definition (norm), one can begin studying the geometry of the space.

**Remark**: We can define a "sphere" in $V$ using the norm concept. The sphere is the set of all vectors in $V$ with a fixed norm. For example, in $\mathbb{R}^2$, the sphere with radius $r$ is the set of all vectors with norm $r$.

$S = {v \in V | \|v-v_0\| \leq r}$


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

**Remark**: Note that $lim_{p \rightarrow \infty} \|x\|_p = \|x\|_{\infty} = max_i |x_i|$  
Geometric visualization of the $p$-norms in $\mathbb{R}^2$ is given below. 
 
<p align="center">
  <img rotate ="90" 
  style="filter: invert(88%);"
  src="https://upload.wikimedia.org/wikipedia/commons/6/60/Vector_norms.png?20060103191713" />
</p>

<ins>Example</ins>: Let $\|x\|_{\frac{1}{2}} = ({|\alpha_1|^{1/2}+|\alpha_2|^{1/2})}^2$ where, $x=\begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix}$ is $\|x\|_{\frac{1}{2}}$ a norm ?  
- Show a counter example for (P3),  
    Let $x = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$ and $y = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$  
    then $\|x+y\|_{\frac{1}{2}} = ({|1|^{1/2}+|1|^{1/2})}^2 = 4$  
    but $\|x\|_{\frac{1}{2}} + \|y\|_{\frac{1}{2}} = ({|1|^{1/2}+|0|^{1/2})}^2 + ({|0|^{1/2}+|1|^{1/2})}^2 = 2$  
    hence $\|x+y\|_{\frac{1}{2}} \nleq \|x\|_{\frac{1}{2}} + \|y\|_{\frac{1}{2}}$  

-----
#EE501 - [[Linear Systems Theory]] at [[METU]]