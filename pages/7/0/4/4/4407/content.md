
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Statement

Classically, the **fundamental theorem of algebra** states that 

* The [[field]] of [[complex number]]s $\mathbb{C}$ is [[algebraically closed field|algebraically closed]]. In other words, every nonconstant [[polynomial function]] with [[coefficients]] in $\mathbb{C}$ has a [[root]] in $\mathbb{C}$. 

Since every non-zero polynomial could be made a [[monic polynomial]] by dividing by the leading coefficient, it could also be expressed as

* The [[field]] of [[complex number]]s $\mathbb{C}$ is [[integrally closed field|integrally closed]]. In other words, every [[monic polynomial|monic]] [[polynomial function]] with [[coefficients]] in $\mathbb{C}$ has a [[root]] in $\mathbb{C}$. 

Many proofs of this theorem are known (see the [references](#References) below); some use [[complex analysis]] (the reciprocal of a [[polynomial function]] cannot be bounded), some use [[algebraic topology]] (the degree of a map is invariant with respect to homotopy), and some use advanced calculus (polynomial functions on the complex numbers are [[open map|open mappings]]). All of these proofs involve, at some level, the fact that the real numbers are [[Dedekind real number|Dedekind complete]], which has as a consequence the fact that the real numbers are [[archimedean field|archimedean]]. 

## Algebraic proof via real closed fields 

Despite its name, the fundamental theorem of algebra makes reference to a concept from [[analysis]] (the field of complex numbers).  However, the analytic part may be reduced to a minimum: that the field of [[real numbers]] is [[real closed field|real closed]].  This has been known essentially forever, and is easily proved using (for example) the [[intermediate value theorem]].

The rest of the proof is algebraic and, unlike the other proof methods, applies to all [[real closed field]]s, which need not be archimedean. It is due to [[Emil Artin]], and forms a basic chapter in the Artin--Schreier theory of real closed fields.

We recall that a _real closed field_ is an [[ordered field]] such that every positive element has a [[square root]], and every polynomial function of odd degree has a root.  Note that the polynomial function $x^2 + 1$ cannot have any root in a real closed field --- or in fact in any ordered field, since we always have $x^2\ge 0$ and hence $x^2+1 \ge 1$.

+-- {: .num_theorem}
###### Theorem 
If $F$ is real closed, then $K = F[\sqrt{-1}]$ is algebraically closed. 
=--

+-- {: .proof} 
###### Proof 
We must show that any [[irreducible polynomial]] $p$ of degree greater than $0$ with coefficients in $K$ has a root in $K$. Since $F$ has characteristic $0$, it is a [[perfect field]]. 

Thus the [[splitting field]] of $p$ is a finite [[Galois extension]] $L$ of $F$, with [[Galois group]] $G$. If $G(2)$ is the [Sylow 2-group](http://ncatlab.org/nlab/show/class+equation#sylow_theorems) of $G$, then the [[fixed field]] $E$ of $G(2)$ is an odd degree extension of $F$. Any $\alpha \in E$ must then have an irreducible polynomial function $q \in F[x]$ of odd degree. But since $F$ is real closed, $q$ has a root in $F$; by irreducibility, $\deg(q) = 1$ and $\alpha \in F$, forcing $E = F$ and $G = G(2)$. We have ${|G|} \gt 1$ since the splitting field contains $K$. 

So $G$ is a $2$-[[primary group]]. But for any [[prime number]] $p$, a nontrivial finite $p$-group has nontrivial [[center]] (see [here](/nlab/show/class+equation#pgroup)), and is therefore [[solvable group|solvable]] by an inductive argument. Therefore the extension $L/F$ arises from a tower of non-trivial [[quadratic extension]]s 

$$F \subseteq L_1 \subseteq \ldots \subseteq L_n = L$$ 

By the [[quadratic formula]], the first field $L_1$ arises by adjoining roots to $F$ of a polynomial function $x^2 + a x + b$, 

$$\frac{-a \pm \sqrt{a^2 - 4b}}{2},$$ 

where $a^2 - 4b$ is negative. Since $F$ is real closed, the positive element $4b - a^2$ has a square root in $F$, so that the roots displayed above belong to $K = F[\sqrt{-1}]$. So $L_1 = K$. But $K$ has no nontrivial quadratic extensions by the lemma that follows, so in fact $L_1 = L_n = K$ and the theorem is proved. 
=-- 

+-- {: .num_lemma #sqrt}
###### Lemma 
Every element of $K = F[\sqrt{-1}]$ has a square root in $K$. 
=-- 

+-- {: .proof} 
###### Proof 
The proof is most easily apprehended by analogy with polar coordinate representations of complex numbers and half-angle formulas, where a square root of $r e^{i\theta}$ is given by $r^{1/2}e^{i\theta /2}$. Let $i$ be a fixed square root of $-1$, and let $a + b i$ be an arbitrary element of $K$, with $a, b \in F$. We must solve $(x + y i)^2 = a + b i$, i.e., find $x, y \in F$ that solve 

$$x^2 - y^2 = a, \qquad 2x y = b$$ 

Since $a^2 + b^2$ has a square root in $F$, we may assume by homogeneity in $x, y$ that $(a, b)$ is on the unit circle: $a^2 + b^2 = 1$. By interchanging $x$ and $y$ if need be, we may assume $0 \leq a \leq 1$; replacing $y$ by $-y$ if need be, we may assume $b \geq 0$. Taking $x, y \geq 0$ such that 

$$x^2 = \frac{1+a}{2}, \qquad y^2 = \frac{1-a}{2},$$ 

we obtain a solution (since $x^2 - y^2 = a$ and $4 x^2 y^2 = b^2$). 
=--


## Classical FTA via advanced calculus 

As noted above, many proofs of the fundamental theorem are known. The following proof, ultimately rooted in the fact that [[polynomial mappings]] on $\mathbb{C}$ are [[open mappings]], has the advantage that it requires very little machinery. From what I ([[Todd Trimble]]) understand, it is close to the method used by Argand to give his proof (1814)[^1]. 

[^1]: Despite the credit given to Gauss for his demonstration of 1799, Argand's proof is often credited as the first one that is *fully rigorous*. The proof given here also uses the [[Bolzano-Weierstrass theorem]] ([Bolzano 1817](Bolzano-Weierstrass+theorem#Bolzano1817)), making it somewhat contemporaneous. Argand is also widely credited as the one who introduced the cutting-edge idea of viewing complex numbers and their operations *geometrically*, which the proof here also uses (the complex plane $\mathbb{C}$ being also known as the Argand plane). 

Let $f\colon \mathbb{C} \to \mathbb{C}$ be a nonconstant polynomial mapping, and suppose $f$ has no zero. 

1. Let $s$ be the [[infimum]] of values ${|f(z)|}$; choose a [[sequence]] $z_1, z_2, z_3, \ldots$ such that ${|f(z_n)|} \to s$. Since $\lim_{z \to \infty} f(z) = \infty$, the sequence $z_n$ must be bounded; by the [[Bolzano-Weierstrass theorem]] it has a [[sequence|subsequence]] $z_{n_k}$ that converges to some point $z_0$. Then ${|f(z_{n_k})|}$ converges to ${|f(z_0)|}$ by continuity, and converges to $s$ as well, so ${|f(z)|}$ attains an absolute minimum $s$ at $z = z_0$. By supposition, $f(z_0) \neq 0$. 

2. The polynomial function $f$ may be uniquely written in the form 
$$f(z) = f(z_0) + g(z)(z - z_0)^n$$ 
where $g$ is polynomial function and $g(z_0) \neq 0$. Put 
$$F(z) = f(z_0) + g(z_0)(z - z_0)^n$$ 
and choose $\delta \gt 0$ small so that 
$${|z - z_0|} = \delta \Rightarrow {|g(z) - g(z_0)|} \lt {|g(z_0)|}.$$ 

3. $F$ maps the circle $C = \{z : {|z - z_0|} = \delta\}$ _onto_ a circle of radius $r = {|g(z_0)|}\delta^n$ centered at $f(z_0)$. (This uses the fact that any complex number has an $n^{th}$ root, which one can prove using polar coordinate representations. We omit the details.) Choose $z' \in C$ so that $F(z')$ is on the line segment between the origin and $f(z_0)$ (we can always choose $\delta$ so that also $r \lt {|f(z_0)|}$). Then 
$${|F(z')|} = {|f(z_0)|} - r$$
We also have 
$${|f(z') - F(z')|} = {|g(z') - g(z_0)|} {|z' - z_0|^n} \lt {|g(z_0)|} \delta^n = r$$ 
according to how we chose $\delta$ in 2. We conclude by observing the strict inequality 
$${|f(z')|} \leq {|F(z')|} + {|f(z') - F(z')|} \lt {|f(z_0)|} - r + r = {|f(z_0)|},$$ 
which contradicts the fact that ${|f(z)|}$ attains an absolute minimum at $z = z_0$.  

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
\label{TheComplexMagmaVersionOfFTA} 
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

These coefficients must satisfy the two equations which are the image in degree-2 [[integral cohomology]] of the two [[unit laws]] (the first assumed property on $K$):

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

of the algebra $H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z}) \cong \mathbb{Z}[[c]]/c^n \mathbb{Z}[[c]]$ with itself. 

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


{#TwoLemmas} A variant of this proof works with the [[real cohomology]] of infinite complex projective space. 

There is an isomorphism of $\mathbb{R}$-algebras:

$$
  H^{\bullet}\big( \mathbb{C}P^{\infty}; \mathbb{R}\big) 
    \cong 
  \mathbb{R}[[c]]
  \mathrlap{\,.}
$$

There is a comultiplication on $H^{\bullet}(\mathbb{C}P^{\infty} ; \mathbb{R})$ which is related to the [complex orientation](complex+oriented+cohomology+theory#DefInTermsOfGeneralizedFirstChernClass) on the [[Eilenberg-MacLane spectrum]] $H\mathbb{R}$. More precisely, there is a map of $\mathbb{R}$-algebras

$$
  \Delta 
    \;\colon\; 
  H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R}) 
    \rightarrow 
  H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R})   
    {\hat{\otimes}}_{\mathbb{R}} 
  H^{\bullet} ( \mathbb{C}P^{\infty} ; \mathbb{R}) 
$$

which is the unique map of $\mathbb{R}$-algebras such that 

$$
  \Delta(c) = c \otimes 1 + 1 \otimes c 
  \mathrlap{\,.}
$$

When $\mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]]$ is identified with $\mathbb{R}[[x,y]]$, this is the additive [[formal group law]] on $\mathbb{R}$.

Then we have the following facts:

* $H^{\bullet} ( \mathbb{C}P^n ; \mathbb{R}) \cong \mathbb{R}[[c]] / c^n \mathbb{R}[[c]]$ as $\mathbb{R}$-algebras.

* Any continuous binary operation on $\mathbb{C}P^{n}$ with a unit (satisfying the left and right [[unit laws]]) induces a quotient of the $\mathbb{R}$-algebra $\mathbb{R}[[c]]$ which commutes with the comultiplication in the sense that the following diagram commutes

\begin{xymatrix}
  \mathbb{R}[[c]] 
    \ar[d] 
    \ar[r] 
    &  
    \mathbb{R}[[c]] 
   \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]] 
   \ar[d]  
     \cr
   \mathbb{R}[[c]] / c^n \mathbb{R}[[c]]        
     \ar[r] 
    & 
    \big( \mathbb{R}[[c]]/c^n \mathbb{R}[[c]] \big) 
    \hat{\otimes} 
    \big( \mathbb{R}[[c]]/c^n \mathbb{R}[[c]] \big)
    \mathrlap{\,.}
