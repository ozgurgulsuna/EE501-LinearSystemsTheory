###### Linear Spaces ######
## Fields ##

**Definition**: A [[field]] is a set $F$ of [[scalar]]s with two operations, addition and multiplication, such that the following axioms hold:

**Addition**  

- (A1) $a+b=b+a$ for all $a,b \in F$ (commutativity of addition)  
- (A2) $(a+b)+c=a+(b+c)$ for all $a,b,c \in F$ (associativity of addition)  
- (A3) There exists an element $0 \in F$ such that $a+0=a$ for all $a \in F$ (existence of additive identity)
This element is commonly denoted by $0_F$.  
- (A4) For every $a \in F$ there exists an element $-a \in F$ such that $a+(-a)=0_F$ (existence of additive inverse)
This element is commonly denoted by $(-a)$.

**Multiplication**

- (M1) $a \cdot b=b \cdot a$ for all $a,b \in F$ (commutativity of multiplication)  
- (M2) $(a \cdot b) \cdot c = a \cdot (b \cdot c)$ for all $a,b,c \in F$ (associativity of multiplication)  
- (M3) There exists an element in $F$ such that $a \cdot 1_F = a$ for all $a \in F$ (existence of multiplicative identity)  
- (M4) For every $a \in F$ except $0_F$ there exists an element $a^{-1} \in F$ such that $a \cdot a^{-1} = 1_F$ (existence of multiplicative inverse)

**Distributivity**

- (D1) $a \cdot (b+c) = a \cdot b + a \cdot c$ for all $a,b,c \in F$ (distributivity of multiplication over addition)

At least two elements must exist in a field, the additive identity $0_F$ and multiplicative identity $1_F$.

Field examples include $\mathbb{R}$, $\mathbb{C}$, $\mathbb{Q}$, $\mathbb{Z}_p$ where $p$ is a prime number. $\mathbb{R}$ are the real numbers, $\mathbb{C}$ are the [[complex numbers]], $\mathbb{Q}$ are the rational numbers, $\mathbb{Z}_p$ are the integers modulo $p$.

In a sense, what I understand from the fields are, mathematical concepts that are used to define the operations on the elements of the vector spaces.  

###### Linear Spaces ######
## $\mathbb{F}^n$ ##

**Definition**: The set of all [[list]]s of length $n$ with elements from a [[field]] $\mathbb{F}$ is denoted by $\mathbb{F}^n$.

$$\mathbb{F}^n = \{(x_1, x_2, \ldots, x_n) \mid x_i \in \mathbb{F}, i=1,2,\ldots,n\}$$

Addition and scalar multiplication are defined as follows:
$$(x_1, x_2, \ldots, x_n) + (y_1, y_2, \ldots, y_n) = (x_1+y_1, x_2+y_2, \ldots, x_n+y_n)$$
$$\alpha(x_1, x_2, \ldots, x_n) = (\alpha x_1, \alpha x_2, \ldots, \alpha x_n)$$


-----
#EE501 - [[Linear Systems Theory]] at [[METU]]