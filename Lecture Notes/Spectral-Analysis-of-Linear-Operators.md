## Spectral Analysis of Linear Operators ##

**Definition:** Let $A:V \to V$ be a linear transformation defined over vector space $V$. A subspace $W$ of $V$ is called an invariant under $A$ if $A(x) \in W$ for all $x \in W$.

> Let $A$ be a linear transformation defined over $\mathbb{R}^2$ such that $A(x,y) = (x+y, x-y)$. Then, $W = \{(x,0) \in \mathbb{R}^2 \mid x \in \mathbb{R}\}$ is an invariant subspace under $A$.

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> $R(A)$ is an invariant subspace under $A$.  

_<ins>Solution:</ins>_ Let $x \in R(A)$. Then, $x = Ay$ for some $y \in V$. Then, $Ax = A(Ay) = A^2y \in R(A)$.

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> Let $M = \text{s}pan \bigg\{ \begin{bmatrix} 1 \\ 1 \end{bmatrix}\bigg \}$ and $A = \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix}$. is $M$ an invariant subspace under $A$  

_<ins>Solution:</ins>_ Let $x = \begin{bmatrix} x_1 \\ x_1 \end{bmatrix} \in M$. Then, $Ax = \begin{bmatrix} x_1 + 2x_1 \\ 2x_1 + x_1 \end{bmatrix} = \begin{bmatrix} 3x_1 \\ 3x_1 \end{bmatrix} = 3 x_1 \begin{bmatrix} 1 \\ 1 \end{bmatrix} \in M$. Thus, $M$ is an invariant subspace under $A$.

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> $N(A)$ is an invariant subspace under $A$.

_<ins>Solution:</ins>_ Let $x \in N(A)$. Then, $Ax = 0 \in N(A)$.

--------------------------------------------------------------------------------------------------------------
**Definition:** Powers of a linear transformation $A$ are defined as follows:

$$A^k = \underbrace{A(A(\cdots(Ax)\cdots))}_{k \text{ times}}$$

By using this definition, polynomials of a linear transformation $A$ can be constructed as linear combinations of powers of $A$

$$p(A) = \alpha_0 A^n + \alpha_1 A^{n-1} + \cdots + \alpha_{n-1}A + \alpha_n I$$

where $I$ is the identity transformation and $\alpha_0, \alpha_1, \cdots, \alpha_n$ are scalars. 

> **Property:** $A \ p(A) = p(A) \ A \ \implies$ A commutes with any polynomial of $A$.

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> Show that $A^2 = 2A + 3I$ for $A = \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix}$.

_<ins>Solution:</ins>_ $A^2 = \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix} \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix} = \begin{bmatrix} 5 & 4 \\ 4 & 5 \end{bmatrix} = 2 \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix} + \begin{bmatrix} 3 & 0 \\ 0 & 3 \end{bmatrix} = 2A + 3I$.

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> Show that $R(p(A)) \text{ and } N(p(A))$ are invariant subspaces under $A$ for any polynomial $p(A)$.

_<ins>Solution:</ins>_ Let $x \in R(p(A))$. Then, $x = p(A)y$ for some $y \in V$. Then, $Ax = Ap(A)y = p(A)(Ay) \in R(p(A))$. Thus, $R(p(A))$ is an invariant subspace under $A$. 

Let $x \in N(p(A))$. Then, $p(A)x = 0$. Then, $(p(A)A)x = (Ap(A))x = A0 = 0$. Thus, $Ax \in N(p(A))$. Thus, $N(p(A))$ is an invariant subspace under $A$.

--------------------------------------------------------------------------------------------------------------
**Definition:** Let $A$ denote the matrix representation of a linear transformation $A:V \to V$ with $A$ being an $n \times n$ matrix. Then, the **eigenvalues** of $A$ are the roots of the **characteristic polynomial** of $A$.

$$\det(sI - A) = 0$$

$$\lambda_i = \text{eigenvalues for } A $$

$$\text{ in other words, roots of } \det(sI - A) = 0$$

--------------------------------------------------------------------------------------------------------------
**Definition:** Vectors $e_i \in V$ satisfying $Ae_i = \lambda_i e_i$ are called **eigenvectors** of $A$ corresponding to the eigenvalues $\lambda_i$.