\end{xymatrix}



On the [[power series ring]] $\mathbb{R}[[c]]$ consider the multiplication
$$
  \mu 
    \;\colon\; 
  \mathbb{R}[[c]]  
    \hat{\otimes}_{\mathbb{R}} 
  \mathbb{R}[[c]] 
    \longrightarrow 
  \mathbb{R}[[c]]
$$
given by
$$
  \mu \big( 
    \sum_{i= 0}^{\infty} a_i c^i 
      \otimes 
    \sum_{i=0}^{\infty} b_i c^i 
  \big)
  =
  \sum_{i=0}^{\infty} 
  \sum_{\ i_1 + i_2 = i, i_1, i_2 \in \mathbb{N} } 
   a_{i_1} b_{i_2} c^{i} 
$$
and the comultiplication 
$$
  \Delta 
    \;\colon\; 
  \mathbb{R}[[c]] 
    \longrightarrow 
  \mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]]
$$
given by
$$ 
  \Delta \left( c \right) 
    = 
  c \otimes 1 + 1 \otimes c
  \mathrlap{\,.}
$$


\begin{theorem} 
Let $I \subset \mathbb{R}[[c]]$ be an ideal of $\mathbb{R}[[c]]$ such that
 
$$
  \Delta (I) 
    \subseteq 
  I \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]] 
    + 
  \mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} I
