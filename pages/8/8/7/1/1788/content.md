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

There is an [[isomorphism]] of [commutative algebras](https://ncatlab.org/nlab/show/commutative+algebra) of

$$
  \big(
    \mathbb{Z}[c]/c^n\mathbb{Z}[c]
  \big) 
    \otimes_{\mathbb{Z}}
  \big(
    \mathbb{Z}[c]/c^n\mathbb{Z}[c]
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

Where $H^\bullet(-; \mathbb{Z})$ is the [[integral cohomology]] of a topological space.

$H^\bullet(\mu;\mathbb{Z})$ is in fact a [[ring homomorphism]], hence we have

$$
\begin{aligned}
 0 = &  H^{\bullet}(\mu; \mathbb{Z})(c^n) \\
  = &  (1 \otimes c + c \otimes 1)^n \\
  = &  \sum_{i=0}^{n} \binom{n}{i} (1 \otimes c)^i (c \otimes 1)^{n-i} \\
  = &  \sum_{i=0}^{n} \binom{n}{i} c^{n-i} \otimes c^{i} \\
  = &  \sum_{0 \lt i \lt n} \binom{n}{i} c^{n-i} \otimes c^{i}
\end{aligned}
$$

As elements of the tensor product
 
$$
  H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z}) 
    \otimes_{\mathbb{Z}} 
  H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z})  
   \;\cong\; 
  \left( 
    \mathbb{Z}[[c]]/c^n \mathbb{Z}[[c]] 
  \right) 
    \otimes_{\mathbb{Z}}
  \left( 
    \mathbb{Z}[[c]]/c^n \mathbb{Z}[[c]]
  \right)
  \mathrlap{\,.}
$$

of the Hopf-algebra $H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z}) \cong \mathbb{Z}[[c]]/c^n \mathbb{Z}[[c]]$ with itself. 

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

{#TwoLemmas} The above proof can be modified to pertain to a fact about the cellular or singular [[cohomology]] of $\mathbb{C}P^{\infty}$ with coefficients in $\mathbb{R}$ of $H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R})$. As an $\mathbb{R}$-algebra, there is an isomorphism

$$
H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R}) \cong \mathbb{R}[[c]]
$$

There is a comultiplication on $H^{\bullet}(\mathbb{C}P^{\infty} ; \mathbb{R})$ which is related to the [complex orientation](https://ncatlab.org/nlab/show/complex+oriented+cohomology+theory#DefInTermsOfGeneralizedFirstChernClass) on the [Eilenberg-Maclane spectrum](https://ncatlab.org/nlab/show/Eilenberg-Mac+Lane+spectrum) $H\mathbb{R}$. More precisely, there is a map of $\mathbb{R}$-algebras

$$
\Delta : H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R}) \rightarrow H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R}) {\hat{\otimes}}_{\mathbb{R}} H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R}) 
$$

which is the unique map of $\mathbb{R}$-algebras such that 

$$
\Delta(x) = c \otimes 1 + 1 \otimes c 
$$

When $\mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]]$ is identified with $\mathbb{R}[[x,y]]$, this is the additive formal group law on $\mathbb{R}$.

Then we have the following facts:

* $H^{\bullet} ( \mathbb{C}P^n ; \mathbb{R}) \cong \mathbb{R}[[c]] / c^n \mathbb{R}[[c]]$ as an $\mathbb{R}$-algebra

* Any continuous binary operation on $\mathbb{C}P^{n}$ with a unit (satisfying the left and right unit identities) induces a quotient of the $\mathbb{R}$-algebra $\mathbb{R}[[c]]$ which commutes with the comultiplication in the sense that the following diagram commutes

\begin{xymatrix}
\mathbb{R}[[c]] \ar[d] \ar[r] &  \mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]] \ar[d]  \cr
 \mathbb{R}[[c]] / c^n \mathbb{R}[[c]]        \ar[r] & ( \mathbb{R}[[c]]/c^n \mathbb{R}[[c]]) \hat{\otimes} (\mathbb{R}[[c]]/c^n \mathbb{R}[[c]])         \cr
