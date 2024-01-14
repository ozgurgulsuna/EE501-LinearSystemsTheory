###### Minimal Polynomial ######
## Jordan Chains ##

>**<center>Let A be an nxn matrix and Ā be its Jordan canonical form.</center>**
> * $ \bar A = B^{-1}AB \text{,  where B is invertible and composed of the basis vectors for the } N(A-\lambda_iI)^{m_i}$
> * $ \text{rank}(A) = \text{rank}(B A) = \text{rank}( A B) = \text{rank}(\bar A)$
> * $ \text{dim}(N(A-\lambda_iI)) = \text{dim}(N(\bar A - \lambda_iI))$

$ A \in \mathbb{C}^{n \times n} \\
\bar A = J = B^{-1}AB \\
\mathbb{C}^n = N(A-\lambda_1I)^{m_1} \oplus \cdots \oplus N(A-\lambda_kI)^{m_k} \\
\ \ \ \ \ \ \text{We look for basis vectors for } N((A - \lambda_iI)^{m_i}) \\
B = \begin{bmatrix} B_1 & B_2 & \cdots & B_n \end{bmatrix} \\
B_i = \begin{bmatrix} b_i^2 & b_i^3 & \cdots & b_i^{r_i} \end{bmatrix} \text{ where } b_i, \cdots, b_i^{r_i} \text{ have to be basis vectors for } N((A-\lambda_iI)^{m_i})$

Let $M_i := A - \lambda_iI$ , and let's choose a vector x such that $x \in N(M_i^j)$ or $M_i^jx = 0$ , but $x \notin N(M_i^{j-1})$

Now consider the chain of vectors $x, M_ix, M_i^2x, \cdots, M_i^{j-1}x$ , which is linearly independent. We can see this by contradiction. Suppose that the chain is linearly dependent. Then there exists a vector $M_i^kx$ such that $M_i^kx = \sum_{l=0}^{k-1} c_lM_i^lx$ , where $c_l \in \mathbb{C}$ . But then $M_i^kx = 0$ , which is a contradiction. Thus, the chain is linearly independent.

$$ \{ M_i^{m_i-1}x, M_i^{m_i-2}x, \cdots, M_ix, x \} \text{ is linearly independent} $$

<center>

```
┌──────────────────────────────────┬──────────┐
│                                  │  N(Σᵢᵐ)  │
│                       - x        └──────────┤
│      ┌───────────────────────────┬──────────┤
│      │                           │ N(Σᵢᵐ⁻¹) │
│      │               - Σᵢx       └──────────┤
│      │      ┌────────────────────┬──────────┤
│      │      │                    │ N(Σᵢ²)   │
│      │      │       - Σᵢᴹᶦ⁻²     └──────────┤
│      │      │    ┌───────────────┬──────────┤
│      │      │    │               │ N(Σᵢ)    │
│      │      │    │               └──────────┤
│      │      │    │ - Σᵢᴹᶦ⁻¹                 │
└──────┴──────┴────┴──────────────────────────┘
```

</center>

--------------------------------------------------------------------------------------------------------------
<ins>Example</ins>: Find the Jordan canonical form of $A = \begin{bmatrix} 1 & 1 & -1 \\ -1 & 3 & 2 \\ 0 & 0 & 1 \end{bmatrix}$

<ins>Solution</ins>:

$ d(s) = \text{det}(sI - A) = (s-1)[(s-3)(s-1)+1] = (s-2)^2(s-1) $

$ \lambda_1 = 2 \text{, } \lambda_2 = 1 $

$\Sigma_1 \ = \ \ A-2I \ \ = \begin{bmatrix} -1 & 1 & -1 \\ -1 & 1 & 2 \\ 0 & 0 & -1 \end{bmatrix}$
$ \text{ dim }N ( \Sigma_1) = 3-2 = 1 \neq r_1 = 2$

$ \Sigma_1^2 = (A-2I)^2 =  \begin{bmatrix} -1 & 1 & -1 \\ -1 & 1 & 2 \\ 0 & 0 & -1 \end{bmatrix} \begin{bmatrix} -1 & 1 & -1 \\ -1 & 1 & 2 \\ 0 & 0 & -1 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 4 \\ 0 & 0 & 1 \\ 0 & 0 & 1 \end{bmatrix} \text{ dim }N(\Sigma_1^2) = 3-1 = 2 = r_1$