$$

Then $I$ must be one of the following ideals:

* $\{ 0 \}$

* $c \cdot \mathbb{R}[[c]]$

* $\mathbb{R}[[c]]$

\end{theorem}

\begin{proof}\label{ProofCharacterizingIdeals} 
The ring of formal power series $\mathbb{R}[[c]]$ over the [[field]] $\mathbb{R}$ is a [[discrete valuation ring]]. Its unique maximal ideal is generated by $c$. Consequently, every non-zero ideal in $\mathbb{R}[[c]]$ is principal and is generated by some power of $c$ (see [there](power+series#PrincipalIdealDomain)).
Therefore, $I = \{0\}$ or there exists a non-negative integer $n \in \mathbb{N}$ such that $I = (c^n) = c^n \cdot \mathbb{R}[[c]]$.

If $I = \{0\}$, the condition $\Delta(\{0\}) = \{0\} \subseteq \{0\} + \{0\}$ holds trivially. Therefore we now assume that $I$ is a non-zero ideal, so that $I = (c^n)$ for some $n \ge 0$.

To analyze the ideal condition, we use the canonical [[isomorphism]] of topological $\mathbb{R}$-algebras:
$$
  \begin{array}{ccc}
  \mathbb{R}[[c]] 
    \hat{\otimes}_{\mathbb{R}} 
  \mathbb{R}[[c]] 
    &\overset{\sim}{\longrightarrow}&
  \mathbb{R}[[x, y]]
  \\
  c \otimes 1 &\mapsto& x
  \\
  1 \otimes c &\mapsto& y\mathrlap{\,.}
  \end{array}
$$

Under this isomorphism:

1. The comultiplication acts as $\Delta(c) = x + y$.

2. The bounding ideal $I \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]] + \mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} I$ corresponds precisely to the ideal generated by $x^n$ and $y^n$, namely $(x^n, y^n) \subset \mathbb{R}[[x, y]]$. 

