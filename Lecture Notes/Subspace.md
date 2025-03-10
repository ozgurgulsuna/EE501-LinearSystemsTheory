###### Linear Spaces ######
### Subspaces ###

**Definition**: Let $V$ be a vector space. A subset $W$ of $V$ is called a [[subspace]] of $V$ iff $W$ is a vector space with respect to the operations of $V$, that is,

- (S1) $w_1 + w_2 \in W$   $\forall w_1, w_2 \in W$ (closure under addition)
- (S2) $c w \in W$   $\forall c \in F$ and $\forall w \in W$ (closure under scalar multiplication)

> **Remark**: $W$ is a subspace of $V$ iff $W$ is nonempty and $W$ is closed under addition and scalar multiplication. All other axioms are inherited from the original vector space $V$.

------------------------------------------------------------------------------
<ins>Example</ins>: linear space $V = \mathbb{R}^2$, subspace $W = [\alpha \space 0]^T \in \mathbb{R}^2 : \alpha \in \mathbb{R}$  
<ins>Solution</ins>: Let  $w_1 = [\alpha_1 \space 0]^T$ and $w_2 = [\alpha_2 \space 0]^T$ and $c \in \mathbb{R}$, 
- (S1) $w_1 = \begin{bmatrix} \alpha_1 \\ 0 \end{bmatrix}$ and $w_2 = \begin{bmatrix} \alpha_2 \\ 0 \end{bmatrix}$ be two arbitrary elements of $W$. Then $w_1 + w_2 = \begin{bmatrix} \alpha_1 + \alpha_2 \\ 0 \end{bmatrix} \in W$
- (S2) $c w1 = \begin{bmatrix} c \alpha_1 \\ 0 \end{bmatrix} \in W$ for all $c \in \mathbb{R}$.
Hence $W$ is a subspace of $V$.

------------------------------------------------------------------------------
<ins>Example</ins>: linear space $V = \mathbb{R}^2$, subspace $W = [\alpha \space 1]^T \in \mathbb{R}^2 : \alpha \in \mathbb{R}$  
<ins>Solution</ins>: Let  $w_1 = [\alpha_1 \space 1]^T$ and $w_2 = [\alpha_2 \space 1]^T$
- (S1) $w_1 = \begin{bmatrix} \alpha_1 \\ 1 \end{bmatrix}$ and $w_2 = \begin{bmatrix} \alpha_2 \\ 1 \end{bmatrix}$ be two arbitrary elements of $W$. Then $w_1 + w_2 = \begin{bmatrix} \alpha_1 + \alpha_2 \\ 2 \end{bmatrix} \notin W$

------------------------------------------------------------------------------
> **Remark**: In $\mathbb{R}^2$, a subspace is a line through the origin. Any line through the origin is a subspace of $\mathbb{R}^2$.


In function spaces, an example can be given as follows:  
<ins>Example</ins>: linear space $V =$ set of all real-valued functions of a real variable $t\rightarrow f(t)$;  
subspace $W_1 =$ set of all continuous functions [+]  
subspace $W_2 =$ set of all constant functions  [+]  
subspace $W_3 =$ set of all functions periodic with $\pi$ [+]
subspace $W_4 =$ set of all functions which are discontinuous at $t=1$ [-]  

> **Remark**: 0 vector is a subspace of any vector space, even subspace of itself, and it is the smallest subspace.

[+] $W_1, W_2, W_3$ are subspaces of $V$  
[-]  $W_4$ is not a subspace of $V$  

------------------------------------------------------------------------------
<ins>Example</ins>:  Show that $Y+Z$ is a linear subspace of $X$, if $Y$ and $Z$ are also linear subspaces of $X$.  
<ins>Proof:</ins> Let $w_1+w_2 \in W$, with  
$w_1=y_1+z_1$ where $y_1 \in Y, \ z_1 \in Z$  
$w_2=y_2+z_2$ where $y_2 \in Y, \ z_2 \in Z$  
then  
$$\begin{align*}
w_1+w_2=y_1+z_1+y_2+z_2 &=(y_1+y_2)+(z_1+z_2) \\
y_1+y_2 \in Y , z_1+z_2 \in Z &\Rightarrow w_1+w_2 \in Y+Z
\end{align*}$$  
Shows that $Y+Z$ is closed under addition. (lemma 1)  

