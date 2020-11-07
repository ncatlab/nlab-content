
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#SplittingPrinciple}

In [[algebraic topology]], a _splitting principle_ for a [[classifying space]] $B G$ for some [[topological group]] $G$ ([[delooping]] of some [[∞-group]] $G$) is a map from a [[torus]]-classifying space 


$$
  B (T^n) \overset{f}{\longrightarrow} B G
$$ 

such that  the induced pullback of [[cohomology rings]] is an [[injective function]]

   $$
     f^\ast \;\colon\; H^\bullet(B G) \hookrightarrow H^\bullet(B T^n)
     \,,
   $$

   hence allowing to view the cohomology of $G$-[[principal ∞-bundles]] in terms of that of plain [[torus]]-[[principal bundles]].


In particular for $G$ a classical [[compact Lie group]] such as the [[unitary group]], the splitting principle holds and allows to express [[Chern classes]] of [[complex vector bundles]] as algebraic expressions in just [[first Chern classes]] of [[complex line bundles]].

## Statement

Let $G$ be a [[connected topological space|connected]] [[compact Lie group]] and write $U(1)^n \simeq T \stackrel{i}{\hookrightarrow} G$ for a [[maximal torus]].

Let $X$ be a [[connected topological space]] and $P \to X$ a $G$-[[principal bundle]] over $X$ [[classifying space|classified]] by a map $g \colon X \to B G$.

Then consider the [[coset space]] $G/T$ and the $G/T$-[[fiber bundle]] $Y\to X$ [[associated bundle|associated]] to $P$, this is equivalently the [[homotopy pullback]] in the diagram

$$
  \array{
    Y &\stackrel{(g_1,\cdots, g_n)}{\longrightarrow}& B T & \simeq B U(1)^n 
    \\
    \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{B i}}
    \\
    X &\stackrel{g}{\longrightarrow}& B G
  }
  \,.
$$

This diagram shows that the pullback of the $G$-principal bundle $P \to X$ along $p$ to $Y$ is equivalently a $T$-principal bundle splitting as [[circle group]]-principal bundles classified by $(g_1, \cdots, g_n)$. 

That this is a useful splitting is the content of:

