###### Linear Spaces ######
## Convergence ##

**Definition**: Let $(V,F)$ be a vector space. A sequence of vectors $\{x_n\}_{n=1}^{\infty}$ in $V$ is said to converge to a vector $x \in V$ if for every $\epsilon > 0$ there exists an integer $N$ such that $\|x_n - x\| < \epsilon$ for all $n \geq N$. In this case we write $x_n \rightarrow x$ as $n \rightarrow \infty$.

> **Remark**: The sequence is said to be **convergent** if it converges to some vector $x \in V$. Otherwise, it is said to be **divergent**.

<ins>**Example**</ins>: Let $V=R \ \ \|v\|=v$, consider the sequence

$$\left\{ (\frac{1}{2})^n \right\}_{n=1}^{\infty}$$

Proove that this sequence converges to $0$ as $n \rightarrow \infty$.

$~$<ins>**Proof**</ins>:  DO IT LATER

**Definition**: Let $(V,F, \|.\|)$ be a normed space. A sequence of vectors $\{x_n\}_{n=1}^{\infty}$ in $V$ is said to be a **Cauchy sequence** if for every $\epsilon > 0$ there exists an integer $N$ such that $\|x_n - x_m\| < \epsilon$ for all $n,m \geq N$.

- **Proof**: $\|x_n - x_m\| < \epsilon$ for all $n,m \geq N$ implies $\|x_n - x\| < \epsilon$ for all $n \geq N$.
------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]