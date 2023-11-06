###### Linear Spaces ######
## Linear (Vector) Spaces ##

**Definition**: A linear space (or vector space) over a [[field]] $F$ is a set $V$ with two operations, addition and scalar multiplication such that the following axioms hold:

**Vector Addition** $(+): V \times V \rightarrow V$ such that $x + y \in V$ for all $x,y \in V$.
- (A1) $x + y = y + x$   $\forall x,y \in V$ (commutativity)  
- (A2) $x + (y + z) = (x + y) + z$   $\forall x,y,z \in V$ (associativity)  
- (A3) There exists an element $0 \in V$ such that $x + 0 = x$   $\forall x \in V$ (existence of additive identity)  
- (A4) For every $x \in V$ there exist an element $-x \in V$ such that $x + (-x) = 0$   $\forall x \in V$ (existence of additive inverse)


**Scalar Multiplication** $(\cdot): F \times V \rightarrow V$ such that $\alpha x \in V$ for all $\alpha \in F$ and $x \in V$.  
- (M1) $\alpha (bx) = (\alpha b)x$   $\forall \alpha, \beta \in F$ and $\forall x \in V$ (associativity)  
- (M2) $\alpha(x+y) = \alpha x + \alpha y$   $\forall \alpha \in F$ and $\forall x,y \in V$ (distributivity)  
- (M3) $(\alpha + \beta)x = \alpha x + \beta x$   $\forall \alpha, \beta \in F$ and $\forall x \in V$ (distributivity)  
- (M4) $1_Fx = x$   $\forall x \in V$ (existence of multiplicative identity)

Elements of the vector space are called vectors, or points.

Scalar multiplication in a vector space depends on the field $F$. Thus when we say $x \in V$, we mean that $x$ is a vector in the vector space $V$ over the field $F$ or $(V,F)$.  
For example, $\mathbb{R}^n$ is a vector space over the field $\mathbb{R}$, and $\mathbb{C}^n$ is a vector space over the field $\mathbb{C}$.

> The simplest vector space contains only one point. In other words, $\{0\}$ is a vector space.


--------------------------------------------------------------------------
<ins>Example</ins>: Show that $x 0_F  = 0_V$ for all $x \in V$  
<ins>Proof:</ins>
1. $y = x0_F = 0_V$ is assumed to be true.
2. $x + y = x + x0_F = x1_F+ x0_F$      (M4)
3. $x + y = x(1_F + 0_F) = x1_F$            (M3)
4. $x + y + (-x) = x1_F + (-x1_F)$      (A4)
5. $y = x(1_F + (-1_F)) = x0_V = 0_V$     (A2)    $\blacksquare$
  
------------------------------------------------------------------------------------------
<ins>Example</ins>: Show that $x0_F = 0_v$  
<ins>Proof:</ins>  
1. Assume $y = x0_F$ and show $y = 0_V$.  
2. $x + y = x + x0_F = x1_F + x0_F$       (M4)
3. $x + y = x1_F + x0_F = x(1_F + 0_F)$   (M3)
4. $x + y = x(1_F + 0_F) = x1_F$              (A3)
5. $x + y = x1_F = x$                            (M4)
6. $x + y + (-x) = x + (-x)$               (A4)
7. $y = x + (-x) = 0_V$                         (A4)    $\blacksquare$

>**Remark**: A vector space has a unique additive identity.


###### Linear Spaces ######
### Function Space ###
**Definition**: Let $S$ be a set and $F$ be a field. The set of all functions from $S$ to $F$ is denoted by $F^S$.

For $f,g \in F^S$, the sum $f+g \in F^S$ is the function defined by  

$$(f+g)(x) = f(x) + g(x), \ \forall x \in S$$

For $f \in F^S$ and $\alpha \in F$, the product $\alpha f \in F^S$ is the function defined by

$$(\alpha f)(x) = \alpha f(x), \ \forall x \in S$$  

------------------------------------------------------------------------------
<ins>Example</ins>: Set of all [[polynomials]] with degree n with coefficients in $F$ is denoted by $F[x]_n$.