<ins>Example:</ins> Find the eigenvalues and eigenvectors of $A = \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix}$.

_<ins>Solution:</ins>_ $\det(sI - A) = \det \begin{bmatrix} s-1 & -2 \\ -2 & s-1 \end{bmatrix} = (s-1)^2 - 4 = s^2 - 2s - 3 = (s-3)(s+1) = 0$. Thus, $\lambda_1 = 3$ and $\lambda_2 = -1$.

$$\text{For } \lambda_1 = 3, \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = 3 \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} \implies \begin{bmatrix} -2 & 2 \\ 2 & -2 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = 0 \implies x_1 = x_2 \implies \begin{bmatrix} x_1 \\ x_1 \end{bmatrix} = x_1 \begin{bmatrix} 1 \\ 1 \end{bmatrix}$$

$$\text{For } \lambda_2 = -1, \begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = -1 \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} \implies \begin{bmatrix} 2 & 2 \\ 2 & 2 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = 0 \implies x_1 = -x_2 \implies \begin{bmatrix} x_1 \\ -x_1 \end{bmatrix} = x_1 \begin{bmatrix} 1 \\ -1 \end{bmatrix}$$

$$\text{Thus, } e_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix} \text{ and } e_2 = \begin{bmatrix} 1 \\ -1 \end{bmatrix} \text{ are the eigenvectors of } A \text{ corresponding to } \lambda_1 = 3 \text{ and } \lambda_2 = -1 \text{ respectively.}$$

$$\text{Note that } e_1 \text{ and } e_2 \text{ are linearly independent.}$$

$$\text{Also, } \begin{bmatrix} 1 \\ 1 \end{bmatrix} \text{ and } \begin{bmatrix} 1 \\ -1 \end{bmatrix} \text{ are orthogonal.}$$

$$\text{Thus, } \mathbb{R}^2 = \text{span} \bigg \{ \begin{bmatrix} 1 \\ 1 \end{bmatrix}\bigg \} \oplus \text{span} \bigg \{ \begin{bmatrix} 1 \\ -1 \end{bmatrix}\bigg \}$$

--------------------------------------------------------------------------------------------------------------
**Theorem:** Consider the linear tranasformation $y = Ax$ with $A$ being an $n \times n$ matrix. Suppose that

I. $\mathbb{C}^n = M_1 \oplus M_2 \oplus \cdots \oplus M_k$

II. $M_i$ is an invariant subspace under $A$ for $i = 1, 2, \cdots, k$

Then, the transformation $A$ can be represented as a block diagonal matrix.

$\bar A = \begin{bmatrix} \bar  A_1 & 0 & \cdots & 0 \\ 0 & \bar A_2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & \bar  A_k \end{bmatrix}$

where $\bar A = P^{-1}AP$ 

$P = \begin{bmatrix} p_1 & p_2 & \cdots & p_k \end{bmatrix}$

$p_i = \begin{bmatrix} e_i^1 & e_i^2 & \cdots & e_i^{n_i} \end{bmatrix}$

$n_i$ is the dimension of $M_i$ and $e_i^j$ is the $j^{th}$ eigenvector of $A$ corresponding to the eigenvalue $\lambda_i$.

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> Let $A = \begin{bmatrix} 1 & 1 & -1 \\ -1 & 3 & -2 \\ 0 & 0 & 1 \end{bmatrix}$. $M_1 =\text{span} \bigg \{ \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} \bigg \}$ and $M_2 = \text{span} \bigg \{ \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix} \bigg \}$ are invariant subspaces under $A$.  

1- Is $M_1$ invariant under $A$?

2- Is $M_2$ invariant under $A$?

3- Change the basis in both domain and codomain to $\{ b_1^1, b_1^2, b_2^1 \}$ 

_<ins>Solution:</ins>_ 1- Let $x \in M_1$. Then, $x = \alpha_1 \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix} + \alpha_2 \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}$. Then, $Ax = \begin{bmatrix} 2\alpha_1 + \alpha_2 \\ 2\alpha_1 + 3\alpha_2 \\ 0 \end{bmatrix} = 2\alpha_1 + \alpha_2 \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix} + 2\alpha_2 \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} \in M_1$. Thus, $M_1$ is an invariant subspace under $A$.

