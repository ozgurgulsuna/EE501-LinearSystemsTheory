## Functions of a Matrix ##

The motivation is to study matrix-valued functions, which stems from the differential equations describing linear systems.

$$ \large \dot{x} = A x(t) $$
$$ \large x(t) = e^{At} x(0) $$

The power series representation of any function is

$$ \large f(s) = \sum_{i=0}^{\infty} \alpha_i s^i $$

where $s \in \mathbb{C}$.

The power series representation of a matrix-valued function is

$$ \large f(A) = \sum_{i=0}^{\infty} \alpha_iA^i $$

where $A \in \mathbb{C}^{n \times n}$. This solution is another matrix as the same size as $A$.

The exponential function is defined for matrices as

$$ \large e^t = \sum_{i=0}^{\infty} \frac{t^i}{i!} \implies e^A = \sum_{i=0}^{\infty} \frac{A^i}{i!} $$

By using Cayley-Hamilton Theorem, we can write $A^i$ as a linear combination of $I,A,A^2,\cdots,A^{n-1}$.

$$ \large e^A = c_0 I + c_1 A + c_2 A^2 + \cdots + c_{n-1} A^{n-1} $$

where $c_i$ are scalars.

> Remark: One can use the minimal polynomial of a matrix to express the $l$th power of a matrix in terms of $I,A,A^2,\cdots,A^{l-1}$. $l$ is the order of the minimal polynomial.
>
> $$ \large e^A = c_0 I + c_1 A + c_2 A^2 + \cdots + c_{l-1} A^{l-1} $$

--------------------------------------------------------------------------------------------------------------
## First Method ##

Let 

$$ f(s) = \sum_{i=0}^{\infty} \alpha_i s^i $$

$$ f(A) = \sum_{i=0}^{\infty} \alpha_i A^i $$

Define $p(s)$ and $P(A)$ as follows

$$ \large p(s) = c_0 + c_1 s + c_2 s^2 + \cdots + c_{l-1} s^{l-1} $$

$$ \large P(A) = c_0 I + c_1 A + c_2 A^2 + \cdots + c_{l-1} A^{l-1} $$

Then we have the equality 

$$ \large f(A) = P(A) $$

where $P(A)$ is a polynomial of $A$.

_Case I: $A$ is diagonalizable_

Suppose

$ \large m(s) = (s - \lambda_1 ) (s - \lambda_2 ) \cdots (s - \lambda_{\sigma} ) $

$ l = \sigma $ , $ m_1 = m_2 = \cdots = m_{\sigma} = 1 $

$ \large f(A) = P(A) = c_0 I + c_1 A + c_2 A^2 + \cdots + c_{l-1} A^{l-1} $

$ Ae_i = \lambda_i e_i $

Let $e_i$ be the eigenvector of $A$ corresponding to $\lambda_i$, multiply both sides by $e_i$.

$ \sum_{n=0}^{l-1} \alpha_i A^n e_i = \sum_{n=0}^{l-1} c_n \lambda_i^n e_i $

$ \sum_{n=0}^{l-1} \alpha_i \lambda_i^n e_i = \sum_{n=0}^{l-1} c_n \lambda_i^n e_i $

$ \alpha_i \lambda_i^n = c_n \lambda_i^n $

$ \alpha_i = c_n $

$ \large f(A) = P(A) = \sum_{i=0}^{l-1} \alpha_i A^i = \sum_{i=0}^{l-1} c_i A^i $

$ \large f(\lambda_i) = P(\lambda_i) $

--------------------------------------------------------------------------------------------------------------
<ins>Example</ins>: $A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$ find $e^A$ and $log(A)$

<ins>Solution</ins>:

$ d(s) = (s - 3)(s - 1) $

$ \lambda_1 = 3 $, $ \lambda_2 = 1 $

$ m(s) = (s - 3)(s - 1) $, $l = 2 $

$ p(s) = c_0 + c_1 s $, and $ P(A) = c_0 I + c_1 A $

$ Ae_1 = 3e_1 $, $ Ae_2 = e_2 $

$ f(3) = p(3) \\
 f(1) = p(1) $  

