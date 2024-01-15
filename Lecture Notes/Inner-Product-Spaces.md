## [Inner Product Spaces] ##

**Definition**: Let $(V,F)$ be a vector space. An [[inner product]] is a map of the form $\langle\cdot,\cdot\rangle : V \times V \rightarrow F$ such that for all $x,y,z \in V$ and $c \in F$ the following axioms hold:

(P1) $\langle x,y \rangle = \overline{\langle y,x \rangle}$ (conjugate symmetry)

(P2) a. $\langle x+y,z \rangle = \langle x,z \rangle + \langle y,z \rangle$ (linearity in the first argument) 
      b. $\langle cx,y \rangle = c\langle x,y \rangle$ (homogeneity in the first argument)
 
(P3) $\langle x,x \rangle \geq 0$ and $\langle x,x\rangle = 0$ iff $x=0_v$ (positive definiteness)

















fill missing parts

**Theorem**: $\textit{"Cauchy-Schwarz Inequality"}$ Let $(V,F)$ be a vector space with an inner product $\langle\cdot,\cdot\rangle$. Then for all $x,y \in V$ the following inequality holds:

$$|\langle x,y \rangle|^2 \leq \langle x,x \rangle \langle y,y \rangle$$

**Proof**: Let $x,y \in V$ and $c \in F$.

1. $$\large\begin{align*} 0 & \leq \langle x-cy,x-cy \rangle \\
& = \langle x,x \rangle - \langle x,cy \rangle - \langle cy,x \rangle + \langle cy,cy \rangle \\
& = \langle x,x \rangle - \overline{c}\langle x,y \rangle - c\langle y,x \rangle + |c|^2\langle y,y \rangle \\
& = \langle x,x \rangle - \overline{c}\langle x,y \rangle - c\overline{\langle x,y \rangle} + |c|^2\langle y,y \rangle \\
& = \langle x,x \rangle - 2Re(c\langle x,y \rangle) + |c|^2\langle y,y \rangle \\
\end{align*}$$









-----
#EE501 - [[Linear Systems Theory]] at [[METU]]