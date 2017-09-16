The cubical singular complex $KX$, or $S^\square X$, of a topological space $X$ has an additional structure of compositions. 

Let $(m) = (m_1, \ldots\, , m_n)$ be an $n$-tuple of positive integers
and

$$\phi_{(m)} : I^n \rightarrow [0, m_1] \times \cdots \times [0,
m_n]$$ 

be the map $(x_1 , \ldots \, , x_n) \mapsto (m_1 x_1, \ldots  \, ,
m_n x_n).$ Then a _subdivision of type $(m)$_  of a map $\alpha : I^n
\rightarrow X$ is a factorisation $\alpha = \alpha' \circ
\phi_{(m)}$; its  _parts_ are the cubes $\alpha_{(r)}$ where
$(r) = (r_1, \ldots , r_n)$ is an $n$-tuple of integers with $1
\leq r_i \leq m_i$, $i = 1, \ldots , n,$ and where
$\alpha_{(r)} : I^n \rightarrow X$ is given by

$$(x_1, \ldots , x_n) \mapsto
\alpha'(x_1 + r_1 - 1, \ldots , x_n + r_n - 1).$$

We then say that $\alpha$ is the _composite_  of the cubes $\alpha_{(r)}$ and write
$\alpha = [\alpha_{(r)}]$. The _domain_ of $\alpha_{(r)}$ is
then the set $\{(x_1,\ldots,x_n) \in I^n : r_i-1 \leq x_i
\leqslant r_i, 1 \leq i \leq n\}$.

The composite is _in direction_ $j$  if $m_j$ is the only
$m_i \gt 1,$ and we then write $\alpha = [\alpha_1 , \ldots\, ,
\alpha_m{_j} ]_j;$ the composite is _in the directions_ $j$,
$k$ $(j \neq k)$  if $m_j$, $m_k$ are the only $m_i \gt 1,$ and we then write

$$\alpha = [ \alpha_{rs}]_{j,k} $$

for $r = 1 , \ldots , m_j$ and $s = 1, \ldots \,, m_k.$

These definitions and notations are useful for showing how the singular cubical complex allows expression for _algebraic inverses to subdivision_. 


A _cubical set with connections and compositions and inverses_ is a cubical
set $K$ with connections in which each $K_n$ has $n$ partial
compositions $+_i$ and $n$ unary operations $-_i\; i =
1,2,\ldots,n)$ satisfying the following axioms.

 If $a,b \in K_n$, then $a+_i b$ is defined if and only if  $ \partial^+_i a=\partial^-_i  b
$, and then for $\alpha=\pm$:

$$ \begin{cases} \partial^-_i (a+_i b) = \partial^-_i a & \\
         \partial^+_i (a+_i b) = \partial^+_i b & \end{cases}$$

$$
 \partial^\alpha_i (a +_j b) = \begin{cases} \partial^\alpha_i a+_{j-1}\partial^\alpha_i b &(i \lt j) \\
         \partial^\alpha_i a+_j \partial^\alpha_i b& (i \gt j), \end{cases}
          $$

 If $a \in K_n$, then $-_i a$ is defined and

$$
\begin{cases}\partial^-_i (-_i a)=\partial^+_i a & \\ \partial^+_i(-_i a)=\partial^-_i a &
\end{cases} $$

$$
 \partial^\alpha_i(-_j a) = \begin{cases} -_{j-1}\partial^\alpha_i a & (i\lt j) \\
                     -_{j}\partial^\alpha_i a & (i \gt j)
\end{cases}
$$

$$      \varepsilon_i(a+_j b) = \begin{cases}
      \varepsilon_i a +_{j+1} \varepsilon_i b & (i \leq j) \\
      \varepsilon_i a +_j\varepsilon_i b & (i \gt j) \end{cases}$$ 

$$      \varepsilon_i (-_j b) =
                  \begin{cases}
     -_{j+1} \varepsilon_ia & (i \leq j) \\
     -_j \varepsilon_ia & (i \gt j) \end{cases}$$
     

$$    \Gamma^\alpha _i (a+_j b) = \begin{cases}
      \Gamma_i^\alpha a +_{j+1} \Gamma_i^\alpha b & (i \lt j) \\
      \Gamma_i^\alpha  a +_j\Gamma_i\alpha  b & (i \lt j) \end{cases}$$

$$    \Gamma_j^+(a+_j b)= (\Gamma_j^+ a +_{j} \varepsilon_j a) +_{j+1}
    (\varepsilon_{j+1} a +_{j} \Gamma_j^+ b)$$ 


$$    \Gamma_j^-(a+_j b)= (\Gamma_j^- a +_{j} \varepsilon_{j+1}  b) +_{j+1}
    (\varepsilon_{j} b +_{j} \Gamma_j^- b)$$

These last two equations are  called the _transport laws_ and the right hand sides are also written respectively 

$$ \begin{bmatrix} \Gamma^+_j a & \varepsilon_j a \\
\varepsilon_{j+1} a & \Gamma^+_j b  \end{bmatrix} \quad _{j+1}\!\downarrow ^{\textstyle\to ^j} $$


$$ \begin{bmatrix} \Gamma^-_j a & \varepsilon_{j+1} b \\
\varepsilon_{j} b & \Gamma^-_j b  \end{bmatrix} \quad _{j+1}\!\downarrow ^{\textstyle\to ^j} $$



We have for $i \ne j$ and whenever both sides are defined:

$$
   (a+_i b) +_j (c+_i d) = (a+_j c) +_i (b+_j d)
$$

These relations are called the _interchange laws_. Further:

$
-_i (a+_j b) = (-_i a) +_j (-_i b)$    and  $ -_i (-_j a) =
-_j (-_i a)$  if $i \ne j$  

$-_j(a+_j b)  = (-_j  b)+_j(-_j a)$  and  $ -_j (-_j a) =a$.
   



 It is easily verified that the singular cubical set $KX$ of a
space $X$  satisfies these axioms if $+_j , -_j$  are defined by

$$
   (a+_j b)(t_1 ,t_2 ,\ldots \, ,t_n ) = \begin{cases}
   a(t_1 ,\ldots \, , t_{j-1},2t_j,t_{j+1} ,\ldots, ,t_n) &(t_j \leq
   \frac{1}{2})\\
   b(t_1 ,\ldots \, , t_{j-1},2t_j-1,t_{j+1} ,\ldots \, ,t_n) &(t_j \geq
   \frac{1}{2})\\
   \end{cases}
 $$

whenever  $ \partial^+_j a=\partial^-_j b$; and

$$
(-_j a)(t_1 ,t_2 ,\ldots,t_n ) = a(t_1 ,\ldots,
t_{j-1},1-t_j,t_{j+1} ,\ldots,t_n).
$$




##References## 

* R. Brown and P.J. Higgins, The algebra of cubes, _J. Pure
Appl. Alg.+, 21 (1981), 233--260.


* F. Al-Agl, R. Brown and R. Steiner, Multiple categories: the equivalence   between a globular and cubical approach, _Advances in Mathematics_, 170,   (2002), 71--118.