Let $c w_1 \in W$, $\forall c \in F$
$$\begin{align*}
c w_1=c(y_1+z_1) &=(cy_1)+(cz_1) \\
cy_1 \in Y , cz_1 \in Z &\Rightarrow cw_1 \in Y+Z
\end{align*}$$  
Shows that $Y+Z$ is closed under scalar multiplication. (lemma 2)
Hence $Y+Z$ is a linear subspace of $X$.  

------------------------------------------------------------------------------
<ins>Example</ins>:  If $Y$ and $Z$ are subspaces of X, then $Y \cap Z$ is a subspace of $X$.  
$~$<ins>Proof:</ins>
- $0 \in Y$, $0 \in Z$ then by definition $0 \in Y \cap Z$  
- for $u,w \in Y$ and  $u,w \in Z \implies u,w \in Y \cap Z$  

now we need to show that $u+w \in Y \cap Z$ (closure under addition)
- starting  $u \in Y, w \in Y \implies u+w \in Y$
- similarly $u \in Z, w \in Z \implies u+w \in Z$
    - hence $u+w \in Y \cap Z$

now we need to show that $cu \in Y \cap Z$ (closure under scalar multiplication)
- starting  $u \in Y \implies cu \in Y$, $\forall c \in F$
- similarly $u \in Z \implies cu \in Z$, $\forall c \in F$
    - hence $cu \in Y \cap Z$

Hence $Y \cap Z$ is a subspace of $X$.

------------------------------------------------------------------------------
<ins>Example</ins>: For $Y$ and $Z$ are subspaces of $X$, show that whether $Y \cup Z$ is a subspace of $X$ or not.  
$~$<ins>Proof:</ins>
Prove by contradiction.
- Assume $Y \cup Z$ is a subspace of $X$. Then $Y \cup Z$ is closed under addition and scalar multiplication.
- Let $Y =\{(y,0):y \in \mathbb{R}\}$ and $Z =\{(0,z):z \in \mathbb{R}\}$.
- Then $u_1=(1,0) \in Y$ and $u_2=(0,1) \in Z$.
- $u_1+u_2=(1,1) \notin Y \cup Z$.

------------------------------------------------------------------------------
<ins>Example</ins>: Is $\mathbb{R}^2$ a subspace of complex vector space $\mathbb{C}^2$?  
$~$<ins>Proof:</ins> Note that we consider complex vector space, so if $x \in \mathbb{R}^2$ then $x \in \mathbb{C}^2$.  
- $i \in \mathbb{C}$ and $x \in \mathbb{R}^2$ then $ix \in \mathbb{R}^2$.
    - $i(1,1) =(i,i) \notin \mathbb{R^2}$

Hence $\mathbb{R}^2$ is not a subspace of $\mathbb{C}^2$.



$~$

###### Subspaces ######
### Sums of Subspaces ###

**Definition**: Suppose $W_1,...,W_m$ are subspaces of a vector space $V$. The sum of $W_1,...,W_m$ is the set of all possible sums of elements of $W_1,...,W_m$:

$$W_1 + ... + W_m = \{w_1 + ... + w_m : w_i \in W_i, i = 1,...,m\}$$

> **Remark**: $W_1 + ... + W_m$ is the smallest subspace of $V$ containing $W_1,...,W_m$.

### Direct Sums ###
**Definition**: Suppose $W_1,...,W_m$ are subspaces of a vector space $V$. The sum $W_1 + ... + W_m$ is called a direct sum if each element of $W_1 + ... + W_m$ can be written in one and only one way as a sum $w_1 + ... + w_m$ with $w_i \in W_i$.

> **Remark**: if $W_1+...+W_m$ is a direct sum, then $W_1 \oplus ... \oplus W_m$ is used to denote the direct sum.

**Example:** Suppose $U_j$ is a subspace of $F^n$ of those vectors whose $j$th component is zero. As $U_2 = \{(0,x,..., 0) \in F^n : x \in F\}$, Then.

$$U_1 \oplus ... \oplus U_n= F^n$$

**Condition for Direct Sum**: Suppose $W_1,...,W_m$ are subspaces of a vector space $V$. Then $W_1 + ... + W_m$ is a direct sum iff the only way to write 0 as a sum $w_1 + ... + w_m$ with $w_i \in W_i$ is by taking $w_1 = ... = w_m = 0$. In other words, Suppose $W$ and $U$ are subspaces of a vector space $V$. Then $W \oplus U$ is a direct sum iff $W \cap U = \{0\}$.  

**Proof**: Proving the statements with iff is equivalent to proving the statements separately, in both directions.

$$W \oplus U \text{ is a direct sum} \iff W \cap U = \{0\}$$