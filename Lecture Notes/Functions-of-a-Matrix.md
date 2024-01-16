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


_Case II: $A$ is not diagonalizable_

--------------------------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]