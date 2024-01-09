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






--------------------------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]