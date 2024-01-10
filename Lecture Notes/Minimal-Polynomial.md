###### Minimal Polynomial ######
## Cayley-Hamilton Theorem ##

<center>Every square matrix satisfies its own characteristic equation.</center>

$$ \mathbf{A}^n + d_1\mathbf{A}^{n-1} + \cdots + d_{n-1}\mathbf{A} + d_n\mathbf{I} = 0 $$

> Remark: Cayley-Hamilton Theorem basically states that nth and higher powers of a matrix can be expressed in terms of lower powers of the matrix. This is a very useful property in solving linear systems.

$ A^n = -d_1A^{n-1} - \cdots - d_{n-1}A - d_nI $

For previous example, we have:

$ A^2 - 4A + 3I = 0 $

$ A^2 = 4A - 3I $

$ A^3 = 4A^2 - 3A = 4(4A - 3I) - 3A = 13A - 12I $

$ A^4 = 4A^3 - 3A^2 = 4(13A - 12I) - 3(4A - 3I) = 49A - 48I $

--------------------------------------------------------------------------------------------------------------
$ \large exp(s) = \sum_{n=0}^{\infty} \frac{s^n}{n!} = I + s + \frac{s^2}{2!} + \frac{s^3}{3!} + \cdots$

$ \large exp(A) = \sum_{n=0}^{\infty} \frac{A^n}{n!} = I + A + \frac{A^2}{2!} + \frac{A^3}{3!} + \cdots$

--------------------------------------------------------------------------------------------------------------
$A^{-1} = ?$

$A^2 - 4A + 3I = 0$

$A - 4I + 3A^{-1} = 0$

$A^{-1} = \Large \frac{(4I - A)}{3}$

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> $A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$ $A^{100}=?$

_<ins>Solution:</ins>_ 

$A^{100} = \alpha A + \beta I$

$\lambda_1 = 3, \lambda_2 = 1 \text{, and } e_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, e_2 = \begin{bmatrix} 1 \\ -1 \end{bmatrix}$ 

$ A e_1 = \lambda_1 e_1 \Rightarrow A^2 e_1 = \lambda_1^2 e_1 \Rightarrow A^3 e_1 = \lambda_1^3 e_1 \Rightarrow \cdots \Rightarrow A^{100} e_1 = \lambda_1^{100} e_1 $

$ A e_2 = \lambda_2 e_2 \Rightarrow A^2 e_2 = \lambda_2^2 e_2 \Rightarrow A^3 e_2 = \lambda_2^3 e_2 \Rightarrow \cdots \Rightarrow A^{100} e_2 = \lambda_2^{100} e_2 $

$ A^{100} = \alpha A + \beta I \Rightarrow A^{100} e_1 = \alpha A e_1 + \beta e_1 \Rightarrow \lambda_1^{100} e_1 = \alpha \lambda_1 e_1 + \beta e_1 \Rightarrow \lambda_1^{100} = \alpha \lambda_1 + \beta \implies 3^{100} = 3\alpha + \beta $

$ A^{100} = \alpha A + \beta I \Rightarrow A^{100} e_2 = \alpha A e_2 + \beta e_2 \Rightarrow \lambda_2^{100} e_2 = \alpha \lambda_2 e_2 + \beta e_2 \Rightarrow \lambda_2^{100} = \alpha \lambda_2 + \beta \implies 1^{100} = \alpha + \beta $

$ \begin{cases} 3^{100} = 3\alpha + \beta \\ 1 = \alpha + \beta \end{cases} \Rightarrow  \begin{matrix} \alpha = \frac{3^{100} - 1}{2} \\ \beta = \frac{-3^{100} + 3}{2} \end{matrix}  $

$ A^{100} = \frac{3^{100} - 1}{2} A + \frac{-3^{100} + 3}{2} I $

--------------------------------------------------------------------------------------------------------------
## Minimal Polynomial ##

**Definition:** The monic polynomial is the polynomial with the highest degree coefficient equal to 1.

$ s^n + a_1s^{n-1} + \cdots \rightarrow $ monic

$ 2s^n + a_1s^{n-1} + \cdots \rightarrow $ not monic


**Definition:** The minimal polynomial of a matrix is the monic polynomial of the lowest degree that has the matrix as a root.

$$m(A) = 0_{n \times n}$$