2- Let $x \in M_2$. Then, $x = \alpha_1 \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}$. Then, $Ax = \begin{bmatrix} 0 \\ \alpha_1 \\ \alpha_1 \end{bmatrix} = \alpha_1 \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix} \in M_2$. Thus, $M_2$ is an invariant subspace under $A$.

3- $P = \begin{bmatrix} 1 & 0 & 0 \\ 1 & 1 & 1 \\ 0 & 0 & 1 \end{bmatrix}$ and $P^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ -1 & 1 & -1 \\ 0 & 0 & 1 \end{bmatrix}$

$\bar A = P^{-1}AP = \begin{bmatrix} 1 & 0 & 0 \\ -1 & 1 & -1 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} 1 & 1 & -1 \\ -1 & 3 & -2 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} 1 & 0 & 0 \\ 1 & 1 & 1 \\ 0 & 0 & 1 \end{bmatrix} = \begin{bmatrix} 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix}$

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> Let $A = \begin{bmatrix} 1 & 0 & 0 \\ -1 & 2 & 1 \\ 0 & 0 & 3 \end{bmatrix}$. Find the eigenvalues and eigenvectors of $A$.

_<ins>Solution:</ins>_ $\det(sI - A) = \det \begin{bmatrix} s-1 & 0 & 0 \\ 1 & s-2 & -1 \\ 0 & 0 & s-3 \end{bmatrix} = (s-1)(s-2)(s-3) = 0$. Thus, $\lambda_1 = 1$, $\lambda_2 = 2$ and $\lambda_3 = 3$.

$\text{For } \lambda_1 = 1, N(A-I) = N \bigg ( \begin{bmatrix} 0 & 0 & 0 \\ -1 & 1 & 1 \\ 0 & 0 & 2 \end{bmatrix} \bigg ) = \text{span} \bigg \{ \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix}\bigg \} = e_1$

$\text{For } \lambda_2 = 2, N(A-2I) = N \bigg ( \begin{bmatrix} -1 & 0 & 0 \\ -1 & 0 & 1 \\ 0 & 0 & 1 \end{bmatrix} \bigg ) = \text{span} \bigg \{ \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}\bigg \} = e_2$

$\text{For } \lambda_3 = 3, N(A-3I) = N \bigg ( \begin{bmatrix} -2 & 0 & 0 \\ -1 & -1 & 1 \\ 0 & 0 & 0 \end{bmatrix} \bigg ) = \text{span} \bigg \{ \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}\bigg \} = e_3$

A is diagonalizable since $e_1, e_2, e_3$ are linearly independent. $P \bar A = AP$

$P = \begin{bmatrix} 1 & 0 & 0 \\ 1 & 1 & 1 \\ 0 & 0 & 1 \end{bmatrix}$ and

$\begin{bmatrix} e_1 & e_2 & e_3 \end{bmatrix} \begin{bmatrix} 1 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 3 \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ -1 & 2 & 1 \\ 0 & 0 & 3 \end{bmatrix} \begin{bmatrix} e_1 & e_2 & e_3 \end{bmatrix}$

$\bar A = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 3 \end{bmatrix}$

--------------------------------------------------------------------------------------------------------------
**Theorem:** Let $A$ be an $n \times n$ matrix with distinct eigenvalues $\lambda_1, \lambda_2, \cdots, \lambda_k$. Then, the eigenvectors $e_1, e_2, \cdots, e_k$ corresponding to $\lambda_1, \lambda_2, \cdots, \lambda_k$ are linearly independent.

$$ \lambda_i \neq \lambda_j \implies e_i \text{ when } i \neq j$$

Then the set of eigenvectors $\{e_1, e_2, \cdots, e_k\}$ for a linearly independent set. Moreover,

$$\text{span} \{e_i\} = N(A - \lambda_i I)$$

$$\text{span} \{e_1, e_2, \cdots, e_k\} = \mathbb{C}^n= N(A - \lambda_1 I) \oplus N(A - \lambda_2 I) \oplus \cdots \oplus N(A - \lambda_k I)$$

$$\bar A = P^{-1}AP = \begin{bmatrix} \lambda_1 & 0 & \cdots & 0 \\ 0 & \lambda_2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & \lambda_k \end{bmatrix}$$

**Proof:** Can be found in the textbook.

--------------------------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]