###### Range and Null Space ######
## Range and Null Space ##

**Definition**: Let $T:V \rightarrow W$ be a linear transformation. The set of all vectors $y \in W$ such that $y = T(x)$ for some $x \in V$ is called the **range** of $T$ and denoted by $\mathcal{R}(T)$.

**Definition**: Let $T:V \rightarrow W$ be a linear transformation. The set of all vectors $x \in V$ such that $T(x) = 0$ is called the **null space** of $T$ and denoted by $\mathcal{N}(T)$.

Let $T:V \rightarrow W$ be a linear transformation. Let $dim(V) = n$ and $dim(W) = m$. Recall that,  

- $\mathcal{R}(T): \text{Range space of } T, \mathcal{R}(T) \subseteq W, dim(\mathcal{R}(T)) = dim(col(T))$
- $\mathcal{N}(T): \text{Null space of } T, \mathcal{N}(T) \subseteq V, dim(\mathcal{N}(T)) = dim(null(T))$

------------------------------------------------------------------------------------------
<ins>Theorem</ins>: $dim(\mathcal{R}(T)) + dim(\mathcal{N}(T)) = dim(V)$  

<ins>Proof</ins>: Let $B = \{v_1, v_2, \dots, v_k\}$ be a basis for $\mathcal{N}(T)$. Extend $B$ to a basis $B' = \{v_1, v_2, \dots, v_k, v_{k+1}, \dots, v_n\}$ for $V$. Then $B'$ is a basis for $V$ and $B'' = \{T(v_{k+1}), T(v_{k+2}), \dots, T(v_n)\}$ is a basis for $\mathcal{R}(T)$. Hence $dim(\mathcal{R}(T)) = n - k = dim(V) - dim(\mathcal{N}(T))$ $\blacksquare$


**Definition**: Let $T:V \rightarrow W$ be a linear transformation. The **rank** of $T$ is defined as $rank(T) = dim(\mathcal{R}(T))$.

> **Remark**: $rank(T)$ is equal to the number of linearly independent columns of $T$.  

> **Remark**: In general, a basis for $\mathcal{R}(T)$ and $\mathcal{N}(T)$  can be found by finding a basis for the column space and null space of the matrix representation of $T$ with respect to some basis for $V$ and $W$.

<ins>Eample</ins>: $V = \mathbb{R}^{2x2}$, $W = V$, Find a basis for $\mathcal{R}(\mathcal{A})$  
$$\begin{align*}
B &= \begin{Bmatrix}\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 \\ 1 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix} \end{Bmatrix} \\
C &= \begin{Bmatrix}\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix},\begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix},\begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix},\begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix} \end{Bmatrix} \\
\mathcal{A}(x) &= Sx + x S^\top = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}x + x\begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}^\top \\
A &= \begin{bmatrix} 1 & 1 & 1 & -1 \\ 0 & 0 & 0 & 0 \\ -1 & 1 & 1 & 1 \\ 0 & -1 & -1 & 0 \end{bmatrix} \\ 
\end{align*}$$

<ins>Solution</ins>: Start with finding a basis for $\mathcal{R}(\mathcal{A})$  
$$\begin{align*}
\mathcal{R}(\mathcal{A}) &:= \{ w \in W  \ |  \  \ \exist v \in V , \ \mathcal{A}v = w \} \\
\mathcal{R}(A) &:= \{ y \in \mathbb{R}^4  \ | \  \ \exist x \in \mathbb{R}^4 , \ Ax = y \} \\
\end{align*}$$

- Start with finding a basis for $\mathcal{R}(A)$
- Convert the vectors in the basis into matrices using the basis $C$.

Finding a basis for $\mathcal{R}(A)$ is equivalent to finding a basis for the column space of $A$. The basis for the column space of $A$ can be found by reducing $A$ to independent columns by elementary column operations and then taking the non-zero columns of the reduced matrix.

$$\begin{align*}  
A &= \begin{bmatrix} 1 & 1 & 1 & -1 \\ 0 & 0 & 0 & 0 \\ -1 & 1 & 1 & 1 \\ 0 & -1 & -1 & 0 \end{bmatrix} \sim \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ -1 & 2 & 0 & 0 \\ 0 & -1 & 0 & 0 \end{bmatrix} \\
\end{align*}$$

$$\begin{align*}
\text{basis for  } \mathcal{R}(A) &= \begin{Bmatrix}\begin{bmatrix} 1 \\ 0 \\ -1 \\ 0 \end{bmatrix},\begin{bmatrix} 0 \\ 0 \\ 2 \\ -1 \end{bmatrix}\end{Bmatrix} \\

\end{align*}$$