The condition $\Delta(I) \subseteq I \hat{\otimes}_{\mathbb{R}} \mathbb{R}[[c]] + \mathbb{R}[[c]] \hat{\otimes}_{\mathbb{R}} I$ therefore requires that the image of the generator $c^n$ belongs to this ideal: 
$$
  (x + y)^n 
    \in 
  \big( x^n, y^n \big)
  \mathrlap{\,.}
$$


Now, the expression $(x+y)^n$ is a homogeneous polynomial of total degree $n$.
Any element $P(x,y) \in (x^n, y^n)$ can be written as $x^n f(x,y) + y^n g(x,y)$ for some power series $f, g \in \mathbb{R}[[x,y]]$. 
Because formal power series expand into components of ascending degrees, the terms of total degree exactly $n$ in $P(x,y)$ must come exclusively from the constant terms of $f$ and $g$. 

Thus, the degree-$n$ homogeneous part of *any* series in the ideal $(x^n, y^n)$ is necessarily of the form $A x^n + B y^n$ for some real constants $A, B \in \mathbb{R}$.

Since $(x+y)^n$ belongs to $(x^n, y^n)$ and is entirely homogeneous of degree $n$, it must equal its own degree-$n$ component. Therefore, there exist $A, B \in \mathbb{R}$ such that:
$$
  (x+y)^n 
   \;=\; 
  A x^n + B y^n
  \mathrlap{\,.}
$$

However, by the [[binomial theorem]], we know that:
$$
  (x+y)^n 
   \;=\; 
  \sum_{i=0}^n \binom{n}{i} x^i y^{n-i}
  \mathrlap{\,.}
$$

For these two expressions to be identical, the coefficients of all cross-terms $x^i y^{n-i}$ (where $0 \lt i \lt n$) must be zero, in particular $\binom{n}{1}$ would need to be zero if $n\gt 1$. 

Now we use that we are working over $\mathbb{R}$, a field of [[characteristic zero]]. The binomial coefficient $\binom{n}{1}=n$ is nonzero for all $n\geq 1$, so we are left with the only possible cases being $n\leq 1$. The case $n=0$ holds by inspection, and corresponds to the improper ideal, and the case $n=1$ obviously satisfies the required identity, and is the proper nonzero ideal in the statement.
\end{proof}


## In constructive mathematics

There are multiple notions used in the formulation of the fundamental theorem of algebra that bifurcate into different notions in [[constructive mathematics]]. 

