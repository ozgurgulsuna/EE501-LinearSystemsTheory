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



--------------------------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]