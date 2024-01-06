## Direct Sum ##

**Definition**: Let $V$ be a vector space and let $M_1, M_2, \ldots, M_k$ be subspaces of $V$. The **sum** of the subspaces $M$ is defined as

$$ M = \{m = m_1 + m_2 + \ldots + m_k \mid m_i \in M_i, i=1,2,\ldots,k\} $$

**Theorem**: The sum of subspaces $M$ is a subspace of $V$.

**Proof**:  
Let x, y $\in M$ Then,  
x = $m_1 + m_2 + \ldots + m_k$  
y = $\bar{m_1} + \bar{m_2} + \ldots + \bar{m_k}$   

$\alpha x + \beta y = \alpha(m_1 + m_2 + \ldots + m_k) + \beta(\bar{m_1} + \bar{m_2} + \ldots + \bar{m_k})$  
$\alpha x + \beta y = (\alpha m_1 + \beta \bar{m_1}) + (\alpha m_2 + \beta \bar{m_2}) + \ldots + (\alpha m_k + \beta \bar{m_k})$  

Since $\alpha m_i + \beta \bar{m_i} \in M_i$ for $i=1,2,\ldots,k$, we have $\alpha x + \beta y \in M$.

> **Remark**: Let $V=M_1+M_2+\ldots+M_k$ and let $M_1, M_2 \ldots, M_k$ are linearly independent. Let $x \in V$  
> $$ x = m_1 + m_2 + \ldots + m_k $$  
> $$\text{where $m_i \in M_i$ for $i=1,2,\ldots,k$}$$
> $$ m_1 + m_2 + \ldots + m_k = 0  \implies m_1 = m_2 = \ldots = m_k = 0$$
> $$\text{since $M_1, M_2 \ldots, M_k$ are linearly independent}$$

**Definition**: Let $M_1, M_2, \ldots, M_k$ be subspaces of $V$.
$$ \begin{align*}
&\text{i) $M = M_1 + M_2 + \ldots + M_k$} \\
&\text{ii) $M_1, M_2, \ldots, M_k$ are linearly independent}
\end{align*}$$

Then, $M$ is called the **direct sum** of $M_1, M_2, \ldots, M_k$ and we write $M = M_1 \oplus M_2 \oplus \ldots \oplus M_k$.

> When we have a direct sum, summation of dimensions of subspaces is equal to the dimension of the direct sum.

------------------------------------------------------------------------------------------

**Example**: $V = \mathbb{R}^4$ &emsp; $x = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} \in \mathbb{R}^4$

$M_1 = \{x \in \mathbb{R}^4 \mid x_3 = x_4 = 0\}$ dimension of $M_1$ is 2  
$M_2 = \{x \in \mathbb{R}^4 \mid x_1 = x_2 = 0\}$ dimension of $M_2$ is 2  
$M_3 = \{x \in \mathbb{R}^4 \mid x_1 = 0\}$ dimension of $M_3$ is 3

- $M_1 + M_2 = \mathbb{R}^4$
- $M_1 \oplus M_2 = \mathbb{R}^4$

------------------------------------------------------------------------------------------

**Definition**: If $M = V$, then $M = M_1 \oplus M_2 \oplus \ldots \oplus M_k$ is called a **direct sum decomposition** of $V$.

> **Remark**: Let $M = M_1 \oplus M_2 \oplus \ldots \oplus M_k$ be a direct sum decomposition of $V$. Then, the decomposition is unique.
**Proof**: Let $M = M_1 \oplus M_2 \oplus \ldots \oplus M_k$ and $M = \bar{M_1} \oplus \bar{M_2} \oplus \ldots \oplus \bar{M_k}$ be two direct sum decompositions of $V$. Then, 
> $$ \begin{align*}
&\text{i) $M = M_1 + M_2 + \ldots + M_k$} \\
&\text{ii) $M_1, M_2, \ldots, M_k$ are linearly independent} \\
&\text{iii) $M = \bar{M_1} + \bar{M_2} + \ldots + \bar{M_k}$} \\
&\text{iv) $\bar{M_1}, \bar{M_2}, \ldots, \bar{M_k}$ are linearly independent}
\end{align*}$$ 
> Let $x \in M_1 \cap \bar{M_1}$, then $x \in M_1$ and $x \in \bar{M_1}$. Since $M_1 \oplus \bar{M_1}$, we have $x = 0$.  
> Let $x \in M_2 \cap \bar{M_2}$, then $x \in M_2$ and $x \in \bar{M_2}$. Since $M_2 \oplus \bar{M_2}$, we have $x = 0$.  
$\vdots$  
> Let $x \in M_k \cap \bar{M_k}$, then $x \in M_k$ and $x \in \bar{M_k}$. Since $M_k \oplus \bar{M_k}$, we have $x = 0$.  
> Since $x = 0$ for all $x \in M_1 \cap \bar{M_1}, M_2 \cap \bar{M_2}, \ldots, M_k \cap \bar{M_k}$, we have $M_1 = \bar{M_1}, M_2 = \bar{M_2}, \ldots, M_k = \bar{M_k}$.

