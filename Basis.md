###### Linear Spaces ######
## Basis ##

**Definition**: Let $V$ be a vector space. A (finite) set of vectors $S=\{v_1, v_2, \dots, v_n\}$ is called a [[basis set]] for $V$ iff

   *  $Span(S)=V$
   * $S$ is [[Linearly Independent]]

A (finite dimensional) linear space $V$ has many bases. All bases of a linear space have the same number of elements. This number is called the [[dimension]] of the linear space.

------------------------------------------------------------------------------------------
<ins>Example</ins>: $V = \mathbb{R}^2$, consider the two [[base]]s:

$S_1 = \begin{Bmatrix}\begin{bmatrix} 0 \\ 1 \end{bmatrix},\begin{bmatrix} 1 \\ 0 \end{bmatrix}\end{Bmatrix}$

1. $S_1$ is linearly independent set since $c_1\begin{bmatrix} 0 \\ 1 \end{bmatrix} + c_2\begin{bmatrix} 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$ implies $c_1 = c_2 = 0$,   $\forall c_1 , c_2 \in \mathbb{R}(F)$.
2. $Span(S_1) = V = \mathbb{R}^2$
Hence $S_1$ is a basis for $V$.

$S_2 = \begin{Bmatrix}\begin{bmatrix} 1 \\ 1 \end{bmatrix},\begin{bmatrix} 2 \\ 3 \end{bmatrix}\end{Bmatrix}$

1. $S_2$ is linearly independent set since $c_1\begin{bmatrix} 1 \\ 1 \end{bmatrix} + c_2\begin{bmatrix} 2 \\ 3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$ implies $c_1 = c_2 = 0$,   $\forall c_1 , c_2 \in \mathbb{R}(F)$.
2. $Span(S_2) = V = \mathbb{R}^2$
   
------------------------------------------------------------------------------------------
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

------------------------------------------------------------------------------------------
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

> **Remark**: The representation of a vector $y$ in a basis $B$ is unique. The representation of a vector $y$ in a basis $B$ is called the [[coordinate vector]] of $y$ with respect to $B$.

------------------------------------------------------------------------------------------
## Ordered Basis ##

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


------------------------------------------------------------------------------------------
<ins>Example</ins>: Show that Matrix $P$ is invertible.  
$~$<ins>Proof</ins>: Let $V$ be an n-dimensional vector space over $\mathbb{R^{n\times n}}$. $B_1$ and $B_2$ are bases for $V$. A vector $v$ holds,  
- $[v]_{B_1} = P[v]_{B_2}$
- $\exist \ Q \in \mathbb{R^{n \times n}}$ s.t.
   - $[v]_{B_2} = Q[v]_{B_1}$
   - $[v]_{B_1} = P[v]_{B_2} = P(Q[v]_{B_1}) = (PQ)[v]_{B_1}$ implies $PQ = I$
   - similarly $QP = I$
- $P$ is invertible and $P^{-1} = Q$  $\blacksquare$

------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]