$ f(3) = e^3 = c_0 + 3c_1 \\
 f(1) = \ e \ = c_0 + c_1 $

$ c_1 = \frac{e^3 - e}{2} \\
 c_0 = \frac{3e - e^3}{2} $

$ e^A = \frac{3e - e^3}{2} I + \frac{e^3 - e}{2} A $

$ e^A = \frac{3e - e^3}{2} \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} + \frac{e^3 - e}{2} \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} $

--------------------------------------------------------------------------------------------------------------
_Case II: $A$ is not diagonalizable_

Consider the following example. Let $A \in \mathbb{R}^3$ and $ m(s) = (s-\lambda_1)^2(s-\lambda_2) $.

$$ \large J = \begin{bmatrix} \lambda_1 & 1 & 0 \\ 0 & \lambda_1 & 0 \\ 0 & 0 & \lambda_2 \end{bmatrix} $$

$$ \sum m_i = 2 + 1 = 3 $$

$$ f(A) = P(A) = c_0 I + c_1 A + c_2 A^2 $$

$$ f(\lambda_1) = P(\lambda_1) \ \ \ f(\lambda_2) = P(\lambda_2) $$

These two equations are not enough to find $c_0,c_1,c_2$.

Consider the matrix $P$ that transforms $A$ into its Jordan canonical form $J$.

We know that $P^{-1} = P^*$ and $P^*AP = J$, and $P$ is in the form of $[e_1,f_1,e_2]$. Where $e_1$ and $e_2$ are the eigenvectors of $A$ corresponding to $\lambda_1$ and $\lambda_2$ respectively. $f_1$ is the generalized eigenvector of $A$ corresponding to $\lambda_1$.

$$ \large P = \begin{bmatrix} \vdots & \vdots & \vdots \\ e_1 & f_1 & e_2 \\ \vdots & \vdots & \vdots \end{bmatrix} $$

$$ \large \begin{bmatrix} \vdots & \vdots & \vdots \\ e_1 & f_1 & e_2 \\ \vdots & \vdots & \vdots \end{bmatrix} \begin{bmatrix} \lambda_1 & 1 & 0 \\ 0 & \lambda_1 & 0 \\ 0 & 0 & \lambda_2 \end{bmatrix} = A \begin{bmatrix} \vdots & \vdots & \vdots \\ e_1 & f_1 & e_2 \\ \vdots & \vdots & \vdots \end{bmatrix} $$



$$ \begin{align*} \large Af_1 \  & = \lambda_1 f_1 + e_1 \\
\large A^2f_1 & = \lambda_1 Af_1 + Ae_1 \\
\large & = \lambda_1^2 f_1 + \lambda_1 e_1 + \lambda_1 e_1 = \lambda_1^2 f_1 + 2 \lambda_1 e_1 \\
\large A^3f_1 & = \lambda_1^2 Af_1 + 2\lambda_1 Ae_1 = \lambda_1^3 f_1 + 3 \large \lambda_1^2 e_1 \\
& \ \ \  \vdots \\
\large A^kf_1 & = \lambda_1^k f_1 + k \lambda_1^{k-1} e_1 \\
\end{align*} $$

Return to the equation $f(A) = P(A)$.

$$ \large \sum_{i=0}^{l-1} \alpha_i A^i = \sum_{i=0}^{l-1} c_i A^i $$

Multiply both sides by $f_1$ from the right.

$$ \large \sum_{i=0}^{l-1} \alpha_i A^i f_1 = \sum_{i=0}^{l-1} c_i A^i f_1 $$

$$ \large \sum_{i=0}^{l-1} \alpha_i \lambda_1^i f_1 + \sum_{i=0}^{l-1} \alpha_i i \lambda_1^{i-1} e_1 = \sum_{i=0}^{l-1} c_i \lambda_1^i f_1 + \sum_{i=0}^{l-1} c_i i \lambda_1^{i-1} e_1 $$

$$ \large f(\lambda_1) f_1 + f'(\lambda_1) e_1 = P(\lambda_1) f_1 + P'(\lambda_1) e_1 $$