+-- {: .num_theorem #GeneralizedSplittingPrinciple}
###### Theorem
**(generalized splitting principle)**

Let $R$ be a [[commutative ring]] in which a [[prime number]] $p$ is a [[unit]] if $H_\bullet(B G,\mathbb{Z})$ has a $p$-[[torsion subgroup]].

Then

1. The $H^\bullet(B G,R)$-module $H^\bullet(B T, R)$ (via $B i^\ast$) is [[free module|free]] on the cohomology of $G/T$:

   $$
     H^\bullet(B T,R)\simeq H^\bullet(B G,R) \otimes H^\bullet(G/T, R)
     \,;
   $$

1. Analogously there is an isomorphism

   $$
     H^\bullet(Y,R) \simeq H^\bullet(X,R)\otimes H^\bullet(G/T,R)
   $$

   and hence $p^\ast$ is the canonical inclusion (and hence in particular is an [[injection]])
   
   $$
     p^\ast \;\colon\;  H^\bullet(X,R)\hookrightarrow H^\bullet(Y,R)
     \,.
   $$

=--

In this general form this is due to ([May](#May)).

+-- {: .num_theorem}
###### Remark

Since the elements 

$$
  c \in H^\bullet(B G,R)
$$ 

are the [[universal characteristic classes]] of $G$-principal bundles with [[coefficients]] in $R$ (hence by [[Chern-Weil theory]] the [[invariant polynomials]] of the [[Lie algebra]] $\mathfrak{g}$ if $R$ has [[characteristic]]-0), theorem \ref{GeneralizedSplittingPrinciple}
gives the following way to express the characteristic classes of $G$-principal bundles on $X$ by [[tuples]] 
$$
  (c_1^1, \cdots, c_1^n) \coloneqq (B i)^\ast c
$$ 

of characteristic classes -- hence [[first Chern class|first Chern classes]] -- of just circle bundles ([[line bundles]]):

$$
  p^\ast (c(P)) \simeq (g_1^\ast c_1^1, \cdots, g_n^\ast c_1^n)
  \,.
$$

(Since $p^\ast$ is injective, this is a genuine characterization of $c(P)$).

=--

+-- {: .num_remark #InjectivityOfPullbackInCohomologyToBT}
###### Remark

One way to see that $B i^*\colon H^*(B G) \to H^*(B T)$ is injective is by using [[Chern-Weil theory]] to recognise that this map is just $Sym^{\ast} \mathfrak{g}^{\vee} \to Sym^{\ast} \mathfrak{t}^{\vee}$ for $G$ a compact [[Lie group]]. This tells us firstly that these cohomology rings are particularly nice.

One can define a [[Becker-Gottlieb transfer|transfer map]] $\tau\colon H^*(B T) \to H^*(B G)$ as in [this MO answer](http://mathoverflow.net/questions/61784/cohomology-of-bg-g-compact-lie-group/61943#61943), and then show, following ([Dupont 1978](#Dupont78), chapter 8), that $\tau\circ B i^*\colon H^*(B G)\to H^*(B G)$ is multiplication by the [[Euler class]] $\chi(G/T)$. Thus if $\chi(G/T) \gt 0 $ then $\tau\circ B i^*$ hence $B i^*$ is injective. One can calculate $\chi(G/T) = | N(T)/T |$, where $N(T)/T =: W_T$ is the [[Weyl group]] of the maximal torus $T$, using a [[Lefschetz trace formula|Lefshetz fixed point]]-argument, giving the result.

=--

## Examples
 {#Examples}

### Complex vectors bundles and their Chern roots
 {#ComplexVectorBundleAndTheirChernRoots}

For $G = U(n)$ the [[unitary group]], the [[universal characteristic classes]] are the [[Chern classes]] $c_k \in H^\bullet(B U(n), \mathbb{Z})$. By the discussion at _[Chern class -- Properties -- Splitting principle and Chern roots](Chern+class#SplittingPrinciple).
the universal splitting principle here says that 

$$
  (B i)^\ast(\sum_k c_k) = (1 + x_1) \cdots (1+ x_n)
  \,,
$$

where the $x_i \in H^\bullet(B U(1)^n , \mathbb{Z})$ are the universal characteristic classes of the [[maximal torus]], hence are $n$ incarnations of the universal [[first Chern class]] (equivalently: the [weights](group+character#RelationToChernRootsAndSplittingPrinciple) of the [[group characters]] of $U(n)$).
It follows that every [[complex vector bundle]] $\xi$ of [[rank]] $n$ over a space $X$ when pulled back to its [[flag space]] bundle decomposes as a [[direct sum]] of [[complex line bundles]] $\zeta_i$ and has [[Chern classes]] $c_k$ expressed in terms of the [[first Chern classes]] of these line bundles as

$$
  c_k(p^\ast \xi ) = \sigma_k(c_1(\zeta_1), \cdots, c_n(\zeta_n))
  \,.
$$

This case is what is traditionally is often meant by default by the "splitting principle".

For the [[special unitary group]] the situation is the same, only that here the splitting is into a sum of line bundles whose [[tensor product]] is constrained to be [[trivial vector bundle|trivializable]].

### Linear representations and Brauer induction

The [[Brauer induction theorem]] may be regarded as the splitting principle for [[linear representations]] ([Symonds 91](#Symonds91)), see also at _[[characteristic classes of linear representations]]_,

### Real vector bundles 
 {#RealVectorBundles}

Under the _[Relation between Pontryagin classes and Chern classes](Pontryagin+class#FurtherRelationToChernClasses)_ the above translates into a splitting principle also for [[real vector bundles]].

### Genera and Hirzebruch characteristic series

The basic theorem of [[Hirzebruch series]] expresses [[genera]] via the splitting principle. The Hirzebruch characteristic series $K_\phi$ is a [[series]] in a single variable $x = c_1(L)$, to be thought of as the [[first Chern class]] of the universal [[complex line bundle]] over $B U(1)$. 

The Hirzebruch formula for the value of the [[genus]] $\phi$ on an [[orientation|oriented]] [[manifold]] $X$

$$
  \phi(X) = \langle K_\phi(T X), [X]\rangle
$$

denotes the pairing of that class of the [[tangent bundle]] with the [[fundamental class]] which under the splitting principle pulls back on the [[flag space]] bundle to the class $\prod_k K_\phi(x_k)$ of the corresponding direct sum of line bundles.


## Related concepts

* [[Snaith's theorem]]

## References


* {#May} [[Peter May]], _A note on the splitting principle_, Topology and its Applications Volume 153, Issue 4, 1 November 2005, Pages 605-609 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Split.pdf), [doi:10.1016/j.topol.2005.02.007](https://doi.org/10.1016/j.topol.2005.02.007))

* Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 10.2 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

Discussion in the derivation of [[Chern classes]] and [[Stiefel-Whitney classes]] includes

* {#Kochmann96} [[Stanley Kochmann]], section 2.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

See also

* Wikipedia, _[Splitting principle](https://en.wikipedia.org/wiki/Splitting_principle)_

* _Notes on the splitting principle_ ([pdf](http://www.math.sunysb.edu/~azinger/mat566/splitting.pdf))

* {#Dupont78} Johan L. Dupont, _Curvature and Characteristic Classes_, Lecture Notes in Mathematics, **640** (1978) doi:[10.1007/BFb0065364](http://dx.doi.org/10.1007/BFb0065364).

Discussion in the context of [[complex oriented cohomology theory]] and their [[generalized Chern classes]] includes

* [Kochmann 96, section 4.3](#Kochmann96)

* [[Jacob Lurie]], lecture 4 of _[[Chromatic Homotopy Theory]]_, 2010 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf)) 

More expository discussion in the context of [[characteristic classes]] with applications in [[mathematical physics]] is in

* {#Zhang11} [[Yang Zhang]], _A brief introduction to characteristic classes
from the differentiable viewpoint_, 2011 ([pdf](http://www.nbi.dk/~zhang/notes/A brief introduction to characteristic classes from the differentiable viewpoint.pdf))

The generalization to a splitting principle for [[twisted vector bundles]] ([[twisted cohomology]]) is discussed (in terms of [[bundle gerbe modules]]) in 

* {#Tomoda07} [[Atsushi Tomoda]], _On the splitting principle of bundle gerbe modules_, Osaka J. Math. Volume 44, Number 1 (2007), 231-246. ([Euclid](https://projecteuclid.org/euclid.ojm/1174324334), talk slides [pdf](http://ton.prosou.nu/official/ryousi2005.pdf))

For [[characteristic classes of linear representations]]:

* {#Symonds91} [[Peter Symonds]], _A splitting principle for group representations_, Comment. Math. Helv. (1991) 66: 169 ([doi:10.1007/BF02566643](https://doi.org/10.1007/BF02566643))

[[!redirects Chern root]]