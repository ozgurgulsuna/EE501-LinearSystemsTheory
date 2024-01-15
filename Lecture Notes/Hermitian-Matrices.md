###### Minimal Polynomial ######
## Hermitian Matrices ##

**Definition:** An $n \times n$ matrix $A$ is said to be **Hermitian** if $A = A^H = A^*$. Its conjugate transpose is equal to itself. If $A$ is real, then $A = A^T$.

--------------------------------------------------------------------------------------------------------------
**Theorem:** Let $A$ be Hermitian. Then $ \langle x,Ax \rangle $ is real for all $x \in \mathbb{C}^n$.

**Proof:** We will start with properties of inner products.

1- $ \large \langle x,y\rangle  = \overline{\langle y,x\rangle }$. 

Then we will substitute $A = A^*$ 
and in the last step we will use,
 
2- $ \large \langle x,Py\rangle  = \langle P^*x,y\rangle $.

Check the properties of inner products [here](Inner-Product-Spaces.md).


$\large\langle x,Ax\rangle  = \overline{\langle Ax,x\rangle } = \overline{\langle A^*x,x\rangle } = \overline{\langle x,Ax\rangle } \ \ \ \ \ \blacksquare$ 

--------------------------------------------------------------------------------------------------------------
**Theorem:** Let $A$ be Hermitian. Then all eigenvalues of $A$ are real.

**Proof:** Let $\lambda$ be an eigenvalue of $A$ and $x$ be the corresponding eigenvector. Then $Ax = \lambda x$. Then we will use the previous theorem.

$\large\lambda\langle x,x\rangle  = \langle \lambda x,x\rangle  = \langle Ax,x\rangle  = \overline{\langle x,Ax\rangle } = \overline{\langle x,\lambda x\rangle } = \overline{\lambda\langle x,x\rangle } = \overline{\lambda}\langle x,x\rangle $

Since $\langle x,x\rangle  \neq 0$, we can divide both sides by $\langle x,x\rangle $.

$\large\lambda = \overline{\lambda} \ \ \ \ \ \blacksquare$ 

--------------------------------------------------------------------------------------------------------------
**Theorem:** Let $A$ be Hermitian. Then all eigenvectors corresponding to distinct eigenvalues are orthogonal. Let $A$ be Hermitian and $\lambda_i \neq \lambda_j$ be two distinct eigenvalues of $A$ with corresponding eigenvectors $e_i$ and $e_j$. Then $\langle e_i,e_j\rangle = 0$.

**Proof:** Let $A$ be Hermitian and $\lambda_i \neq \lambda_j$ be two distinct eigenvalues of $A$ with corresponding eigenvectors $e_i$ and $e_j$. Then $Ae_i = \lambda_i e_i$ and $Ae_j = \lambda_j e_j$. Then we will use the previous theorem.

$\large \langle e_i,Ae_j\rangle  = \langle e_i,\lambda_je_j \rangle  = \lambda_j \langle e_i,e_j\rangle  \\
\large \langle e_i,Ae_j\rangle  = \langle A^*e_i,e_j\rangle  =\lambda_i \langle e_i,e_j\rangle  $

Then we will subtract the equations.

$\large (\lambda_j - \lambda_i)\langle e_i,e_j\rangle  = 0$

Since $ \large \lambda_j \neq \lambda_i$, we have $ \large \langle e_i,e_j\rangle  = 0 \ \ \ \ \ \blacksquare$

--------------------------------------------------------------------------------------------------------------
**Theorem:** Let $A$ be Hermitian. Then its minimal polynomial is

$$ \large m(s) = (s - \lambda_1 ) (s - \lambda_2 ) \cdots (s - \lambda_{\sigma} ) $$

where $\lambda_i$ are the distinct eigenvalues of $A$.

**Proof:** _Set Equality_ We will prove that $m(s)$ has no repeated roots. For which we need to use $N((A-\lambda I)) = N((A-\lambda I)^2)$.

In order to show the equality, we will prove that $N((A-\lambda I)) \subseteq N((A-\lambda I)^2)$ and $N((A-\lambda I)^2) \subseteq N((A-\lambda I))$.

1- $N((A-\lambda I)) \subseteq N((A-\lambda I)^2)$

Let $x \in N((A-\lambda I))$. Then $(A-\lambda I) x = 0$. Then we will multiply both sides by $(A-\lambda I)$.

$(A-\lambda I)^2 x = 0$