No need to check $\Sigma_2$ because $r_2 = 1$

$ m(s) = (s-2)^2(s-1) = d(s) $

From the minimal polynomial, we can see that the Jordan canonical form will have a 2x2 block for $\lambda_1 = 2$ and a 1x1 block for $\lambda_2 = 1$

$ \bar A = J = \begin{bmatrix} 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix} \rightarrow \ P J = A P $

Now we will construct the chain of vectors, which will be used to construct the basis vectors.

$ x \in N(\Sigma_1^2) \text{ but } x \notin N(\Sigma_1) $

$ \Sigma_1^2x = 0 \rightarrow \begin{bmatrix} 0 & 0 & 4 \\ 0 & 0 & 1 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \rightarrow x_3 = 0$

$ \Sigma_1x \neq 0 \rightarrow \begin{bmatrix} -1 & 1 & -1 \\ -1 & 1 & 2 \\ 0 & 0 & -1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ 0 \end{bmatrix} \neq \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \rightarrow x_1 \neq x_2 $

Select $x = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}$ such that $x \in N(\Sigma_1^2) \text{ but } x \notin N(\Sigma_1)$

The chain of vectors for $\lambda_1 = 2$ is

$ \Big \{ \ \Sigma_1x \ , \ x  \ \Big \} = \Bigg  \{ \begin{bmatrix} -1 \\ -1 \\ 0 \end{bmatrix}, \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}  \Bigg \} $

```
┌──────────────────────────────────┬──────────┐
│                                  │ N(Σ₁²)   │
│                     - x          └──────────┤
│                  ┌───────────────┬──────────┤
│                  │               │ N(Σ₁)    │
│                  │               └──────────┤
│                  │ - Σ₁x                    │
└──────────────────┴──────────────────────────┘
```

Now we will construct the chain of vectors for $\lambda_2 = 1$

$ \Sigma_2 = A - I = \begin{bmatrix} 0 & 1 & -1 \\ -1 & 2 & 2 \\ 0 & 0 & 0 \end{bmatrix} $
$ \text{ dim }N(\Sigma_2) = 3-2 = 1 = r_2 $

$ y \in N(\Sigma_2) $

$ \Sigma_2y = 0 \rightarrow \begin{bmatrix} 0 & 1 & -1 \\ -1 & 2 & 2 \\ 0 & 0 & 0 \end{bmatrix} \begin{bmatrix} y_1 \\ y_2 \\ y_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \rightarrow y = \begin{bmatrix} 4 \\ 1 \\ 1 \end{bmatrix} $

The chain of vectors for $\lambda_2 = 1$ is

$ \Big \{y  \Big \} = \Bigg  \{\begin{bmatrix} 4 \\ 1 \\ 1 \end{bmatrix}  \Bigg \} $

```
┌──────────────────────────────────┬──────────┐
│                                  │ N(Σ₂)    │
│                                  └──────────┤
│                                  - y        │
└─────────────────────────────────────────────┘
```

Now we will construct the change of basis matrix $P$, or $B$ in the general case.

$ P = \begin{bmatrix} \ \ \Sigma_1x \ \ \ \  \vert & \ x & \vert \ \ \ \ \ y \ \ \end{bmatrix} = \begin{bmatrix} -1 & 1 & 4 \\ -1 & 0 & 1 \\ 0 & 0 & 1 \end{bmatrix} $

$ J = P^{-1}AP \ = \  \begin{bmatrix} -1 & 1 & 4 \\ -1 & 0 & 1 \\ 0 & 0 & 1 \end{bmatrix}^{-1} \begin{bmatrix} 1 & 1 & -1 \\ -1 & 3 & 2 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} -1 & 1 & 4 \\ -1 & 0 & 1 \\ 0 & 0 & 1 \end{bmatrix} = \begin{bmatrix} 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix} $

$ A P = P \bar A  \implies \begin{bmatrix} 1 & 1 & -1 \\ -1 & 3 & 2 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} -1 & 1 & 4 \\ -1 & 1 & 1 \\ 0 & 0 & 1 \end{bmatrix} = \begin{bmatrix} -1 & 1 & 4 \\ -1 & 1 & 1 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix} $

--------------------------------------------------------------------------------------------------------------

### Special Case 1. ###



