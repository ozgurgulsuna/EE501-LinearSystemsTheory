###### Linear Transformations ######
## Linear Mapping ##

**Definition**: Let $V$ and $W$ be linear spaces over the same field $F$. A mapping $\mathcal{T}: V \rightarrow W$ is called a linear mapping satisfying 

$$\mathcal{T}(ax+by) = a\mathcal{T}(x) + b\mathcal{T}(y) \ \ \ \ \ \ \forall x,y \in V \ \ \ \ \ \ \forall a,b \in F$$

here $V$ is called the domain of $T$ and $W$ is called the codomain of $\mathcal{T}$.

------------------------------------------------------------------------------------------
<ins>Example</ins>: Let $V = W$ polynomials of degree less than $n$ in $S$; $\mathcal{T} = \frac{d}{ds}$

**_Solution_**: Let $p,q \in V$ and $\alpha_1,\alpha_2 \in F$ then ,   
p(s) = $\sum_{i=0}^{n-1} a_is^i$ and q(s) = $\sum_{i=0}^{n-1} b_is^i$  
$\alpha_1p(s) + \alpha_2q(s) = \sum_{i=0}^{n-1} (\alpha_1a_i + \alpha_2b_i)s^i$  
$\frac{d}{ds}(\alpha_1p(s) + \alpha_2q(s)) = \sum_{i=0}^{n-1} (\alpha_1a_i + \alpha_2b_i)is^{i-1} = \alpha_1\sum_{i=0}^{n-1} a_is^{i-1} + \alpha_2\sum_{i=0}^{n-1} b_is^{i-1} = \alpha_1\frac{dp}{ds} + \alpha_2\frac{dq}{ds}$  
$\mathcal{T}(\alpha_1p+\alpha_2q) = \frac{d}{ds}(\alpha_1p+\alpha_2q) = \alpha_1\frac{dp}{ds} + \alpha_2\frac{dq}{ds} = \alpha_1\mathcal{T}(p) + \alpha_2\mathcal{T}(q) \ \blacksquare$

<!-- 
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

> Sharing the same field is a necessary condition for two vector spaces to be comparable. For example, $\mathbb{R}^n$ and $\mathbb{C}^n$ are not comparable.  

> The simplest vector space contains only one point. In other words, $\{0\}$ is a vector space.

------------------------------------------------------------------------------------------
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


### Function Space ###  
**Definition**: Let $S$ be a set and $F$ be a field. The set of all functions from $S$ to $F$ is denoted by $F^S$.

For $f,g \in F^S$, the sum $f+g \in F^S$ is the function defined by  

$$(f+g)(x) = f(x) + g(x), \ \forall x \in S$$

For $f \in F^S$ and $\alpha \in F$, the product $\alpha f \in F^S$ is the function defined by

$$(\alpha f)(x) = \alpha f(x), \ \forall x \in S$$  

------------------------------------------------------------------------------------------
<ins>Example</ins>: Set of all [[polynomials]] with degree n with coefficients in $F$ is denoted by $F[x]_n$.


> What essentially function spaces are, is that they are the set of all functions from a set to a field. For example, the set of all polynomials with degree n with coefficients in $F$ is denoted by $F[x]_n$. -->

------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]