$$\begin{align*}
\begin{bmatrix} 1 \\ 0 \\ -1 \\ 0 \end{bmatrix} = [w_1]_C \implies w_1 &= 1c_1 + 0c_2 + (-1)c_3 + 0c_4 = c_1 - c_3 \\
 &= \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} - \begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix} = \begin{bmatrix} 0 & -1 \\ -1 & 0 \end{bmatrix} \\
\end{align*}$$

$$\begin{align*}
\begin{bmatrix} 0 \\ 0 \\ 2 \\ -1 \end{bmatrix} = [w_2]_C \implies w_2 &= 0c_1 + 0c_2 + 2c_3 + (-1)c_4 = 2c_3 - c_4 \\
 &= \begin{bmatrix} 2 & 2 \\ 2 & 0 \end{bmatrix} - \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix} \\
\end{align*}$$

$$\begin{align*}
\text{basis for  } \mathcal{R}(\mathcal{A}) &= \begin{Bmatrix}\begin{bmatrix} 0 & -1 \\ -1 & 0 \end{bmatrix},\begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix}\end{Bmatrix} \\
dim(\mathcal{R}(A)) &= 2 = \text{rank}(A) \\
\end{align*}$$


1. $A$ is a $4x4$ matrix, $dim(\mathcal{R}(A)) = 4 - dim(\mathcal{N}(A))$
2. $dim(\mathcal{N}(A)) = 2$ since $rank(A) = 2$
3. $dim(\mathcal{R}(A)) = 4 - 2 = 2$
4. $dim(\mathcal{R}(\mathcal{A})) = 2$


Now, we need to find a basis for $\mathcal{N}(\mathcal{A})$.  

$$\begin{align*}
\mathcal{N}(\mathcal{A}) &:= \{ v \in V  \ |  \  \ \mathcal{A}v = 0 \} \\
\mathcal{N}(A) &:= \{ x \in \mathbb{R}^4  \ | \  \ Ax = 0_W \} \\
\end{align*}$$

- Start with finding a basis for $\mathcal{N}(A)$
- Convert the vectors in the basis into matrices using the basis $B$.

Finding a basis for $\mathcal{N}(A)$ is equivalent to finding a basis for the null space of $A$. The basis for the null space of $A$ can be found by reducing $A$ by elementary row operations and then equating the $\bar Ax =0$.

$$\begin{align*}
A &= \begin{bmatrix} 1 & 1 & 1 & -1 \\ 0 & 0 & 0 & 0 \\ -1 & 1 & 1 & 1 \\ 0 & -1 & -1 & 0 \end{bmatrix} \sim \begin{bmatrix} 1 & 0 & 0 & -1 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} = \bar A \\
\end{align*}$$

$$\begin{align*}
\bar Ax = 0 \\
\begin{bmatrix} 1 & 0 & 0 & -1 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} &= \begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix} \\
x_1 - x_4 = 0  \implies x_1 &= x_4 \\
x_2 + x_3 = 0 \implies x_2 &= -x_3 \\
\end{align*}$$

$$\begin{align*}
\begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} &= \begin{bmatrix} x_1 \\ x_2 \\ -x_2 \\ x_1 \end{bmatrix} = x_1\begin{bmatrix} 1 \\ 0 \\ 0 \\ 1 \end{bmatrix} + x_2\begin{bmatrix} 0 \\ 1 \\ -1 \\ 0 \end{bmatrix} \\
\end{align*}$$

$$\begin{align*}
\text{basis for  } \mathcal{N}(A) &= \begin{Bmatrix}\begin{bmatrix} 1 \\ 0 \\ 0 \\ 1 \end{bmatrix},\begin{bmatrix} 0 \\ 1 \\ -1 \\ 0 \end{bmatrix}\end{Bmatrix} \\
\end{align*}$$

$$\begin{align*}
\begin{bmatrix} 1 \\ 0 \\ 0 \\ 1 \end{bmatrix} = [v_1]_B \implies v_1 &= 1b_1 + 0b_2 + 0b_3 + 1b_4 = b_1 + b_4 \\
 &= \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} + \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \\
\end{align*}$$

$$\begin{align*}
\begin{bmatrix} 0 \\ 1 \\ -1 \\ 0 \end{bmatrix} = [v_2]_B \implies v_2 &= 0b_1 + 1b_2 + (-1)b_3 + 0b_4 = b_2 - b_3 \\
 &= \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} - \begin{bmatrix} 0 & 0 \\ 1 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix} \\
\end{align*}$$

$$\begin{align*}
\text{basis for  } \mathcal{N}(\mathcal{A}) &= \begin{Bmatrix}\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix},\begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}\end{Bmatrix} \\
dim(\mathcal{N}(A)) &= 2 = \text{nullity}(A) \\
\end{align*}$$








**Definition**: Let $T:V \rightarrow W$ be a linear transformation. The **nullity** of $T$ is defined as $nullity(T) = dim(\mathcal{N}(T))$.



------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]