First of all, the notion of a field of [[real numbers]] bifurcates into multiple distinct notions of the real numbers, so one has a fundamental theorem of algebra for every field of [[complex numbers]] $\mathbb{C} = \mathbb{R}[i]/(i^2 + 1)$ of a notion of real numbers $\mathbb{R}$, ranging from the [[Cauchy real numbers]] to any [[sequentially Cauchy complete|Cauchy complete]] [[Archimedean ordered field]], examples of which include the [[HoTT book real numbers]], which is the [[initial object|initial]] Cauchy complete Archimedean ordered field, and the [[Dedekind real numbers]], which is the [[terminal object|terminal]] Cauchy complete Archimedean ordered field. 

Secondly, one has to decide what kind of polynomial functions to use for the FTA. In constructive mathematics, one usually considers three notions of polynomial functions, which in constructive mathematics are defined using the [[tight apartness relation]] on the real numbers rather than [[denial inequality]]:

1. non-constant polynomial functions: a polynomial function $p(z) = \sum_{i \leq n} a_n z^n$ is *non-constant* if one has at least one coefficient $a_i$ in $\mathbb{C}$ apart from zero, with $0 \lt i \leq n$

1. polynomial function with positive [[degree of a polynomial|degree]]: a polynomial function $p(z) = \sum_{i \leq n} a_n z^n$ has a positive degree $n$ if $a_n$ is apart from zero, with $n \gt 0$

1. [[monic]] polynomial functions: a polynomial function $p(z) = \sum_{i \leq n} a_n z^n$ is monic if $a_n = 1$, with $n \gt 0$

However, the FTA that uses monic polynomial functions imply the other versions: 

\begin{theorem}
Suppose that the FTA for monic polynomial functions hold. Then the FTA for non-constant polynomial functions hold. 
\end{theorem}

\begin{proof}
Lemma 6 and Corollary 1 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) hold for any [[Heyting field]] $F$ as their proofs only require the field structure of $F$, and Theorem 1 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) is the FTA for non-constant functions and depends on Lemma 6, Corollary 1, and the FTA for monic polynomial functions but otherwise only depends on the field structure of $F$. 
\end{proof}

The converses come from the fact that every polynomial with positive degree is non-constant and every monic polynomial has positive degree. Thus, it suffices to only consider monic polynomials in the fundamental theorem of algebra. 

Finally, one has to decide whether to use [[mere proposition|mere]] existence of a [[root]] in the sense of traditional [[first-order logic]] or constructive existence in the sense of the [[BHK interpretation]] in the formulation of the FTA. One can also consider, instead of exact roots, approximate roots of the polynomial function. 

As a result, there are multiple different versions of the fundamental theorem of algebra which are equivalent in classical mathematics but are not equivalent in constructive mathematics. Different authors have ended up proving different versions of the fundamental theorem of algebra for different kinds of real numbers, without assuming any constructive [[taboos]], while other versions of the fundamental theorem of algebra are unprovable without certain constructive [[taboos]] and may even be provably false from other constructive [[taboos]]. 

### Constructive FTA with mere existence of zeroes

The version of the fundamental theorem of algebra that uses mere existence for existence of zeroes is stated as follows: 

\begin{proposition}
Every [[monic]] [[polynomial function]] $p(z) = \sum_{i \leq n} a_n z^n$ with [[degree of a polynomial|degree]] $n$ has a [[root]] $p$ in $\mathbb{C}$. 
\end{proposition}

* [Ruitenburg 1991](#Ruitenburg91) has proven, without using any constructive [[taboos]], that every [[monic polynomial|monic]] [[polynomial function]] with coefficients in the Cauchy complex numbers, with one of the coefficients invertible, has a root in the Cauchy complex numbers. 

* This is lemma 5 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00), which is valid for the field of [[complex numbers]] $\mathbb{C} = \mathbb{R}[i]/(i^2 + 1)$ of any [[sequentially Cauchy complete space|Cauchy complete]] [[Archimedean ordered field]] $\mathbb{R}$. 

* In addition, section 5 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) includes a list of authors who proved the fundamental theorem of algebra for monic polynomials, some like [[Brouwer]] with additional assumptions such as [[countable choice]]. 

### Constructive FTA with constructive existence of zeroes

The version of the fundamental theorem of algebra that uses the [[BHK interpretation]] for constructive existence of zeroes is stated as follows: 

\begin{proposition}
For every [non-constant / positive degree / monic] [[polynomial function]] $p(z) = \sum_{i \leq n} a_n z^n$ with degree $n$, one can construct a specified root of $p$ in $\mathbb{C}$. 
\end{proposition}