What essentially function spaces are, is that they are the set of all functions from a set to a field. For example, the set of all polynomials with degree n with coefficients in $F$ is denoted by $F[x]_n$.

###### Linear Spaces ######
## [[Basis]] ##

**Definition**: Let $V$ be a vector space. A (finite) set of vectors $S=\{v_1, v_2, \dots, v_n\}$ is called a [[basis set]] for $V$ iff

   *  $Span(S)=V$
   * $S$ is [[Linearly Independent]]

A (finite dimensional) linear space $V$ has many bases. All bases of a linear space have the same number of elements. This number is called the [[dimension]] of the linear space.

<ins>Example</ins>: $V = \mathbb{R}^2$, consider the two [[base]]s:

$S_1 = \begin{Bmatrix}\begin{bmatrix} 0 \\ 1 \end{bmatrix},\begin{bmatrix} 1 \\ 0 \end{bmatrix}\end{Bmatrix}$,             $S_2 = \begin{Bmatrix}\begin{bmatrix} 1 \\ 1 \end{bmatrix},\begin{bmatrix} 2 \\ 3 \end{bmatrix}\end{Bmatrix}$

1. $S_1$ is linearly independent set since $c_1\begin{bmatrix} 0 \\ 1 \end{bmatrix} + c_2\begin{bmatrix} 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$ implies $c_1 = c_2 = 0$,   $\forall c_1 , c_2 \in \mathbb{R}(F)$.
2. $Span(S_1) = V = \mathbb{R}^2$
Hence $S_1$ is a basis for $V$.

1. $S_2$ is linearly independent set since $c_1\begin{bmatrix} 1 \\ 1 \end{bmatrix} + c_2\begin{bmatrix} 2 \\ 3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$ implies $c_1 = c_2 = 0$,   $\forall c_1 , c_2 \in \mathbb{R}(F)$.
2. $Span(S_2) = V = \mathbb{R}^2$
   

<ins>Example</ins>: $V = \mathbb{R}^2$, and $F = \mathbb{R}$, consider the base:  
$B = \begin{Bmatrix}\begin{bmatrix} 1 \\ 0 \end{bmatrix},\begin{bmatrix} 1 \\ 1 \end{bmatrix}\end{Bmatrix}$  $y = \begin{bmatrix} 2 \\ 3 \end{bmatrix}$ $[y]_B$=?

<ins>Solution</ins>:  
1. $B$ is linearly independent set since $c_1\begin{bmatrix} 1 \\ 0 \end{bmatrix} + c_2\begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$ implies $c_1 = c_2 = 0$,   $\forall c_1 , c_2 \in \mathbb{R}(F)$.  
2. $Span(B) = V = \mathbb{R}^2$  
3. $[y]_B = \begin{bmatrix} c_1 \\ c_2 \end{bmatrix}$  
4. $y = c_1\begin{bmatrix} 1 \\ 0 \end{bmatrix} + c_2\begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} c_1 + c_2 \\ c_2 \end{bmatrix}$  
5. $c_1 + c_2 = 2$ and $c_2 = 3$  
6. $c_1 = -1$ and $c_2 = 3$  
7. $[y]_B = \begin{bmatrix} -1 \\ 3 \end{bmatrix}$


<ins>Example</ins>: $V = Span\{cos(t), sin(t)\}$, and $F = \mathbb{R}$, consider the base:  
$B = \begin{Bmatrix}cos(t), sin(t)\end{Bmatrix}$  $y = cos(t-\frac{\pi}{3})$ $[y]_B$=?

<ins>Solution</ins>:

1. $B$ is linearly independent set since $c_1cos(t) + c_2sin(t) = 0$ implies $c_1 = c_2 = 0$,   $\forall c_1 , c_2 \in \mathbb{R}(F)$.  
2. $Span(B) = V = Span\{cos(t), sin(t)\}$  
3. $[y]_B = \begin{bmatrix} c_1 \\ c_2 \end{bmatrix}$
4. $y = c_1cos(t) + c_2sin(t) = cos(t-\frac{\pi}{3}) = cos(t)cos(\frac{\pi}{3}) + sin(t)sin(\frac{\pi}{3}) = \frac{1}{2}cos(t) + \frac{\sqrt{3}}{2}sin(t)$     
5. $c_1 = \frac{1}{2}$ and $c_2 = \frac{\sqrt{3}}{2}$ 
6. $[y]_B = \begin{bmatrix} \frac{1}{2} \\ \frac{\sqrt{3}}{2} \end{bmatrix}$  


**Claim**: For a given basis $B$, the representation $[y]_B$ of a vector $y$ is unique.  
   <ins>Proof</ins>: By contradiction.  
   Assume $[y]_B = \begin{bmatrix} c_1 \\ c_2 \end{bmatrix}$ and $[y]_B = \begin{bmatrix} d_1 \\ d_2 \end{bmatrix}$  
   Then $y = c_1b_1 + c_2b_2 = d_1b_1 + d_2b_2$  
   $c_1b_1 + c_2b_2 - d_1b_1 - d_2b_2 = 0$  
   $(c_1 - d_1)b_1 + (c_2 - d_2)b_2 = 0$  
   Since $B$ is linearly independent, $c_1 - d_1 = 0$ and $c_2 - d_2 = 0$  
   Hence $c_1 = d_1$ and $c_2 = d_2$  $\blacksquare$

**Remark**: The representation of a vector $y$ in a basis $B$ is unique. The representation of a vector $y$ in a basis $B$ is called the [[coordinate vector]] of $y$ with respect to $B$.

###### Linear Spaces ######
## [[Ordered Basis]] ##

**Definition**: Let $V$ be a vector space. An ordered set of basis vectors $S=\{v_1, v_2, \dots, v_n\}$ is called an [[ordered basis]] for $V$.
If $y = (x_1,x_2,...,x_n)$ is an ordered basis for $V$, then every vector $x \in V$ can be written as a linear combination of the basis vectors as follows:


**Theorem:** Let $V$ be an n-dimensional vector space over $\mathbb{R}$. Let $B_1$ and $B_2$ be two bases for $V$. Then there exists a unique $n \times n$ real invertible matrix $P$ such that $[x]_{B_2} = P[x]_{B_1}$ for all $x \in V$.

<ins>Proof</ins>: By construction.





<ins>Example</ins>: Consider $V =$ polynomials of degree $\leq 2$ with coefficients in $\mathbb{R}$ and the bases:  
$B_1 = \begin{Bmatrix}1, t-1, (t-1)^2\end{Bmatrix}$  
$B_2 = \begin{Bmatrix}1, t, t^2\end{Bmatrix}$  
Find the matrix $P$ such that $[x]_{B_1} = P[x]_{B_2}$ for all $x \in V$.

<ins>Solution</ins>:  
1. $[x]_{B_1} = \begin{bmatrix} c_1 \\ c_2 \\ c_3 \end{bmatrix}$ and $[x]_{B_2} = \begin{bmatrix} d_1 \\ d_2 \\ d_3 \end{bmatrix}$  
2. $x = c_1 + c_2(t-1) + c_3(t-1)^2 = c_1 + c_2t - c_2 + c_3t^2 - 2c_3t + c_3$  
3. $x = (c_1 - c_2 + c_3) + (c_2 - 2c_3)t + c_3t^2$  
4. $d_1 = c_1 - c_2 + c_3$  
5. $d_2 = c_2 - 2c_3$  
6. $d_3 = c_3$  
7. $c_1 = d_1 + d_2 + d_3$  
8. $c_2 = d_2 + 2d_3$  
9. $c_3 = d_3$  
10. $[x]_{B_1} = \begin{bmatrix} d_1 + d_2 + d_3 \\ d_2 + 2d_3 \\ d_3 \end{bmatrix} = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} d_1 \\ d_2 \\ d_3 \end{bmatrix} = P[x]_{B_2}$  
11. $P = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \end{bmatrix}$ 



-----
#EE501 - [[Linear Systems Theory]] at [[METU]]