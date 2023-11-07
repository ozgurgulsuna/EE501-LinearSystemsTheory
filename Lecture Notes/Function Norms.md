#EE501
## Function Norms ##

**Definition**: Function [[norm]]s are norm definitions applied to [[function space]]s. Function spaces are vector spaces whose elements are functions. The most common function spaces are $L^p$ spaces.  
$$V = \{f(.) | f: [0,1] \rightarrow \mathbb{R} s.t. \int_0^1 |f(x)|^p dx < \infty \space \space \space 1 \leq p < \infty\}$$  
We can define norms on $V$ as follows:  
$$\|f\|_p := \left( \int_0^1 |f(x)|^p dx \right)^{1/p}$$  
where $p \geq 1$.  

Specific Cases
- $\|f\|_1 = \int_0^1 |f(x)| dx$   $L_1-norm$
- $\|f\|_2 = \left( \int_0^1 |f(x)|^2 dx \right)^{1/2}$   $L_2-norm$
- $\|f\|_{\infty} = \sup_{x \in [0,1]} |f(x)|$   $L_{\infty}-norm$




-----
#EE501 - [[Linear Systems Theory]] at [[METU]]