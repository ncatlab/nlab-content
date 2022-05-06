
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Summary

The _Tietze extension theorem_ says that [[continuous functions]] [[extension|extend]] from [[closed subsets]] of a [[normal topological space]] $X$ to the whole space $X$. 

This is a close cousin of [[Urysohn's lemma]] with many applications.

One implication is that [[topological vector bundles]] over a topological space $X$ that trivialize over a [[closed subspace]] $A$ are equivalent to vector bundles on the [[quotient space]] $X/A$ (see [there](topological+vector+bundle#OverClosedSubspaces)). This in turn is what implies the [[long exact sequence in cohomology]] for [[topological K-theory]] (see [there](topological+K-theory#ExactSequences)).



## Statement 

### For continuous functions
 {#ForContinuousFunctions}


+-- {: .num_theorem}
###### Theorem

For $X$ a [[normal topological space]] and $A \subset X$ a [[closed subspace]], there is for every [[continuous function]] $f \colon A \to \mathbb{R}$ to the [[real line]] (with its [[Euclidean space|Euclidean]] [[metric topology]]) a continuous function $\hat f \colon X \to \mathbb{R}$ [[extension|extending]] it, i.e. such that $\hat f|_A = f$:

$$
  \array{
     A &\hookrightarrow & X
     \\
     {}^{\mathllap{f}}\downarrow & \swarrow_{\mathrlap{\exists \hat f} } 
     \\
     \mathbb{R}
  }
$$

Therefore one also says that _$\mathbb{R}$ is an [[absolute extensor]]_ in [[topology]].

=--

+-- {: .proof}
###### Proof


We produce a [[sequence]] of approximations to the desired extension by [[induction]]. Then we will observe that the sequence is a [[Cauchy sequence]] and conclude by observing that this implies that it [[limit of a sequence|limit]] is an extension of $f$ as desired.


For the induction step, let 

$$
  \hat f_n \;\colon\; X \longrightarrow \mathbb{R}
$$

be a [[continuous function]] on $X$ such that the difference of its restriction to $A$ with $f$ is a [[bounded function]], for a bound $c_n \in (0,\infty) \subset \mathbb{R}$:

$$
  \underset{a \in A}{\forall} 
  \left( 
    { \left\Vert f(a) - \hat f_n (a) \right\Vert } \leq c_n
  \right)
  \,.
$$

Consider then the [[pre-image]] subsets 

$$
  S_- \coloneqq \left( f - \hat f_n\vert_A \right)^{-1}\big( [-c_n, -c_n/3] \big) 
  \phantom{AAAA}
  S_+ \coloneqq \left( f - \hat f_n\vert_A \right)^{-1}\big( [c_n/3, c_n] \big)
  \,.
$$

Since the [[closed intervals]] $[-c_n,-c_n/3], [c_n/3, c_n] \subset \mathbb{R}$ are [[closed subsets]], and since $f - \hat f_n\vert_A$ is a [[continuous function]], these are [[closed subsets]] of $A$. Moreover, since [[subsets are closed in a closed subspace precisely if they are closed in the ambient space]], these are also closed subsets of $X$.

Therefore, since $X$ is [[normal topological space|normal]] by assumption,  it follows with [[Urysohn's lemma]] that there is a continuous function

$$
  \phi \;\colon\; X \longrightarrow \mathbb{R}
$$

with 

$$
  \underset{x \in X}{\forall} \left( 0 \leq \phi(x) \leq 1 \right)
$$

and

$$
  \phi\vert_{S_+} = 1
  \phantom{AAAA}
  \phi\vert_{S_-} = 0
  \,.
$$

Consider then the continuous function

$$
  g_{n+1}
    \;\coloneqq\;
  \tfrac{2 c_n}{3} \phi
    - 
  \tfrac{c_n}{3}
$$

This now satisfies

$$
  g_{n+1}\vert_{S_+} = \frac{c_n}{3}
  \phantom{AAAA}
  g_{n+1}\vert_{S_-} = -\frac{c_n}{3}
  \,.
$$

with

$$
  \underset{x \in X}{\forall} \left( 
    \left \Vert g_{n+1} (x) \right\Vert 
     \leq 
    \tfrac{c_n}{3}
  \right)
  \,.
$$

Moreover, observe that this function satisfies

$$
 \underset{a \in A}{\forall} 
 \left(
    \left\Vert f - \hat f_n(a) - g_{n+1}(a)  \right\Vert
    \leq \tfrac{2 c_n}{3}
 \right)
 \,.
$$

To wit, this is because

1. for $a \in S_+$ we have $g_{n+1}(a) = \tfrac{c_n}{3}$ and $f(a) - \hat f_{n}(a) \in [c_n/3,c_n]$;

1. for $a \in S_-$ we have $g_{n+1}(a) = -\tfrac{c_n}{3}$ and $f(a) - \hat f_{n}(a) \in [-c_n/3,-c_n]$;

1. for $a \in Y \setminus \{S_+ \cup S_-\}$ we have $g(a) \in [-c_n/3,c_n/3]$ as well as $f(a) - \hat f_{n}(a) \in [-c_n/3, c_n/3]$.


It follows that if we set

$$
  \hat f_{n+1} \coloneqq \hat f_n + g_{n+1}
$$

then

$$
  \underset{a \in A}{\forall}
  \left(
     { \left\Vert f(a) - \hat f_{n+1}(a) \right\Vert }
     \leq 
     \tfrac{2 c_n}{3}
  \right)
  \,.
$$

This gives the induction step.

To start the induction, first assume that $f$ is bounded by a constant $c_0$. Then we may set 

$$
  \hat f_0 \coloneqq const_0
  \,.
$$

Hence [[induction]] now gives a [[sequence]] of continuous functions

$$
  (\hat f_n)_{n \in \mathbb{N}}
$$

with the property that 

$$
  \underset{a \in A}{\forall} 
  \left(
    \left\Vert f(a) -\hat f_n(a) \right\Vert
    \leq \left( \tfrac{2}{3}\right)^n c_0
  \right)
  \,.
$$

Moreover, for $n_1, n_2 \in \mathbb{N}$ with $n_2 \geq n_1$ and $x \in X$ we have 

$$
  \begin{aligned}
    {\Vert \hat f_{n_2}(x) - \hat f_{n_1}(x) \Vert}
    & = 
    {\Vert g_{n_1 + 1}(x) + g_{n_1 + 2}(c) + \cdots + g_{n_2}(x) \Vert}
    \\
    & \leq
    \underoverset{k = n_1+1}{n_2}{\sum}
    \tfrac{1}{3^{k}} c_0
    \\
    & \leq
    \underoverset{k = n_1+1}{\infty}{\sum}
    \tfrac{1}{3^{k}} c_0
  \end{aligned}
$$

That the [[geometric series]] $\sum_{k = 0}^\infty 1/3^k$ [[convergence of a sequence|converges]]

$$
  \underoverset{n}{k = 0}{\sum} 1/3 k
   \overset{n \to \infty}{\longrightarrow}
  \frac{1}{1 - 1/3} = 3/2
$$

this becomes arbitrarily small for large $n_1$. 

This means that the sequence $(\hat f_{n+1})_{n\in \mathbb{N}}$ is a [[Cauchy sequence]] in the [[supremum norm]] for real-valued functions.

Since uniform Cauchy sequences of continuous functions with values in a [[complete space|complete]] [[metric space]] [[uniform convergence|converge uniformly]] to a [[continuous function]] ([this prop.](uniform+convergence#FunctionsUniformCauchySequence)) this implies that the sequence [[uniform convergence|converges uniformly]] to a [[continuous function]]. By construction, this is an extension as required.

Finally consider the case that $f$ is not a [[bounded function]]. In this case consider any [[homeomorphism]] $\phi \colon \mathbb{R}^1 \overset{\simeq}{\to} (-c_0,c_0) \subset \mathbb{R}^1$ between the [[real line]] and an [[open interval]] Then $\phi \circ f$ is a continous function bounded by $c_0$ and hence the above argument gives an extension $\widehat {\phi \circ f}$. Then $\phi^{-1} \circ \widehat{ \phi \circ f }$ is an extension of $f$.


=--

### For smooth functions 
 {#Manifolds}

See _[[Whitney extension theorem]]_, also _[[Steenrod-Wockel approximation theorem]]_.

### For smooth loci 

Let $\mathbb{L} = (C^\infty Ring^{fin})^{op}$ be the category of [[smooth loci]],
the [[opposite category]] of finitely generated [[generalized smooth algebra]]s.
By the theorem discussed there, there is a [[full and faithful functor]]
[[Diff]] $\hookrightarrow \mathbb{L}$.

+-- {: .num_defn}
###### Definition

For $A = C^\infty(\mathbb{R}^n)/J$ and $B = C^\infty(\mathbb{R}^n)/I$
with $I \subset J$ and $B \to A$ the projection of [[generalized smooth algebra]]s
the corresponding [[monomorphism]] $\ell A \to \ell B$ in $\mathbb{L}$ 
exhibits $\ell A$ as a **closed smooth sublocus** of $\ell B$.

=--

+-- {: .num_lemma}
###### Lemma

Let $X$ be a [[smooth manifold]] and let $\{g_i \in C^\infty(X)\}_{i = 1}^n$ be [[smooth function]]s that are independent in the sense that at each common zero point $x\in X$, $\forall i : g_i(x)= 0$ we have the [[derivative]] $(d g_i) : T_x X \to \mathbb{R}^n$ is a surjection, then the ideal $(g_1, \cdots, g_n)$ coincides with the ideal of functions that vanish on the zero-set of the $g_i$.

=--

This is lemma 2.1 in Chapter I of ([MoerdijkReyes](#MoerdijkReyes)).

+-- {: .num_prop}
###### Proposition

If $\ell A \hookrightarrow \ell B$  is a closed
sublocus of $\ell B$ then every morphism $\ell A \to R$
extends to a morphism $\ell B \to R$


=--

This is prop. 1.6 in Chapter II of ([MoerdijkReyes](#MoerdijkReyes)).

+-- {: .proof}
###### Proof


Since we have $R = \ell C^\infty(\mathbb{R})$ and $C^\infty(\mathbb{R})$
is the free [[generalized smooth algebra]] on a single generator,
a morphism $\ell A \to R$ is precisely an element of $C^\infty(\mathbb{R}^n)/J$. This is represented by an element in $C^\infty(\mathbb{R}^n)$ which in particular defines an element in $C^\infty(\mathbb{R}^n)/I$.

=--

## Related theorems

[[!include extension theorems -- table]]

* [[Urysohn's lemma]]

* [[Hadamard lemma]]

* [[Borel's theorem]]

* [[Steenrod-Wockel approximation theorem]]

* [[Whitney extension theorem]]

* [[Taimanov theorem]]

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[smooth Serre-Swan theorem]]

* [[derivations of smooth functions are vector fields]]



## References

Leture notes include

* Adam Boocher, _A proof of the Tietze Extension Theorem Using Urysohn's Lemma_, 2005 ([pdf](http://www.maths.ed.ac.uk/~aboocher/math/tietze.pdf))

Discussion via [[algebraic topology]]:

* [[Norman Steenrod]], _Cohomology operations, and obstructions to extending continuous functions_, Advances in Mathematics Volume 8, Issue 3, June 1972, Pages 371-416 (<a href="https://doi.org/10.1016/0001-8708(72)90004-7">doi:10.1016/0001-8708(72)90004-7</a>, [pdf](http://www.maths.ed.ac.uk/%7Eaar/papers/steen6.pdf))

Discussion of the smooth version includes

* {#MoerdijkReyes} [[Ieke Moerdijk]], [[Gonzalo Reyes]], chapters I and II of: _[[Models for Smooth Infinitesimal Analysis]]_


See also

* Wikipedia, _[Tietze extension theorem](https://en.wikipedia.org/wiki/Tietze_extension_theorem)_

* [[Planet Math]], _[Proof of the Tietze extension theorem](http://planetmath.org/proofoftietzeextensiontheorem)_


