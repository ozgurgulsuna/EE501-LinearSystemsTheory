###### Linear Spaces ######
## Span and Linear Independence ##

**Linear Combination**: A [[linear combination]] of a set of vectors $S = \{v_1, v_2, \dots, v_n\}$ in a vector space $V$ is a vector of the form $c_1v_1 + c_2v_2 + \dots + c_nv_n$, where $c_1, c_2, \dots, c_n$ are scalars.

**Span**: Let $S = \{v_1, v_2, \dots, v_n\}$ be a set of vectors in a vector space $V$. The set of all linear combinations of the vectors in $S$ is called the [[span]] of $S$ and is denoted by $Span(S)$.

**Linear Independence**: A set of vectors $S = \{v_1, v_2, \dots, v_n\}$ in a vector space $V$ is called [[linearly independent]] iff the only linear combination of the vectors in $S$ that equals the zero vector is the trivial linear combination, that is, $c_1v_1 + c_2v_2 + \dots + c_nv_n = 0$ implies $c_1 = c_2 = \dots = c_n = 0$.

> Zero vector cannot be an element of an independent set.

------------------------------------------------------------
<ins>**Example**</ins>:  $X =  \left\{\begin{bmatrix} 0 \\ 1 \end{bmatrix} ,\begin{bmatrix} 0 \\ 1 \end{bmatrix}\right\} $

- $X$ is linearly independent set since $c_1\begin{bmatrix} 0 \\ 1 \end{bmatrix} + c_2\begin{bmatrix} 0 \\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$ implies $c_1 = c_2 = 0$,   $\forall c_1 , c_2 \in \mathbb{R}(F)$.

- $Span(X) = \mathbb{R}^2$

------------------------------------------------------------
<ins>**Example**</ins>: Consider the linear space of polynomials with degree $n \leq 2$. Let subset $S=\{p_1, p_2, p_3\}$ where $p_1(t) = 1$, $p_2(t) = t$, $p_3(t) = t^2$. Is $S$ linearly independent?  
$~$<ins>**Proof**</ins>: Let $a_1, a_2, a_3 \in \mathbb{R}$,  
- $a_1p_1(t) + a_2p_2(t) + a_3p_3(t) = 0$
- $a_1 + a_2t + a_3t^2 = 0$
- $a_1 = a_2 = a_3 = 0$
    - Hence $S$ is linearly independent.

------------------------------------------------------------
<ins>**Example**</ins>: $S =\{cos(t), sin(t), cos(t-\pi/3)\}$   
$~$<ins>**Proof**</ins>: Let $a_1, a_2, a_3 \in \mathbb{R}$,
- $a_1cos(t) + a_2sin(t) + a_3cos(t-\pi/3) = 0$
- $a_1cos(t) + a_2sin(t) + a_3(cos(t)cos(\pi/3) + sin(t)sin(\pi/3)) = 0$
- $a_1cos(t) + a_2sin(t) + a_3(cos(t)1/2 + sin(t)\sqrt{3}/2) = 0$
- $a_1cos(t) + a_2sin(t) + a_3cos(t)/2 + a_3sin(t)\sqrt{3}/2 = 0$
- $a_1cos(t) + a_3cos(t)/2 + a_2sin(t) + a_3sin(t)\sqrt{3}/2 = 0$
- $(a_1 + a_3/2)cos(t) + (a_2 + a_3\sqrt{3}/2)sin(t) = 0$
- $a_1 + a_3/2 = 0$ and $a_2 + a_3\sqrt{3}/2 = 0$
- $a_1 = -a_3/2$ and $a_2 = -a_3\sqrt{3}/2$ 
    - Hence $S$ is linearly dependent.



------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]