**Definition**: Let $V$ be an inner product space and let $M_1, M_2, \ldots, M_k$ be subspaces of $V$. The **orthogonal sum** of the subspaces $M$ is defined as

$$ <m_1, m_2> = 0 \quad \forall\text{ $m_1 \in M_1$ and $m_2 \in M_2$} $$

Orthogonality is denoted by $M_1 \perp M_2$.

------------------------------------------------------------------------------------------
**Definition**: Let $M = M_1 \oplus M_2 \oplus \ldots \oplus M_k$ and let $M_1 \perp M_2 \perp \ldots \perp M_k$. Then, $M$ is called the **orthogonal direct sum** of $M_1, M_2, \ldots, M_k$ and we write $M = M_1 \substack{\perp \\ \oplus} M_2 \substack{\perp \\ \oplus} \ldots \substack{\perp \\ \oplus} M_k$.

------------------------------------------------------------------------------------------
**Definition**: Let $M = M_1 \oplus M_2 \oplus \ldots \oplus M_k$ be a direct sum decomposition of $V$. Then, the **orthogonal complement** of $M_i$ is defined as

$$ M_i^{\perp} = \{x \in V \mid <x, m_i> = 0 \quad \forall\text{ $m_i \in M_i$}\} $$

> **Theorem**: $M_i^{\perp}$ is a subspace of $V$.  
> **Proof**: $x,y \in M^{\perp}$ then $\alpha x + \beta y \in M^{\perp}$ should be shown.
> - $0 \in M_i^{\perp}$ since $<0, m_i> = 0$ for all $m_i \in M_i$.
> - Let $x, y \in M_i^{\perp}$ and let $\alpha, \beta \in \mathbb{R}$. Then,
> $$ <\alpha x + \beta y, m_i> = \alpha<x, m_i> + \beta<y, m_i> = 0 $$
> for all $m_i \in M_i$. Therefore, $\alpha x + \beta y \in M_i^{\perp}$.

------------------------------------------------------------------------------------------
**Example**: $V = \mathbb{R}^3$ &emsp; $M = \text{span}\left\{\begin{bmatrix} 0 \\ -1 \\ 1 \end{bmatrix}, \begin{bmatrix} -1 \\ 0 \\ 1 \end{bmatrix} \right\}$ &emsp; $M^{\perp} = ? $

**Solution**: Let $x = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} \in M^{\perp}$


$<x, m_1> = 0$ &emsp; $<x, m_2> = 0$

$<x, \begin{bmatrix} 0 \\ -1 \\ 1 \end{bmatrix}> = 0 $  
$x_2 - x_3 = 0$  
$x_2 = x_3$  


$<x, \begin{bmatrix} -1 \\ 0 \\ 1 \end{bmatrix}> = 0$  
$-x_1 + x_3 = 0$  
$x_1 = x_3$  

$x = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} x_3 \\ x_3 \\ x_3 \end{bmatrix} = x_3 \begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix}$

$M^{\perp} = \text{span}\left\{\begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix}\right\}$

------------------------------------------------------------------------------------------

**Theorem**: Let $V$ be an inner product space and let $M$ be a subspace of $V$. Then, we can always write $M \oplus M^{\perp} = V$. That is $V$ can always be written as the direct sum of a subspace and its orthogonal complement.

**Proof**: We need to show two things:
1. $M$ and $M^{\perp}$ are linearly independent.
2. Any $x \in V$ can be written as $x = m + m^{\perp}$ where $m \in M$ and $m^{\perp} \in M^{\perp}$.

See lecture notes for the full proof.

-----
#EE501 - [[Linear Systems Theory]] at [[METU]]