> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\linebreak


\[\label{FiberIntegralViaHomAdjunct}\]
\begin{tikzcd}
  X
  \\[-100pt]
  H^{n+1}\big(
    X
     \times
    \mathbf{B} \mathbb{Z}
    ;
    \mathcal{A}
  \big)
  \ar[
    d,
    equals
  ]
  \ar[
    rrr,
    "{ \int_{\mathbf{B} \mathbb{Z}} }"
  ]
  &&&
  H^n\big(
    X;
    \mathcal{A}
  \big)
  \ar[
    d,
    equals
  ]
  \\
  \pi_0 \mathrm{Map}\big(
    X \times \mathbf{B} \mathbb{Z}
    ,
    \mathbf{B}^{n+1} \mathcal{A}
  \big)
  \ar[
    r,
    "{ \widetilde{(-)} }"
  ]
  &
  \pi_0 \mathrm{Map}\big(
    X 
    ,
    \mathrm{Map}(
      \mathbf{B} \mathbb{Z},
      \mathbf{B}^{n+1} \mathcal{A}
    )
  \big)
  \ar[
    r,
    "{ \sim }"
  ]
  &[-10pt]
  \pi_0 \mathrm{Map}\big(
    X 
    ,
    \mathbf{B}^{n+1} \mathcal{A}
    \times 
    \mathbf{B}^n \mathcal{A}
  \big)
  \ar[
    r,
    "{
      \mathrm{Map}(X, \mathrm{pr}_2)
    }"
  ]
  &
  \pi_0 \mathrm{Map}\big(
    X 
    ,
    \mathbf{B}^n \mathcal{A}
  \big)
\end{tikzcd}




---


$\esh$



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


Jun4 730 DeanYoung testing ...



## Using the cellular cohomology of complex projective space
 {#ViaCellularCohomology}

There is a proof using that the [[cellular cohomology]] of [[complex projective space]] $\mathbb{CP}^{n-1}$ is (see [there](complex+projective+space#Cohomology))

$$
  H^i(\mathbb{CP}^{n-1}, \mathbb{Z}) \cong \mathbb{Z}^{a_i}
  \mathrlap{\,,}
$$ 

where 
$$
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

and in which the cup product induces a ring-isomorphism 

$$
H^* (\mathbb{CP}^n, \mathbb{Z}) \simeq  \mathbb{Z}[c] / c^n \mathbb{Z}[c]
$$

where $c$ is the integral first Chern class (see [here](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace)

\begin{theorem} 
Let $K$ be a [[finite dimensional vector space]] over $\mathbb{C}$ with $\mu \colon K \otimes_{\mathbb{C}} K \rightarrow K$ a $\mathbb{C}$-[[linear map]] and an element designated by $\eta : \mathbb{C} \rightarrow K$ satisfying the following two properties:

* ([[unitality]]) $\mu \circ \left( \eta \otimes Id_{K} \right) \circ \eta_1 \ = \ Id_K \ = \ \mu \circ \left( Id_K \otimes \eta \right) \circ \eta_2$ where $\eta_1 : \{ * \} \times \mathbb{CP}^{n-1}  \rightarrow \mathbb{CP}^{n-1}$ and $\eta_2 : \mathbb{CP}^{n-1} \times \{ * \} \rightarrow \mathbb{CP}^{n-1}$ are the unit isomorphisms with respect to the cartesian closed category induced by [product](cartesian+product#InAGeneraCategory).

* (no [[zero-divisors]]) for $a, b \in K$, if $\mu (a \otimes b) = 0$, then either $a = 0$ or $b = 0$.

Then $K$ is [[isomorphism|isomorphic]] to $\mathbb{C}$ itself as a [[complex vector space|$\mathbb{C}$-vector space]], i.e. $\text{dim}(K) = 1$.
\end{theorem}

Note that we obtain such a nonassociative $\mathbb{C}$-algebra as the [[splitting field]] of any complex [[irreducible  polynomial]].

\begin{proof}
Using the second property we obtain a [[continuous function]] 

$$ 
 \mu |_{ \mathbb{C}^n - \{ 0 \} }  \ : \ \left( \mathbb{C}^{n} - \{ 0 \} \right) \times \left( \mathbb{C}^{n} - \{ 0 \} \right)\ \rightarrow\ \mathbb{C}^{n} - \{ 0 \}
$$

Bilinearity implies that $\pi \circ  \mu|_{ \mathbb{C}^n - \{ 0 \} }$ factors through the product $\mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1}$ where $\pi :  \mathbb{C}^{n} - \{ 0 \} \rightarrow \mathbb{CP}^{n-1}$ is the quotient map. We get a continuous function

$$
 [ \mu|_{ \mathbb{C}^n} ] \ : \ \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1} \rightarrow \mathbb{CP}^{n-1}
$$

We obtain two equations by applying degree-2 [[integral cohomology]] to the two unit laws in the first property, irrespective of any associativity or commutativity of $K$:

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

Let $y \in H^2(\mathbb{CP}^{n-1})$ be the generator of the [[cohomology ring]] $H^* ( \mathbb{CP}^{n-1} )$. We have:

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

We can write 

$$
  H^2(\mu,\mathbb{Z})(y) 
    = 
  a \cdot (1 \otimes y) + b \cdot (y \otimes 1)
$$

for some $a, b \in \mathbb{Z}$.

The two equations obtained from the unit laws for $K$ imply that:

$$
  a = 1, 
  \,
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
  H^*\big(
   \mathbb{CP}^{n-1};
   \mathbb{Z}
  \big) 
    \otimes_{\mathbb{Z}} 
  H^*\big(
    \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)  
    \cong  
  H^*\big(
    \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)
  \mathrlap{\,.}
$$

But $H^*(\mu,\mathbb{Z})$ is a [[ring homomorphism]], so

$$
  H^*(\mu,\mathbb{Z})(y^n) 
    = 
  (1 \otimes y + y \otimes 1)^n 
    = 
  \sum_{i = 0}^n {\binom{n}{i}} (1 \otimes y)^i \cdot (y \otimes 1)^{n-i} 
    = 
  \sum_{i = 0}^n y^{n-i} \otimes y^{i}
$$

as elements of the commutative Hopf-algebra

$$
  H^*(\mathbb{CP}^{n-1},\mathbb{Z}) 
    \otimes_{\mathbb{Z}} 
  H^*(\mathbb{CP}^{n-1},\mathbb{Z})  
   \;\cong\; 
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right) 
   \otimes  
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right)
  \mathrlap{\,.}
$$

The left-hand side is $0$.

The right hand side is 

$$ 
   \sum_{i = 1}^{n-1} y^{n-i} \otimes y^{i} 
  \mathrlap{\,.}
$$

By way of [[proof by contradiction|contradiction]], suppose that $n = \text{dim}(K)$ is greater than $1$. In this case, each of the terms $y^i \otimes y^{n-i}$ is nonzero for $0 \lt i \lt n$, and their sum is as well.

This implies that 

$$
  \sum_{i= 1}^{n-1} {\binom{n}{i}}  y^{n-i} \otimes y^{i}$$

is not zero, which contradicts that $y^n$ is zero using the above equation.

This implies $n = 1$ and hence the claim.
\end{proof}



## Using the complex topological $K$-theory of complex projective space
 {#ViaComplexTopologicalK-Theory}





