###### EE501 - HW1 ######
## Problem Set ##

**Q1.** Let $F$ be a field. For an arbitrary element $a \in F$ prove the following.
1. The additive inverse $−a$ is unique.
2. The multiplicative inverse $a^{−1}$ is unique given that $a \neq 0$.  

------------------------------------------------------------------------------------------
**_Solution_**:  
1.  Let $v \in F$ is an arbitrary element in $F$. Assume that $v$ has two additive inverses with $w_1,w_2 \in F$.Then,  
   $v+w_1 = 0 \ \rightarrow w_1 = -v$  
   $v+w_2 = 0 \ \rightarrow w_2 = -v$  
   Therefore, $w_1 = w_2 = -v$ for any $w_1,w_2 \in F$ and the additive inverse is unique.

> **Remark**: For any $v$ in $F$, there exists a unique additive inverse that is, $-v$ in $F$.

2. Let $v \in F$ is an arbitrary element in $F$. $\exists \ w \in F$ s.t. $vw = 1_F$ (multiplicative inverse).  
   Let $w_1,w_2 \in F$ be two multiplicative inverses of $v$. Then,  
   $vw_1 = 1_F$ and $w_1 = \dfrac{1}{v}$  
   similarly,  
   $vw_2 = 1_F$ and $w_2 = \dfrac{1}{v}$  
   Therefore, $w_1 = w_2 = \dfrac{1}{v}$ for any $w_1,w_2 \in F$ and the multiplicative inverse is unique.

------------------------------------------------------------------------------------------
**Q2.** Let $F = \mathbb{R}_{>0}$ (the set of strictly positive real numbers). We define addition and multiplication, respectively, as  

$$ a \oplus b = ab $$
$$ a \odot b = e^{ln(a)ln(b)}$$  

   for $a,b \in F$

1. Find the additive identity $0_F$ and the multiplicative identity $1_F$.
2. Find the additive inverse $-a$ and the multiplicative inverse $a^{-1}$ for an arbitrary $a \in F$.
3. Prove that $F$ is a field.

------------------------------------------------------------------------------------------
**_Solution_**: First notice that, $a \oplus b = ab = e^{ln(a)+ln(b)}$  
1. For $a \in F = \mathbb{R}_{>0}, \ \ \ \exists \ 0_F \in F \ \text{s.t.}$  
    $a \oplus 0_F = a0_F = a \implies 0_F = 1_{\mathbb{R}}$  
    Similarly,
    For $a \in F = \mathbb{R}_{>0}, \ \ \ \exists \ 1_F \in F \ \text{s.t.}$  
    $a \odot 1_F = e^{ln(a)ln(1_F)} = a \implies 1_F = e$  

2. 



------------------------------------------------------------------------------------------
**Q3.** Let $(V, F)$ be a linear space. Given $a \in F$ and $v \in V$ prove the following.

1.  $a0_V = 0_V$
2.  $-0_V = 0_V$
3.  $0_Fv = 0_V$
4.  $(-1_F)v = -v$



------------------------------------------------------------------------------------------
**_Solution_**:
1. $a0_V = a(0_V + 0_V) = a0_V + a0_V$  
   $a0_V + (-a0_V) = a0_V + a0_V + (-a0_V)$  
   $0_V = a0_V \ \blacksquare$  

A more rigorous proof would be as follows.

1. $a0_V = a(v+(-v))$  
   $a0_V = av + a(-v)$  
   $a0_V = av + (-a)v$  
   $a0_V = (a + (-a))v$  
   $a0_V = 0_Fv$  
   $a0_V = 0_V \ \blacksquare$  

This solution takes into account of two other lemma to be proven.  
       **Lemma 1**: $-v = -1_fv$  
       **Lemma 2**: $0_Fv = 0_V$

2. $-0_V = -0_V + 0_V$  
   $-0_V = -0_V + (0_V + 0_V)$  
   $-0_V = (-0_V + 0_V) + 0_V$  
   $-0_V = 0_V + 0_V$  
   $-0_V = 0_V \ \blacksquare$  

3. $0_Fv = (0_F + 0_F)v$  
   $0_Fv = 0_Fv + 0_Fv$  
   $0_Fv + (-0_Fv) = 0_Fv + 0_Fv + (-0_Fv)$  
   $0_V = 0_Fv \ \blacksquare$  

another solution could be as follows.

3. $0_Fv = 0_Fv$  
   $0_Fv + v = 0_Fv + v$  
   $0_Fv + v = 0_Fv + 1_Fv$  
   $0_Fv + v = (0_F + 1_F)v$  
   $0_Fv + v = 1_Fv$  
   $0_Fv + v = v$  
   $0_Fv = 0_V  \ \blacksquare$   

4. $(-1_F)v = (-1_F)v + 0_V$  
   $(-1_F)v = (-1_F)v + (v + (-v))$  
   $(-1_F)v = ((-1_F)v + (1_F)v) + (-v)$  
   $(-1_F)v = ((-1_F + 1_F)v) + (-v)$  
   $(-1_F)v = 0_Fv + (-v)$  
   $(-1_F)v = 0_V + (-v)$  
   $(-1_F)v = -v \ \blacksquare$  


------------------------------------------------------------------------------------------
#EE501 - [[Linear Systems Theory]] at [[METU]]