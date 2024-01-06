## Hilbert Projection Theorem ##

Let $H$ be a Hilbert space ( inner product space that is complete with respect to the norm induced by the inner product) and $M$ be a finite dimensioal subspace of $H$. Then for any $x \in H$, there exists a unique $y \in M$ such that

$$\min_{m \in M} \|x-m\|$$

has a unique solution $y$. In other words "we can find a unique point in $M$ that is closest to $x$". If $m^*$ is the closest point to $x$ in $M$, then $x-m^* \perp M$.

**Proof:** See lecture notes.


> **Remark:** The proof stated that $m^* = x_1$ is the closest point to $M$. It can also be interpreted as the best approximation of $x$ choosen from the vectors in $M$. The $x_2$ term is the error in the approximation.

-----------------------------------------------------------------------------------
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

-----------------------------------------------------------------------------------
<ins>Example:</ins> Let $x \in V$ and $M = \text{span}\{v_1, v_2\}$. Find the best approximation of $x$ in $M$.

_<ins>Solution:</ins>_ We need to find $m^*$ such that $m^* = \alpha_1 v_1 + \alpha_2 v_2$ that is in the span of $M$ and $\|x-m^*\|$ is minimum.

$$(x-m^*) \perp M \implies (x-m^*) \perp \text{both } v_1 \text{ and }v_2$$

$$<x-\alpha_1 v_1 - \alpha_2 v_2, v_1> = <x, v_1> - \alpha_1 <v_1, v_1> - \alpha_2 <v_2, v_1> = 0$$

$$<x-\alpha_1 v_1 - \alpha_2 v_2, v_2> = <x, v_2> - \alpha_1 <v_1, v_2> - \alpha_2 <v_2, v_2> = 0$$

$$\begin{bmatrix} <v_1, v_1> & <v_2, v_1> \\ <v_1, v_2> & <v_2, v_2> \end{bmatrix} \begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} <x, v_1> \\ <x, v_2> \end{bmatrix}$$

$$\begin{bmatrix} \alpha_1 \\ \alpha_2 \end{bmatrix} = \begin{bmatrix} <v_1, v_1> & <v_2, v_1> \\ <v_1, v_2> & <v_2, v_2> \end{bmatrix}^{-1} \begin{bmatrix} <x, v_1> \\ <x, v_2> \end{bmatrix}$$

$$m^* = \alpha_1 v_1 + \alpha_2 v_2$$

-----------------------------------------------------------------------------------
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

-----------------------------------------------------------------------------------
<ins>Example:</ins> Let $H$ be the space of square integrable functions on $[-\pi , \pi ]$ with inner product $<f,g> = \int_{-\pi}^{\pi} f(t)\bar{g(t)}dt$. Let $M$ be the subspace of $H$, $M = \text{span}\{e^{jkt}/\sqrt{2\pi}\}$, $k \text{ from } -N \text{ to } N$. Note that dimension of $M$ is $2N+1$.  

$$<f_n, f_m> = \int_{-\pi}^{\pi} \frac{e^{jnt}}{\sqrt{2\pi}} \frac{e^{-jmt}}{\sqrt{2\pi}} dt = \frac{1}{2\pi} \int_{-\pi}^{\pi} e^{j(n-m)t} dt$$

$$\text{If $n \neq m$, then } \frac{1}{2\pi} \int_{-\pi}^{\pi} e^{j(n-m)t} dt = \frac{1}{2\pi} \frac{e^{j(n-m)t}}{j(n-m)} \Big|_{-\pi}^{\pi} = 0$$

$$\text{If $n = m$, then } \frac{1}{2\pi} \int_{-\pi}^{\pi} e^{j(n-m)t} dt = \frac{1}{2\pi} \int_{-\pi}^{\pi} 1 dt = 1$$

$$\text{Therefore, } <f_n, f_m> = \begin{cases} 1 & \text{if $n = m$} \\ 0 & \text{if $n \neq m$} \end{cases}$$

Now, let $g \in H$ be an arbitrary function. Then $g = g_1 + g_2$ where $g_1 \in M$ and $g_2 \in M^{\perp}$. We need to find $g_1$ such that $\|g-g_1\|$ is minimum.

$$ g_1 = \sum_{k=-N}^{N} \alpha_k \frac{e^{jkt}}{\sqrt{2\pi}} \text{ where } \alpha_k = <g, f_k> = \int_{-\pi}^{\pi} g(t) \frac{e^{-jkt}}{\sqrt{2\pi}} dt$$

$$ \alpha_k = \int_{-\pi}^{\pi} g(t) \frac{e^{-jkt}}{\sqrt{2\pi}} dt$$

$$ g_1 = \sum_{k=-N}^{N} \int_{-\pi}^{\pi} g(t) \frac{e^{-jkt}}{\sqrt{2\pi}} \frac{e^{jkt}}{\sqrt{2\pi}} dt = \sum_{k=-N}^{N} \int_{-\pi}^{\pi} g(t) \frac{1}{2\pi} dt = \int_{-\pi}^{\pi} g(t) dt$$

-----------------------------------------------------------------------------------
<ins>Example:</ins> Find the orthagonal projection of the vector $\begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}$ onto the subspace $M = \text{span}\{\begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix}, \begin{bmatrix} 1 \\ -1 \\ 1 \end{bmatrix}\}$.

_<ins>Solution:</ins>_ We know that the projection matrix is $P = B(B^TB)^{-1}B^T$ where $B$ is the matrix whose columns are the basis vectors of $M$. Therefore,

$$B = \begin{bmatrix} 1 & 1 \\ 1 & -1 \\ 1 & 1 \end{bmatrix}$$

$$B^TB = \begin{bmatrix} 3 & 1 \\ 1 & 3 \end{bmatrix}$$

$$P = \begin{bmatrix} 1 & 1 \\ 1 & -1 \\ 1 & 1 \end{bmatrix} \begin{bmatrix} 3 & 1 \\ 1 & 3 \end{bmatrix}^{-1} \begin{bmatrix} 1 & 1 & 1 \\ 1 & -1 & 1 \end{bmatrix}$$

$$P = \begin{bmatrix} 1 & 1 \\ 1 & -1 \\ 1 & 1 \end{bmatrix} \begin{bmatrix} 3/8 & -1/8 \\ -1/8 & 3/8 \end{bmatrix} \begin{bmatrix} 1 & 1 & 1 \\ 1 & -1 & 1 \end{bmatrix}$$

$$P = \begin{bmatrix} 1/2 & 0 & 1/2 \\ 0 & 1 & 0 \\ 1/2 & 0 & 1/2 \end{bmatrix}$$

$$P \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} = \begin{bmatrix} 1/2 \\ 0 \\ 1/2 \end{bmatrix}$$

-----
#EE501 - [[Linear Systems Theory]] at [[METU]]