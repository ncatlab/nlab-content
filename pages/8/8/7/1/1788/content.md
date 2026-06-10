> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***





\linebreak




$$
  J 
    \;=\;
    \sum_i f_i \theta_i 
      + 
    \sum_j g_j d \theta_j 
    f_i, g_j \in C^\infty(X)
  \,.
$$


\begin{xymatrix}
Q B \ar[d] \ar[r] & Q A \sqcup Q B \ar[d] \ar[r] & A \sqcup Q B \ar[d]\cr
  B        \ar[r] & Q A \sqcup   B        \ar[r] & A \sqcup   B       \cr
\end{xymatrix}


_________



\begin{theorem} (ideals of a power series ring over the field of real numbers) let $I \subseteq \mathbb{R}[[x]]$ be a nonzero ideal of the algebra of power-series over $\mathbb{R}[[x]]$. There is $n \in \mathbb{N}$ such that $I = x^n \cdot \mathbb{R}[[x]]$.
\end{theorem}

\begin{proof} let $f = \sum_{i =0}^{\infty} a_i x^i$ be a nonzero element of $I$ chosen to satisfy 

* $a_n = 1$ where $n = \mathrm{min} \{ i \in \mathbb{N} : a_i \neq 0 \}$. 

* of all nonzero $g \in I$, $\mathrm{min} \left\{   \mathrm{min} \{ i \in \mathbb{N} : b_i \neq 0 \} : b_i \in \mathbb{R}, \sum_{i = 0}^{\infty} b_i x^i \in I  \right\}$

Such an element exists since, if $g = \sum_{i=0}^{\infty} b_i x^i$ is any nonzero element of $I$ satisfying the second property, then we can set

$$ 
f = \sum_{i = 0}^{\infty} b_{\mathrm{min} \{ j \in \mathbb{N} : b_j \neq 0 \} }^{-1} \cdot b_i \cdot x^i 
$$

Define a sequence $f_k = \sum_{i =0}^{\infty} a_{k,i} x^i$ by induction on $k \in \mathbb{N}$ satisfying the inductive hypothesis that $a_{k,i} = 0$ for $i \in \mathbb{N}$ such that

* $i \leq n + k$

* $i \neq n$

For the case in which $k = 0$, set $f_0 = f$. 

For the inductive case, suppose that for some $k \in \mathbb{N}$ we have defined $f_k = \sum_{i = 0}^{\infty} a_{k,i} x^i$ satisfying $a_{k,i} = 0$ for $i \in \mathbb{N}$ such that

* $i \leq n + k$

* $i \neq n$

$$
f_{k+1} = \sum_{i = 0}^{\infty} a_{k+1,i} x^i = f_k ( 1 - a_{k,n+k+1} x^{k} )
$$

Then $a_{k+1,i} = 0$ for $i \in \mathbb{N}$ such that 

* $i \leq n + k + 1$

* $i \neq n$

This concludes the construction of the elements 

$$ f_{k} = \sum_{i = 1}^{\infty} a_{k,i} x^i \in \mathbb{R}[[x]] $$

Next consider the sequence

$$
g_m = \sum_{j = 0}^{m} b_{m,j} x^j = \Pi_{k = 0}^{m} ( 1 - a_{k,n+k+1} x^{k} ) \in \mathbb{R}[[x]]
$$

and consider that 

$$
b_{m+\ell, j} = b_{m, j}
$$

for $j \leq m+1$. This identity implies that 

$$
 g = \Pi_{k =0}^{\infty} (1 - a_{k,n+k+1} x^k )
$$

is well defined.

For each $m \in \mathbb{N}$, $f \cdot g_m$ agrees with $x^n$ through degree $n + m$. The coefficients of $f \cdot g$ and $x^n$ agree in every degree, so $fg = x^n$
\end{proof}

\begin{theorem} let $H = \mathbb{R}[[x]]$ be the Hopf-algebra over $\mathbb{R}$ with multiplication defined by
$$
\mu \left( \sum_{i= 0}^{\infty} a_i x^i \otimes \sum_{i=0}^{\infty} b_i x^i \right)
=
\sum_{i=0}^{\infty} \sum_{i_1 + i_2 = i, i_1, i_2 \in \mathbb{N} } a_{i_1} b_{i_2} x^{i} 
$$
and comultiplication defined by setting
$$ 
\Delta \left( x \right) = x \otimes 1 + 1 \otimes x
$$ 
The Hopf-ideals of $H$ are $\{ 0 \} , x \cdot \mathbb{R}[[x]]$, and $\mathbb{R}[[x]]$.
\end{theorem}

\begin{proof} let $I$ be a nonzero ideal of $\mathbb{R}[[x]]$. By the previous theorem, $I = x^n \cdot \mathbb{R}[[x]]$ for some $n \in \mathbb{N}$. 

$$
\Delta(x^n) = \Delta (x)^n = (x \otimes 1 + 1 \otimes x)^n = \sum_{ i = 0 }^n { \binom{n}{i} } x^i \otimes x^{n - i} \in (x^n \cdot \mathbb{R}[[x]]) \otimes \mathbb{R}[[x]] + \mathbb{R}[[x]] \otimes (x^n \cdot \mathbb{R}[[x]])
$$

For each $(i,j) \in \mathbb{N} \times \mathbb{N}$ such that $i + j = n$, 

$$x^i \otimes x^j \in (x^n \cdot \mathbb{R}[[x]]) \otimes \mathbb{R}[[x]] + \mathbb{R}[[x]] \otimes (x^n \cdot \mathbb{R}[[x]])$$

We can express $(x^n \cdot \mathbb{R}[[x]]) \otimes \mathbb{R}[[x]] + \mathbb{R}[[x]] \otimes (x^n \cdot \mathbb{R}[[x]])$ as a span of an $\mathbb{R}$-basis:

$$
(x^n \cdot \mathbb{R}[[x]]) \otimes \mathbb{R}[[x]] + \mathbb{R}[[x]] \otimes (x^n \cdot \mathbb{R}[[x]])
=
\mathrm{span} \left\{ x^i \otimes x^j : n \leq i \text{ or } n \leq j \right\}
$$

so for each $(i,j) \in \mathbb{N} \times \mathbb{N}$ such that $i + j = n$, either $n \leq i$ or $n \leq j$.

We can conclude from this fact that $n = 0$ or $n = 1$.
\end{proof}