This version of the fundamental theorem of algebra is not provable in [[neutral constructive mathematics]]. To show that this is the case, we turn to reframing the fundamental theorems of algebra in terms of surjectivity and having [[right inverses]] of complex polynomial functions so that one can show that it is equivalent to a weak form of choice. 

Let $p(z) = \sum_{i \leq n} a_n z^n$ be a polynomial function on the complex numbers. Every such $p(z)$ can be written as the sum of a constant $a_0$ and a polynomial function $q(z) = \sum_{1 \leq i \leq n} a_n z^n$ with a [[fixed point]] at zero. As a result, the statement that there exists a complex number $z$ such that $p(z) = 0$ is equivalently the statement that there exists a complex number $z$ such that $q(z) = b$, where $b = -a_0$. Thus, one can rewrite the fundamental theorem of algebra as follows:

\begin{theorem}
Given a complex number $b$ and a [non-constant / positive degree / monic] polynomial function $q(z)$ on the complex numbers such that $q(0) = 0$, there exists a complex number $c$ such that $q(c) = b$. 
\end{theorem}

Or equivalently

\begin{theorem}
Every [non-constant / positive degree / monic] polynomial function $q(z)$ on the complex numbers such that $q(0) = 0$ is [[surjective]]. 
\end{theorem}

One can do the same analysis with the [[BHK interpretation]] of the FTA, the statement that one can construct a specified complex number $z$ such that $p(z) = 0$ is equivalently the statement that one can construct a specified complex number $z$ such that $q(z) = b$, where $b = -a_0$. Thus, one can rewrite the fundamental theorem of algebra as follows:

\begin{theorem}
Given a complex number $b$ and a [non-constant / positive degree / monic] polynomial function $q(z)$ on the complex numbers such that $q(0) = 0$, one can construct a specified complex number $c$ such that $q(c) = b$. 
\end{theorem}

Or equivalently

\begin{theorem}
Every [non-constant / positive degree / monic] polynomial function $q(z)$ on the complex numbers such that $q(0) = 0$ has a [[section]]. 
\end{theorem}

Thus, the gap between the version of the FTA using [[mere proposition|mere]] existence and the version using constructive existence is precisely this weak version of the [[axiom of choice]]:

\begin{proposition}
Every [[surjective]] [[polynomial function]] on the [[complex numbers]], that is [non-constant / with positive degree / monic] and has a [[fixed point]] at zero, has a [[section]]. 
\end{proposition}

This is the reason why some classical proofs of versions of the fundamental theorem of algebra that use mere existence fail to work constructively if they are reliant on a [[square root]] function on the complex numbers, such as the proof in Lemma \ref{sqrt} which uses the [[quadratic formula]]. Such a square root function is a [[section]] of the squaring function $z \mapsto z^2$ and so cannot be proven to exist on the complex numbers from surjectivity of $z \mapsto z^2$, since the square root on the complex numbers, if it exists, is [[discontinuous]] at zero, which implies the constructive taboo [[analytic WLPO]] for the [[real numbers]] and [[decidable equality]] for the complex numbers. In fact, in certain [[topoi]], such as [[sheaves]] over $\mathbb{C}$, one can prove that there are no square root functions because in those topoi all functions on the complex numbers are continuous. 

The unprovability of this weak version of choice in neutral constructive mathematics also implies that one cannot factor every monic polynomial function $p(z)$ of degree $n$ into $n$ distinct monomials $(z - b_i)$ for $i \lt n$ such that $p(z) = \prod_{i \lt n} (z - b_i)$, since one would need to first construct the specified complex roots $b_i$. Thus, the complex numbers are not provably an [[algebraically closed field]]. 

In light of this, one can instead interpret the constructive FTA as a statement about sets of roots rather than about individual roots, an interpretation that dates from [Richman 2000](#Richman00). He constructs a [[complete metric space]] $\hat{M}_n(\mathbb{C})$ which, classically, is the space of $n$-element [[multisets]] of complex numbers (and constructively is the completion of that space) and proves that every complex polynomial function $p$ of degree $n$ may be associated with a point in this space in such a way that the $n$ elements of that point (when viewed as a multiset, if possible, and morally in any case) are the $n$ roots of $p$. 

### Approximate FTA

Alternatively, one can consider an approximate version of the fundamental theorem of algebra using constructive existence in the sense of the [[BHK interpretation]]:

\begin{theorem}
For every [non-constant / positive degree / monic] [[polynomial function]] $p(z) = \sum_{i \leq n} a_n z^n$ with degree $n$, one can construct positive reals $q \lt 1$ and $c \gt \vert f(0) \vert$ and a [[Cauchy sequence]] $w:\mathbb{N} \to \mathbb{C}$ in $\mathbb{C}$ such that for all natural numbers $n$, $\vert p(w_n) \vert \lt q^n c$. 
\end{theorem}

\begin{proof}
This is essentially most of lemma 5 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00), only one stops in the proof before one considers whether the limit of the Cauchy sequence exists or not. 
\end{proof}

