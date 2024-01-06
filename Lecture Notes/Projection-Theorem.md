## Hilbert Projection Theorem ##

Let $H$ be a Hilbert space ( inner product space that is complete with respect to the norm induced by the inner product) and $M$ be a finite dimensioal subspace of $H$. Then for any $x \in H$, there exists a unique $y \in M$ such that

$$\min_{m \in M} \|x-m\|$$

has a unique solution $y$. In other words "we can find a unique point in $M$ that is closest to $x$". If $m^*$ is the closest point to $x$ in $M$, then $x-m^* \perp M$.

**Proof:** See lecture notes.


> **Remark:** The proof stated that $m^* = x_1$ is the closest point to $M$. It can also be interpreted as the best approximation of $x$ choosen from the vectors in $M$. The $x_2$ term is the error in the approximation.

------------------------------------------------------------------------------------------
<ins>Example:</ins> Let $V=\mathbb{R}^2$ and $M = \text{span}\{[1,1]^T\}$. Find the best approximation of $x=[4,7]^T$ in $M$.

_<ins>Solution:</ins>_ We need to find $m^*$ such that $m^* = \alpha \begin{bmatrix} 1 \\ 1 \end{bmatrix}$ and $\|x-m^*\|$ is minimum.

$$(x-m^*) \perp M \implies <x-m^*, m> = 0 \quad \forall m \in M$$

$$<x-m^*, \begin{bmatrix} 1 \\ 1 \end{bmatrix}> = 0$$

$$\text{Replace $x$ and $m^*$ with their values.}$$

$$<\begin{bmatrix} 4-\alpha \\ 7-\alpha \end{bmatrix}, \begin{bmatrix} 1 \\ 1 \end{bmatrix}> = 0$$

$$\text{Recall that $<x,y> = x^Ty$.}$$

$$4-\alpha + 7-\alpha = 0$$

$$\alpha = \frac{11}{2}$$

$$m^* = \frac{11}{2} \begin{bmatrix} 1 \\ 1 \end{bmatrix}$$

------------------------------------------------------------------------------------------
<ins>Example:</ins> Let $x \in V$ and $M = \text{span}\{v_1, v_2\}$. Find the best approximation of $x$ in $M$.

_<ins>Solution:</ins>_ We need to find $m^*$ such that $m^* = \alpha_1 v_1 + \alpha_2 v_2$ that is in the span of $M$ and $\|x-m^*\|$ is minimum.

$$(x-m^*) \perp M \implies (x-m^*) \perp \text{both } v_1 \text{ and }v_2$$

$$<x-\alpha_1 v_1 - \alpha_2 v_2, v_1> = <x, v_1> - \alpha_1 <v_1, v_1> - \alpha_2 <v_2, v_1> = 0$$

$$<x-\alpha_1 v_1 - \alpha_2 v_2, v_2> = <x, v_2> - \alpha_1 <v_1, v_2> - \alpha_2 <v_2, v_2> = 0$$

$$\begin{bmatrix} <v_1, v_1> & <v_2, v_1> \\ <v_1, v_2> & <v_2, v_2> \end{bmatrix} \begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} <x, v_1> \\ <x, v_2> \end{bmatrix}$$

$$\begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} <v_1, v_1> & <v_2, v_1> \\ <v_1, v_2> & <v_2, v_2> \end{bmatrix}^{-1} \begin{bmatrix} <x, v_1> \\ <x, v_2> \end{bmatrix}$$

$$m^* = \alpha_1 v_1 + \alpha_2 v_2$$

------------------------------------------------------------------------------------------
<ins>Example:</ins> Let $V = \mathbb{R}^3$ and $M = \text{span}\{[1,1,1]^T, [1,0,1]^T\}$. Find the best approximation of $x=[4,7,2]^T$ in $M$.

_<ins>Solution:</ins>_ We need to find $m^*$ such that $m^* = \alpha_1 \begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix} + \alpha_2 \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix}$ that is in the span of $M$ and $\|x-m^*\|$ is minimum.

$$(x-m^*) \perp M \implies (x-m^*) \perp \text{both } v_1 \text{ and }v_2$$

$$\begin{bmatrix} <v_1, v_1> & <v_2, v_1> \\ <v_1, v_2> & <v_2, v_2> \end{bmatrix} \begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} <x, v_1> \\ <x, v_2> \end{bmatrix}$$

$$\text{Recall that $<x,y> = x^Ty$.}$$

$$\begin{bmatrix} 3 & 2 \\ 2 & 2 \end{bmatrix} \begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} 13 \\ 6 \end{bmatrix}$$

$$\begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} 3 & 2 \\ 2 & 2 \end{bmatrix}^{-1} \begin{bmatrix} 13 \\ 6 \end{bmatrix}$$

$$\begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} 1 & -1 \\ -1 & 3/2 \end{bmatrix} \begin{bmatrix} 13 \\ 6 \end{bmatrix}$$

$$\begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} 7 \\ -4 \end{bmatrix}$$

$$m^* = \alpha_1 v_1 + \alpha_2 v_2 = 7 \begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix} - 4 \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix} = \begin{bmatrix} 3 \\ 7 \\ 3 \end{bmatrix}$$

------------------------------------------------------------------------------------------


#### Solution of Linear Equations ####

Consider the linear equation as,

$$ Ax = B $$

$$ \text{where $A \in \mathbb{C}^{m \times n}$, $B \in \mathbb{C}^{m \times 1}$ and $x \in \mathbb{C}^{n \times 1}$ is unknown.} $$

a\) **solution exists**: when $b \in \text{R}(A)$  
b\) **solution is unique**: when $N(A) = \{0\}$






-----
#EE501 - [[Linear Systems Theory]] at [[METU]]