\end{xymatrix}

The ideals of the [power-series ring](https://ncatlab.org/nlab/show/power+series#is_a_principal_ideal_domain_given_r_is_a_field)  $\mathbb{R}[[c]]$ are entirely of the form $ c^n \cdot \mathbb{R}[[c]]$.

\begin{theorem} let $H = \mathbb{R}[[c]]$ be the $\mathbb{R}$-algebra defined above with a $\mathbb{R}$ with multiplication 
$$
\mu : \mathbb{R}[[c]]  \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]] \rightarrow \mathbb{R}[[c]]
$$
defined by
$$
\mu \left( \sum_{i= 0}^{\infty} a_i c^i \otimes \sum_{i=0}^{\infty} b_i c^i \right)
=
\sum_{i=0}^{\infty} \sum_{\ i_1 + i_2 = i, i_1, i_2 \in \mathbb{N} } a_{i_1} b_{i_2} c^{i} 
$$
and comultiplication 
$$
\Delta : \mathbb{R}[[c]] \rightarrow \mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]]
$$
defined by setting

$$ 
\Delta \left( c \right) = c \otimes 1 + 1 \otimes c
$$
 
Let $I \subset \mathbb{R}[[c]]$ be an ideal of $\mathbb{R}[[c]]$ such that
 
$$
\Delta (I) \subseteq I \otimes_{\mathbb{R}} \mathbb{R}[[c]] + \mathbb{R}[[c]] \otimes_{\mathbb{R}} I
$$

Then $I$ must be one of the following ideals:

* $\{ 0 \}$

* $c \cdot \mathbb{R}[[c]]$

* $\mathbb{R}[[c]]$

\end{theorem}

\begin{proof} let $I$ be a nonzero ideal of $\mathbb{R}[[c]]$. From the theorem [here](https://ncatlab.org/nlab/show/power+series#is_a_principal_ideal_domain_given_r_is_a_field), $I = c^n \cdot \mathbb{R}[[c]]$ for some $n \in \mathbb{N}$. 

We have

$$
\begin{aligned}
  \Delta(c^n) 
= & \Delta (c)^n \\
= & (c \otimes 1 + 1 \otimes c)^n \\
= & \sum_{ i = 0 }^n { \binom{n}{i} } c^i \otimes c^{n - i} \in (c^n \cdot \mathbb{R}[[c]]) \hat{\otimes} \mathbb{R}[[c]] + \mathbb{R}[[c]]  \hat{\otimes} (c^n \cdot \mathbb{R}[[c]])
\end{aligned}
$$

For each $(i,j) \in \mathbb{N} \times \mathbb{N}$ such that $i + j = n$, 

$$c^i \otimes c^j \in (c^n \cdot \mathbb{R}[[c]])  \hat{\otimes}_{\mathbb{R}}  \mathbb{R}[[c]] + \mathbb{R}[[c]]  \hat{\otimes}_{\mathbb{R}} (c^n \cdot \mathbb{R}[[c]])$$

We can express $(c^n \cdot \mathbb{R}[[c]])  \hat{\otimes}_{\mathbb{R}}  \mathbb{R}[[c]] + \mathbb{R}[[c]]  \hat{\otimes}_{\mathbb{R}}  (c^n \cdot \mathbb{R}[[c]])$ as a span of an $\mathbb{R}$-basis:

$$
(c^n \cdot \mathbb{R}[[c]])   \hat{\otimes}_{\mathbb{R}}  \mathbb{R}[[c]] + \mathbb{R}[[c]]   \hat{\otimes}_{\mathbb{R}}  (c^n \cdot \mathbb{R}[[c]])
=
\mathrm{span} \left\{ c^i \otimes c^j : n \leq i\ \text{ or }\ n \leq j \right\}
$$

so for each $(i,j) \in \mathbb{N} \times \mathbb{N}$ such that $i + j = n$, either $n \leq i$ or $n \leq j$.

We can conclude from this fact that $n = 0$ or $n = 1$.
\end{proof}