Then $x \in N((A-\lambda I)^2)$.

2- $N((A-\lambda I)^2) \subseteq N((A-\lambda I))$

Let $x \in N((A-\lambda I)^2)$. Then $(A-\lambda I)^2 x = 0$. 

$ \langle x, (A-\lambda I)^2 x \rangle  = 0$

$ \langle  x, (A-\lambda I) (A-\lambda I) x \rangle  = 0$

$ \langle (A-\lambda I) x, (A-\lambda I) x \rangle  = 0 = \|(A-\lambda I)x\|^2 \implies (A-\lambda I)x = 0

Then $x \in N((A-\lambda I))$.

Therefore Hermitian matrices $A$ with distinct eigenvalues have no repeated roots in their minimal polynomials. $\blacksquare$

$$ \large d(s) = (s - \lambda_1 ) (s - \lambda_2 ) \cdots (s - \lambda_{\sigma} ) $$

$$ \large m(s) = (s - \lambda_1 ) (s - \lambda_2 ) \cdots (s - \lambda_{\sigma} ) $$

$$ \large \mathbb{C}^n = N((A-\lambda_1 I)) \oplus N((A-\lambda_2 I)) \oplus \cdots \oplus N((A-\lambda_{\sigma} I)) $$

--------------------------------------------------------------------------------------------------------------
**Theorem:** Let $A$ be Hermitian matrix with characteristic polynomial $d(s) = (s - \lambda_1 )^{r_1} (s - \lambda_2 )^{r_2} \cdots (s - \lambda_{\sigma} )^{r_{\sigma}}$. Then there exist a unitary matrix $P$ such that $P^{-1} = P^*$ and $P^*AP = \Lambda$ where $\Lambda$ is a diagonal matrix with diagonal entries $\lambda_1, \lambda_2, \cdots, \lambda_{\sigma}$. 

$$ \large \Lambda = \begin{bmatrix} \lambda_1 & 0 & 0 & \cdots & 0 \\ 0 & \lambda_2 & 0 & \cdots & 0 \\ 0 & 0 & \lambda_3 & \cdots & 0 \\ \vdots & \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & 0 & \cdots & \lambda_\sigma \end{bmatrix} \text{ and each }\Lambda_i \in \mathbb{C}^{r_i \times r_i} \text{ , } \Lambda_i = \begin{bmatrix} \lambda_i & 0 & 0 & \cdots & 0 \\ 0 & \lambda_i & 0 & \cdots & 0 \\ 0 & 0 & \lambda_i & \cdots & 0 \\ \vdots & \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & 0 & \cdots & \lambda_i \end{bmatrix} $$

where $\lambda_i$ are the distinct eigenvalues of $A$.

**Proof**: See the lecture notes, page 50.

--------------------------------------------------------------------------------------------------------------
**Proof:** Let $A$ be Hermitian matrix with eigenvalues $\lambda_1, \lambda_2, \cdots, \lambda_{\sigma}$. Let $\lambda_min = \min_{i=1,2,\cdots,\sigma} \lambda_i$ and $\lambda_max = \max_{i=1,2,\cdots,\sigma} \lambda_i$. Then for all $x \in \mathbb{C}^n$,

$$ \large \lambda_{min} \langle x,x \rangle \leq \langle x,Ax \rangle \leq \lambda_{max} \langle x,x \rangle $$

**Proof:** See the lecture notes, page 51.

--------------------------------------------------------------------------------------------------------------
**Definition:** A Hermitian matrix $A$ is said to be **positive definite** if $\langle x,Ax \rangle > 0$ for all $x \in \mathbb{C}^n$ and $x \neq 0$. A Hermitian matrix $A$ is said to be **positive semidefinite** if $\langle x,Ax \rangle \geq 0$ for all $x \in \mathbb{C}^n$.

**Proof:** _By contradiction._ Let $A$ be positive definite Hermitioan, Then $\lambda_i > 0 \ \forall i = 1,2,\cdots,\sigma$.

$ \rightarrow$ Suppose not, Let $e \leq 0$ be an eigenvector of $A$.

From the positive definiteness of $A$, we have $\langle e,Ae \rangle > 0$.

$\langle e,Ae \rangle = \langle e,\lambda e \rangle = \lambda^* \langle e,e \rangle =\lambda \langle e,e \rangle > 0$

$\lambda \langle e,e \rangle > 0 \implies \lambda > 0$ which is a contradiction. $\blacksquare$

--------------------------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]