$$ \large f(\lambda_1) = P(\lambda_1) $$

$$ \large f'(\lambda_1) = P'(\lambda_1) $$

Which is the additional equation we need to find $c_0,c_1,c_2$.

--------------------------------------------------------------------------------------------------------------
_General Case_

Let $m(s) = (s-\lambda_1)^{m_1}(s-\lambda_2)^{m_2} \cdots (s-\lambda_{\sigma})^{m_{\sigma}}$. We have the following set of equations.

$$ \large f^{(t)}(\lambda_i) = P^{(t)}(\lambda_i) $$

where $t = 0,1,2,\cdots,m_i-1$ and $i = 1,2,\cdots,\sigma$. We have $\sum_{i=1}^{\sigma} m_i = l$ equations.

--------------------------------------------------------------------------------------------------------------
<ins>Example</ins>: $A = \begin{bmatrix} 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 & 1 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}$ Find $\sin{(\pi A)}$.

<ins>Solution</ins>:

$ m(s) = s^3(s-1)^2 $ and the order of the total minimal polynomial is $l = 5$.

$ p(s) = c_0 + c_1 s + c_2 s^2 + c_3 s^3 + c_4 s^4 $

$ p(A) = c_0 I + c_1 A + c_2 A^2 + c_3 A^3 + c_4 A^4 $

We need five equations to find $c_0,c_1,c_2,c_3,c_4$.

Starting with 

$$\begin{align*} f(s) &= \sin{(\pi s)} \\
f'(s) &= \pi \cos{(\pi s)} \\
f''(s) &= -\pi^2 \sin{(\pi s)} \end{align*} $$

Then 

$$ \begin{align*} p(s) &= c_0 + c_1 s + c_2 s^2 + c_3 s^3 + c_4 s^4 \\
p'(s) &= c_1 + 2c_2 s + 3c_3 s^2 + 4c_4 s^3 \\
p''(s) &= 2c_2 + 6c_3 s + 12c_4 s^2\end{align*} $$

For the first eigenvalue $\lambda_1 = 0$. We have $m_1 = 3$.
$$ \begin{align*} & f(\lambda_1) = p(\lambda_1) \\
& f'(\lambda_1) = p'(\lambda_1) \\
& f''(\lambda_1) = p''(\lambda_1) \end{align*}$$

$$ \begin{align*} & f(0) = p(0) \\
& f'(0) = p'(0) \\
& f''(0) = p''(0) \end{align*}$$

$$ \begin{align*} & \sin{(0)} = 0 = c_0 \\
& \pi \cos{(0)} = \pi = c_1 \\
& -\pi^2 \sin{(0)} = 0 = 2c_2  \end{align*}$$


For the second eigenvalue $\lambda_2 = 1$. We have $m_2 = 2$.

$$ \begin{align*} & f(\lambda_2) = p(\lambda_2) \\
& f'(\lambda_2) = p'(\lambda_2) \end{align*}$$

$$ \begin{align*} & \sin{(\pi)} = 0 = c_0 + c_1 + c_2 + c_3 + c_4 \\
& \pi \cos{(\pi)} = -\pi = c_1 + 2c_2 + 3c_3 + 4c_4 \end{align*}$$

$$ \large \begin{bmatrix} 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 & 1 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} c_0 \\ c_1 \\ c_2 \\ c_3 \\ c_4 \end{bmatrix} = \begin{bmatrix} 0 \\ \pi \\ 0 \\ -\pi \\ -\pi \end{bmatrix} $$
$$ \large \begin{bmatrix} c_0 \\ c_1 \\ c_2 \\ c_3 \\ c_4 \end{bmatrix} = \begin{bmatrix} 0 \\ \pi \\ 0 \\ -2\pi \\ \pi \end{bmatrix} $$

$$ \large p(s) = \pi s - 2\pi s^3 + \pi s^4 $$

$$ \large \sin{(\pi A)} = \pi A - 2\pi A^3 + \pi A^4 $$

> Remark: $f(A)$ does not exist when $f^{(t)}(\lambda_i)$ does not exist for some $t$ and $i$.

--------------------------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]