Arguably, this approximate version of the fundamental theorem of algebra is what is important in constructive [[numerical analysis]]. 

## In reverse mathematics

Assuming classical logic, but weak foundations, it can be shown that FTA is true in the [[reverse mathematics]] system $RCA_0$ ([Tanaka-Yamazaki 2005](#TY2005)).


## History
 {#History}

The proof was attempted many times before Gauss gave what is accepted as the first proof in his dissertation ([Gauss 1799](#Gauss1799)), although this was not without issues (Gauss 'fixed' this proof almost 50 years later, but the last gap was not filled until the 20th century).

All proofs of this fact (of which there are many) require something analytic, in the sense that ordinary algebra will not suffice: one needs to know that the real numbers (or the complex numbers) 'have no algebraic gaps'. For instance, the rational numbers famously don't contain the square root of $2$. The cleanest proof I know, due to Artin, that isolates this analytic germ, uses the step-ladder result that the real numbers form what is called a [[real closed field]]. This is essentially saying that non-negative real numbers have square roots, and odd degree polynomial functions have roots (anyone who has plotted a cubic can appreciate this fact). Alternatively, one can characterise real closed fields as those for whom the Intermediate Value Theorem (IVT) holds for polynomial functions. Accepting this result (which does need proof), the FTA follows using pure algebra (although not of the high-school sort).

However, it is of interest, partly theoretical, partly for the sake of finding the bare minimum needed to prove the FTA, to know an elementary proof, namely one that minimises the use of analytic techniques (for instance, the IVT for polynomial functions follows from the IVT for continuous functions, but that is like killing a mosquito with a bazooka). Gauss' second proof ([Gauss 1866](#Gauss1866)) is elementary (and predates Artin's by a long time). Since Gauss lacked modern algebraic techniques, some of his proof is laborious, but ([Taylor 85](#Taylor85)) gives a modern gloss. (With some amusing side notes: as Taylor puts it -- 'Gauss takes the opportunity [to] be rude to his inferior contemporaries'.) Gauss' proof, in modern language, takes up less than a page and a half, but this presupposes familiarity with some of the theory of fields (but which is pure algebra). Artin's proof, by comparison, drawing on major theorems can be given in half a page.

It should be noted, in the context of the last statement, that proofs of the FTA can be given, relying on analytic 'bazooka' theorems, that are one sentence. However, to spell out the proofs of the necessary theorems, one needs a course in analysis, of some variety, so one is merely sweeping a lot under a very small rug. 

In [[constructive mathematics]], there are multiple versions of the FTA which are inequivalent to each other, many of which are not formulated in algebraic terms. For example, the approximate version of the FTA listed above requires one to show that for all polynomials and for all [[neighborhoods]] around zero there exists a complex number $z$ such that the polynomial evaluated at $z$ is in the [[neighborhood]], which is analytic and topological rather than algebraic. 

## References
 {#References}

* {#Gauss1799} [[Carl Gauss]], _Demonstratio nova theorematis functionem algebraicam rationalem integramunius variabilis in factores reales primi vel secundi gradus resolvi posse_, Dissertation, Helmstedt (1799); Werke 3, 1&#8211;30 (1866) ([English transl. pdf](http://www.jon-arny.com/httpdocs/Gauss/Gauss%20Fundamental%20Theorem.pdf)))

* {#Gauss1866} [[Carl Gauss]], _Demonstratio nova altera theorematis omnem functionem algebraicamrationalem integram unius variabilis in factores reales primi vel secundi gradus resolviposse_, Comm. Soc. Reg. Sci. G&#246;ttingen 3, 107&#8211;142 (1816); Werke 3, 33&#8211;56 (1866)

* Michael Eisermann. _An Elementary Real-Algebraic Proof via Sturm Chains_. [pdf](http://www.jon-arny.com/httpdocs/Gauss/Constructive%20roots-annotated.pdf)

  _Another new proof of the theorem that every integral rational algebraic function of one variable can be resolved into real factors of the first or second degree_ translated by [[Paul Taylor]] and B. Leak (1983) ([web](http://www.paultaylor.eu/misc/gauss-web))

* {#Taylor85} [[Paul Taylor]], _Gauss' Second Proof_, Eureka 45 (1985) 42-47 ([pdf](http://www.jon-arny.com/httpdocs/Gauss/Eureka-2-aug24.pdf))

A proof using [[differential topology]]:

* [[John Milnor]]; pp. 8--9 in: _Topology from the differential viewpoint_, Princeton University Press (1997) &lbrack;[ISBN:9780691048338](https://press.princeton.edu/books/paperback/9780691048338/topology-from-the-differentiable-viewpoint), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnortop.pdf)&rbrack;

A [[constructive mathematics|constructive]] proof of the fundamental theorem of algebra for any [[sequentially Cauchy complete space|Cauchy complete]] [[Archimedean ordered field]]: 

* {#GWZ00} Herman Geuvers, Freek Wiedijk, Jan Zwanenburg, *A Constructive Proof of the Fundamental Theorem of Algebra without using the Rationals*, TYPES '00: Selected papers from the International Workshop on Types for Proofs and Programs, Pages 96 - 111, 08 December 2000 &lbrack;[web](https://dl.acm.org/doi/10.5555/646540.696038), [pdf](https://www.cs.ru.nl/F.Wiedijk/pubs/kneser.pdf)&rbrack;

A [[constructive mathematics|constructive]] proof of a variant using finite multisets of complex numbers: 

* {#Richman00} [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*, Pacific Journal of Mathematics **196** 1 (2000) 213–230 &lbrack;[doi:10.2140/pjm.2000.196.213](http://dx.doi.org/10.2140/pjm.2000.196.213), [pdf](https://msp.org/pjm/2000/196-1/pjm-v196-n1-p10-p.pdf)&rbrack;

see also:

* [[Fred Richman]], *Constructive Mathematics without Choice*,
in: *Reuniting the Antipodes -- Constructive and Nonstandard Views of the Continuum* Synthese Library **306**, Springer (2001) 199-206 &lbrack;[doi:10.1007/978-94-015-9757-9_17](https://doi.org/10.1007/978-94-015-9757-9_17)&rbrack;

A [[constructive mathematics|constructive]] algebraic proof for the [[modulated Cauchy real numbers]] without choice princples such as [[weak countable choice]]:

* {#Ruitenberg91} [[Wim Ruitenburg]]: *Constructing Roots of Polynomials over the Complex Numbers*, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract **84** Centre for Mathematics and Computer Science, Amsterdam (1991) 107–-128 &lbrack;[pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf), [[Ruitenburg-Roots.pdf:file]]&rbrack;

A full formalization in the [[Rocq]] [[proof assistant]]:

* Herman Geuvers, [[Freek Wiedijk]], Jan Zwanenburg: *A Constructive Proof of the Fundamental Theorem of Algebra without Using the Rationals &lbrack;[web](http://dl.acm.org/citation.cfm?id=696038)&rbrack;

The [above proof](#ViaCellularCohomology) using [[integral cohomology]] of [[complex projective space]]:

* {#Bruner2009} [[Robert Bruner]]: *cute proof*, message to [ALGTOP-L mailing list](https://rezk.web.illinois.edu/algtop-l/algtop-l.html) (1 Dec. 2009) &lbrack;[algtop-l:2009q4/000645](https://rezk.web.illinois.edu/algtop-l/archives2007-2023/2009q4/000645.html)&rbrack;

Discussion in the context of [[reverse mathematics]]:

* {#TK2005} Kazuyuki Tanaka, Takeshi Yamazaki: _Manipulating the reals in $RCA_0$_, inL _Reverse Mathematics 2001_, Lecture Notes in Logic **21** (2005)

See also:

* Matthew Steed: *Proofs of the Fundamental Theorem of Algebra*, [Reu2014](https://math.uchicago.edu/~may/REU2014/) &lbrack;[pdf](https://math.uchicago.edu/~may/REU2014/REUPapers/Steed.pdf)&rbrack;

* MathOverflow: _[Ways to prove the fundamental theorem of algebra](http://mathoverflow.net/questions/10535/ways-to-prove-the-fundamental-theorem-of-algebra)_

[[!redirects fundamental theorem of algebra]]
[[!redirects Fundamental Theorem of Algebra]]
[[!redirects FTA]]