**Theorem:** Given a matrix $A = \mathbb{C}^{n \ times n}$, let m(s) be its minimal polynomial. Then, the minimal polynomial is the smallest degree polynomial that satisfies the following:

<center>i) m(s) is unique. </center>

<center>ii) m(s) divides d(s) with no remainder. </center>

$$ \exists q(s)  \text{ s.t. } d(s) = q(s)m(s) $$

<center>iii) Every root of m(s) is a root of d(s). </center>


--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> $A = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 3 \end{bmatrix}$ $\Large \substack{d(s) = (s-1)(s-2)(s-3) \\ m(s) = (s-1)(s-2)(s-3)}$

> Remark: When A has distinct eigenvalues (which implies [diagonalizability](https://en.wikipedia.org/wiki/Diagonalizable_matrix) but converse is not true), the minimal polynomial is the same as the characteristic polynomial.

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> $A_1 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{bmatrix}$ $\Large \substack{d(s) = (s-1)(s-2)^2 \\ m(s) = (s-1)(s-2)} \ \ \ \ \ \ \  \normalsize A_2 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 2 & 1 \\ 0 & 0 & 2 \end{bmatrix}$ $\Large \substack{d(s) = (s-1)(s-2)^2 \\ m(s) = (s-1)(s-2)^2}$

A way to check if a minimal polynomial is correct is to check if the characteristic polynomial is zero when the minimal polynomial is substituted for s.

Let $m_1(s) = (s-1)(s-2)$ then $m_1(A) = (A-1I)(A-2I) = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} -1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} \checkmark$

Let $m_2(s) = (s-1)(s-2)$ then $m_2(A) = (A-1I)(A-2I) = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} -1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix} \neq 0 $

Then, $m_2(s) = (s-1)(s-2)^2 \implies m_2(A) = (A-1I)(A-2I)^2 = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} -1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix} \begin{bmatrix} -1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} \checkmark$

$ \mathbb{R}^3 = N(A-1I) \oplus N((A-2I)^2) $ where,

$ N(A-1I) = N \bigg ( \begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \bigg ) = \text{span} \bigg \{ \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} \bigg \} \ \ \text{dim} \bigg ( N(A-1I) \bigg ) = 1$

$ N((A-2I)^2) = N \bigg ( \begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} \bigg ) = \text{span} \bigg \{ \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix} \bigg \} \ \ \text{dim} \bigg ( N((A-2I)^2) \bigg ) = 2$


> Remark: There is a relationship between decomposition form and minimal polynomial in terms of power.
>
>$$ m(s) = (s-\lambda_1)^{d_1} \cdots (s-\lambda_k)^{d_k} $$
>
>$$ \mathbb{R}^n = N(A-\lambda_1I)^{d_1} \oplus \cdots \oplus N(A-\lambda_kI)^{d_k} $$

**Theorem:**

$$\mathbb{C}^n = N(A-\lambda_1I)^{m_1} \oplus N(A-\lambda_2I)^{m_2} \oplus \cdots \oplus N(A-\lambda_kI)^{m_k}$$

$$d(s) = (s-\lambda_1)^{r_1} \cdots (s-\lambda_k)^{r_k}$$

$$r_1 + r_2 + \cdots + r_k = n$$

$$m(s) = (s-\lambda_1)^{m_1} \cdots (s-\lambda_k)^{m_k}$$

$$1 \leq m_i \leq r_i $$

$\bar A = \begin{bmatrix} \bar A_1 & 0 & \cdots & 0 \\ 0 & \bar A_2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & \bar A_k \end{bmatrix}$ $\Large \substack{ \bar A = B^{-1}AB \text{,  B is composed of the basis vectors} \\ B = \begin{bmatrix} e_1 & e_2 & \cdots & e_n \end{bmatrix} \text{  for the  } N(A-\lambda_iI)^{m_i} }$

Size of $\bar A_i$ is $\text{dim} \bigg ( N(A-\lambda_iI)^{m_i} \bigg )$

--------------------------------------------------------------------------------------------------------------
<ins>Example:</ins> $A = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 2 \end{bmatrix}$ $\Large \substack{d(s) = (s-1)^3(s-2) \\ m(s) = (s-1)^2(s-2)}$

--------------------------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]