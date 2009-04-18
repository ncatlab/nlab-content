#Idea#

Smooth Deligne cohomology in degree $n$, 
denoted $\bar H^n(X,\mathbb{Z}) = H(X, \mathbb{Z}(n)^\infty,D)$,
of a smooth manifold $X$
is a realization of the 
[[differential cohomology|differential refinement]] (or smooth extension) $\bar H^n(X,\mathbb{Z})$ of the 
[[integral cohomology]] $H^n(X, \mathbb{Z})$ of $X$ in terms of
[[abelian sheaf cohomology]].

[[differential cohomology|Recall]] 
that analgous to how $H^n(X,\mathbb{Z})$ classifies line $(n-1)$-bundles 
and equivalently line $(n-2)$-gerbes on $X$, $\bar H^n(X, \mathbb{Z})$
classifies line $(n-2)$-gerbes with connection.

Accordingly, the _Deligne complex_ of sheaves $\mathbb{Z}(n)^\infty_D$
is a complex of sheaves of differential forms.

#Definition#

For $k \in \mathbb{N}$
write $\Omega^k(X)$ for the [[sheaf] of smooth differential $k$-forms on $X$
and $C^\infty(X,U(1))$ for the sheaf of smooth $U(1)$-valued functions on 
$X$. Let $C^\infty(X,U(1)) \stackrel{d log}{\to} \Omega^1(X)$ be the 
morphism of sheaves induced by regarding a $U(1) \simeq \mathbb{R}/\mathbb{Z}$-valued function locally
as a $\mathbb{R}$-valued function and applying the deRham differential $d$ to that.

This yields for each $n \in \mathbb{N}$ a complex of sheaves

$$
  \cdots \to 0 \to C^\infty(X,U(1)) \stackrel{d log}{\to}
    \Omega^1(X) \stackrel{d}{\to} \cdots \stackrel{d}{\to}
    \Omega^n(X)
$$

with $\Omega^n(X)$ in degree 0 and $C^\infty(X,U(1))$ in degree $n$.

This is ([[quasi-isomorphism|quasi-isomorphic]]) to the 
**Deligned complex** of sheaves, denoted $\mathbb{Z}(n+1)^\infty_D$.

**Deligne cohomology** in degree $n+1$ of $X$ is the 
[[abelian sheaf cohomology]] of this complex.

#Interpretation in terms of parallel transport#

There is a natural way to understand the Deligne complex of sheaves as a sheaf which assigns to each patch the Lie $n$-groupoid of smooth parallel transport $n$-functors. This perspective is helpful for understanding how Deligen cohomology relates to the bigger picture of [[differential cohomology]].

We start by discussing this in low degree.

There is a [[Lie groupoid]] called $P_1(X)$ whose smooth 
space of objects is $X$ and whose smooth space of morphisms is
a space of classes of smooth paths in $X$. 
Every smooth 1-form $A \in \Omega^1(X)$ induces 
a smooth [[functor]] $tra_A : P_1(X) \to \mathbf{B}U(1)$
from $P_1(X)$ to to the smooth [[groupoid]] $\mathbf{B} U(1)$
with one object and $U(1)$ as its smooth space of morphisms
by sending each path $\gamma : [0,1] \to X$
to $\exp (2 \pi i\int_0^1 \gamma^* A)$. This map 
from 1-forms to smooth functors turns out to be bijective:
every smooth functor of this form uniquely arises this way.
Similarly, one finds that smooth [[natural transformation]]
$\eta_f : tra_A \to tra_{A'}$ between two such functors
is in components precisely a 
smooth function $f : X \to U(1)$ such that $A' = A + d log f$.

Since the analogous statements are true for every open subset 
$U \subset X$ this defines a [[sheaf]] of [[Lie groupoid]]s 
$$
  Funct^\infty(P_1(-), \mathbf{B}U(1)) : Op(X)^{op} \to LieGrpd
  \,.
$$
By the [[Dold-Kan correspondence]] this sheaf of groupoids
corresponds to a sheaf of complexes of groups. This complex
of sheaves is nothing but the degree 2 Deligne complex

$$
  Funct^\infty(\Pi_1(-), \mathbf{B}U(1)) \simeq \mathbb{Z}(2)^\infty_D
  \,.
$$
 
This way Deligne cohomology is realized as computing the
[[(infinity,1)-sheafification|stackification]] of the pre-stack
$Funct^\infty(P_1(-), \mathbf{B}(1))$ of smooth $U(1)$-valued 
parallel transport functors.

The identification generalizes: for all $n$ there is a smooth 
[[n-category|n-groupoid]] $P_n(X)$ whose $k$-morphisms are 
$k$-dimensional smooth paths in $X$. Smooth $n$-functors
$tra_C : _n(X) \to \mathbf{B}^n U(1)$ are canonically identified
with smooth $n$-forms $C \in \Omega^n(X)$ and 
under the [[Dold-Kan correspondence]] the Deligne-complex in degree
$n+1$ is identified with the sheaf of $n$-groupoids of such smooth 
$n$-functors
$$
  n Funct^\infty(P_n(-), \mathbf{B}^n)
  \simeq
  \mathbb{Z}(n+1)^\infty_D
  \,.
$$

See

* John Baez, Urs Schreiber, _Higher Gauge Theory_ ([arXiv](http://arxiv.org/abs/math/0511710))

The full proof for $n=1$ this is in

* Urs Schreiber, Konrad Waldorf, _Parallel transport and functors_ ([arXiv](http://arxiv.org/abs/0705.0452));

for $n=2$ in 

* Urs Schreiber, Konrad Waldorf, _Smooth functors versus differential forms_ ([arXiv](http://arxiv.org/abs/0802.0663))

For more on this see [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].

For higher $n$ there is as yet no detailed proof in the literature, but the
low dimensional proofs have obvious generalizations.

See also 

* U. Bunke, _Index theory, eta forms, and Deligne cohomology_, Memoirs AMS, vol. 198, number 928, [arXiv:math./0201112](http://arxiv.org/abs/math/0201112v4)

* Ulrich Bunke, Thomas Schick, _Uniqueness of smooth extensions of generalized cohomology theories_, [arXiv:0901.4423](http://arxiv.org/abs/0901.4423)