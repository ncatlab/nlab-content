> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***





\linebreak



## Via cohomology of complex projective space
 {#ViaCellularCohomology}

The following expands out a proof indicated by [Bruner 2009](#Bruner2009), of the fundamental theorem of algebra via the [[integral cohomology|integral]] [[cohomology ring]] of [[complex projective space]] $\mathbb{C}P^{n-1}$:

> [Bruner 2009](#Bruner2009): "I just noticed the following proof that the complex numbers $\mathbb{C}$ are algebraically closed, and wonder if anyone has seen it in print anywhere. \linebreak
> An algebraic extension of C is a unital division algebra over $\mathbb{C}$, say of dimension $n$, so induces 
> $$ \mathbb{C}P^{n-1} \times \mathbb{C}P^{n-1} \longrightarrow \mathbb{C}P^{n-1}$$
> satisfying 
> $$ y \mapsto 1 \textstyle{\otimes} y + y \textstyle{\otimes} 1 $$
> in second integral cohomology.  Since $y^n = 0$, we must have $n=1$."

Recall here that the [[integral cohomology]] of [[complex projective space]] $\mathbb{CP}^{n-1}$ is (see [there](complex+projective+space#Cohomology)): 

$$
  H^i\big(
    \mathbb{CP}^{n-1}; 
    \mathbb{Z}
  \big) 
    \cong 
  \mathbb{Z}^{a_i}
  \mathrlap{\,,}
  \;\text{where}\;
  a_i 
    =
  \left\{ 
  \begin{array}{ll}
    1 & \text{if}\; i \in \{ 2j \vert 0 \leq j \leq n-1 \}
    \\
    0 & \text{otherwise}
  \end{array}
  \right.
$$

on which the [[cup product]] induces a ring [[isomorphism]] 

$$
  H^*\big(
    \mathbb{CP}^n, \mathbb{Z}
  \big) 
    \simeq  
  \mathbb{Z}[c] / c^n \mathbb{Z}[c]
  \mathrlap{\,,}
$$

where $c$ denotes the integral [[first Chern class]] (cf. [here](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace)).

\begin{theorem} 
Let $K$ be a [[finite dimensional vector space]] over $\mathbb{C}$ equipped 

1. (unit) a map $\eta : \ast \rightarrow K$ 

1. (product) a [[linear map]] $\mu \colon K \otimes_{\mathbb{C}} K \rightarrow K$

satisfying for $a,b \in K$:

1. ([[unitality]]) $\mu\big(\eta(1),a\big) = a = \mu\big(a,\eta(1)\big)$, 

1. (no [[zero-divisors]]) if $\mu (a \otimes b) = 0$, then $a = 0$ or $b = 0$.

(We do not *need* to require [[associativity]]!)

Then $K$ is [[isomorphism|isomorphic]] to $\mathbb{C}$ itself as a [[complex vector space|$\mathbb{C}$-vector space]], i.e. [[dimension of a vector space|$\text{dim}(K)$]] $= 1$.
\end{theorem}

Note that we obtain such a nonassociative $\mathbb{C}$-algebra as the [[splitting field]] of any complex [[irreducible  polynomial]].

\begin{proof}
The assumed absence of [[zero divisors]] implies that multiplication restricts to the [[complement]] of zero, and [[bilinear map|bilinearity]] of the multiplication then implies that it respects [[complex lines]] and hence descends to a [[continuous map]] between ([[product space|products]] of) [[complex projective space]]

$$
  [ \mu|_{ \mathbb{C}^n \setminus \{0\} } ] 
    \ : \ 
  \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1} 
    \longrightarrow 
  \mathbb{CP}^{n-1}
  \mathrlap{\,.}
$$

Recall that $c \in H^2(\mathbb{CP}^{n-1})$ is the generator of the [[cohomology ring]] $H^* ( \mathbb{CP}^{n-1} )$. We have:

$$
  H^2\big(
    \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1}; 
    \mathbb{Z}
  \big) 
   \cong 
  H^2\big(
    \mathbb{CP}^{n-1}; \mathbb{Z}
  \big) 
   \oplus 
  H^2\big(
    \mathbb{CP}^{n-1}; \mathbb{Z}
  \big) 
  \mathrlap{\,.}
$$

Therefore there must be $a, b \in \mathbb{Z}$ such that pullback of the generator along the product map is

$$
  H^2(\mu,\mathbb{Z})(c) 
    = 
  a \cdot (1 \textstyle{\otimes} c) 
    + 
  b \cdot (c \textstyle{\otimes} 1)
  \mathrlap{\,.}
$$

But these coefficients must satisfy the two equations which are the image in degree-2 [[integral cohomology]] of the two [[unit laws]] (the first assumed property on $K$):

$$ 
  H^2 \left( 
    \mu 
      \circ 
    \left( 
      \eta \times Id_{\mathbb{CP}^{n-1}} 
    \right) , 
    \mathbb{Z} 
  \right)   
  =  
  Id_{H^2 \left( \mathbb{CP}^{n-1} , \mathbb{Z} \right) }
  =   
  H^2 \left( 
    \mu 
    \circ 
    \left( 
      Id_{\mathbb{CP}^{n-1}} \times \eta 
    \right) , 
    \mathbb{Z} 
  \right)
  \mathrlap{\,.}
$$

This implies that:

$$
  a = 1, 
  \;\text{and}\;
  b = 1
  \mathrlap{\,.}
$$

There is an [[isomorphism]] of [[Hopf algebras]] in [[integral cohomology]] of 

$$
  \big(
    \mathbb{Z}[x]/x^n\mathbb{Z}[x]
  \big) 
    \otimes_{\mathbb{Z}}
  \big(
    \mathbb{Z}[x]/x^n\mathbb{Z}[x]
  \big)  
    \cong  
  H^\bullet\big(
   \mathbb{CP}^{n-1};
   \mathbb{Z}
  \big) 
    \otimes_{\mathbb{Z}} 
  H^\bullet\big(
    \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)  
    \cong  
  H^\bullet\big(
    \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)
  \mathrlap{\,.}
$$

But $H^\bullet(\mu;\mathbb{Z})$ is a [[ring homomorphism]], so

$$
  H^\bullet(\mu;\mathbb{Z})(c^n) 
    = 
  (1 \textstyle{\otimes} c + c \textstyle{\otimes} 1)^n 
    = 
  \sum_{i = 0}^n 
  {\binom{n}{i}}\, 
    (1 \otimes c)^i \cdot (c \otimes 1)^{n-i} 
    = 
  \sum_{i = 0}^n 
  {\binom{n}{i}}\, 
    c^{n-i} \otimes c^{i}
$$

as elements of the commutative Hopf algebra

$$
  H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z}) 
    \otimes_{\mathbb{Z}} 
  H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z})  
   \;\cong\; 
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right) 
    \otimes_{\mathbb{Z}}
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right)
  \mathrlap{\,.}
$$

The left-hand side is $0$.

The right hand side is 

$$ 
   \sum_{i = 1}^{n-1} 
   {\binom{n}{i}}\, 
     c^{n-i} 
       \otimes 
     c^{i} 
  \mathrlap{\,.}
$$

By way of [[proof by contradiction|contradiction]], suppose that $n = \text{dim}(K)$ is greater than $1$. In this case, each of the terms $c^i \otimes c^{n-i}$ is nonzero for $0 \lt i \lt n$, and their sum is as well.

This implies that 

$$
  \sum_{i= 1}^{n-1} 
    {\binom{n}{i}}\,  
     c^{n-i} 
       \otimes 
     c^{i}
$$

is not zero, which contradicts that $c^n$ is zero using the above equation.

This implies $n = 1$ and hence the claim.
\end{proof}

{#TwoLemmas} The following two theorems about the power-series algebra $\mathbb{R}[[x]]$ over $\mathbb{R}$ and the Hopf-algebra structure on $\mathbb{R}[[x]]$ apply to a modified form of the above proof which uses cellular cohomology with coefficients in $\mathbb{R}$ instead of cellular cohomology with coefficients in $\mathbb{Z}$:

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
