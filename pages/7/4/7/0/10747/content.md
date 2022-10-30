
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Symmetric spectra are one version of [[highly structured spectra]] that support a [[symmetric monoidal smash product of spectra]]. A _symmetric spectrum_ is a sequence of [[topological spaces]]/[[simplicial sets]] which are compatibly equipped with an [[action]] of the [[symmetric group]].

The [[category]] of _symmetric spectra_ is a [[presentable (∞,1)-category|presentation]] of the [[symmetric monoidal (∞,1)-category]] [[stable (infinity,1)-category of spectra|of spectra]], with the special property that it implements the [[smash product of spectra]] such as to yield itself a [[symmetric monoidal category|symmetric]] [[monoidal model category|monoidal]] [[model category of spectra]]: the _[[model structure on symmetric spectra]]_. This implies in particular that with respect to this [[symmetric smash product of spectra]] an [[E-∞ ring]] is presented simply as a plain [[commutative monoid]] [[internalization|in]] symmetric spectra. This is of course such that truncating down to the [[homotopy category]] yields equivalently the [[stable homotopy category]] with its usual [[smash product of spectra]].


The main technical issue with symmetric spectra is that the naive definition of [[homotopy groups]] for them is not general homotopy correct, one needs to replace by a "semistable symmetric spectrum" first, see [below](#HomotopyGroups). This problem goes away for [[orthogonal spectra]] (these however need to be based on [[topological spaces]] instead of [[simplicial sets]]).

## Definition

### In components
 {#InComponents}

A symmetric spectrum is a [[sequential spectrum]] equipped with an [[action]] of the [[symmetric group]] on each component space, such that the structure maps [[intertwiner|intertwine]] these actions combined with the canonical permutation action on the [[n-spheres]]:

+-- {: .num_defn #SymmetricSpectrum}
###### Definition

A **symmetric spectrum** $X$ in [[sSet]] is

1. a sequence $\{X_n| n \in \mathbb{N}\}$ of [[pointed object|pointed]] [[simplicial sets]];

1. a baspoint preserving left [[action]] of the [[symmetric group]] $\Sigma_n$ on $X_n$;

1. a sequence of morphisms of pointed simplicial sets $\sigma_n \colon X_n \wedge S^1 \longrightarrow X_{n+1}$ 

such that

* for all $n, k \in \mathbb{N}$ the [[composition|composite]]

  $$
    X_n \wedge S^{k} \stackrel{\sigma_n \wedge id}{\longrightarrow} X_{n+1} \wedge S^{k-1} \stackrel{\sigma_{n+1}\wedge id}{\longrightarrow} \cdots \stackrel{\sigma_{n+k-1}}{\longrightarrow} X_{n+k}
  $$

  [[intertwiner|intertwines]] the $\Sigma_{n+k}$-[[action]].

A [[morphism]] of symmetric spectra $f\colon X \longrightarrow Y$ is

* a sequence of morphisms of pointed simplicial sets $f_n \colon X_n \longrightarrow Y_n$

such that

1. each $f_n$ [[intertwiner|intetwines]] the $\Sigma_n$-[[action]];

1. the following [[commuting diagram|diagrams commute]]

   $$
     \array{
        X_n \wedge S^1 &\stackrel{f_n \wedge id}{\longrightarrow}& Y_n \wedge S^1
        \\
        \downarrow^{\mathrlap{\sigma^X_n}} && \downarrow^{\mathrlap{\sigma^Y_n}}
        \\
        X_{n+1} &\stackrel{f_{n+1}}{\longrightarrow}& Y_{n+1}
     }
     \,.
   $$

=--

([Hovey-Shipley-Smith 00, def. 1.2.1](HoveyShipleySmith00), [Schwede 12, def. 1.1](#Schwede12))

### As $\mathbb{S}_{Sym}$-modules
 {#AsSModules}

A more concise equivalent formulation is the following:

+-- {: .num_defn #SphereSpectrumAsDayConvolutionMonoidOverSym}
###### Definition

Write $Sym$ for the standard [[skeletal category|skeleton]] of the [[core]] of [[FinSet]], with [[objects]] labeled by [[natural numbers]], all morphisms [[automorphisms]] and the automorphisms of $n$ forming the [[symmetric group]] $\Sigma_n$. The [[disjoint union]] monoidal structure on [[FinSet]] gives $Sym$ the structure of a [[monoidal category]] with tensor product given by addition of natural numbers on objects.

Write $[Sym,sSet^{\ast/}]$ for the [[functor category]] equipped with the induced [[Day convolution]] product. Write

$$
  \mathbb{S}_{Sym} \in [Sym,sSet^{\ast/}]
$$

for the functor which sends $n$ to the minimal simplicial [[n-sphere]] $S^n = (S^1)^{\wedge^n}$ and which sends elements of the symmetric group to the corresponding endomorphisms of $S^n$ exchanging [[smash product]] factors.

Regard $\mathbb{S}_{Sym}$ as a [[monoid object]] with respect to [[Day convolution]], whose monoidal structure is given via the [discussion there](Day+convolution#Monoids) by the system of canonical natural morphisms

$$
  S^{n_1}\wedge S^{n_2} \longrightarrow S^{n_1 + n_2}
  \,.
$$


=--

+-- {: .num_defn #SymmetricSpectrumAsSModule}
###### Proposition

Symmetric spectra in the sense of def. \ref{SymmetricSpectrum} are equivalently right [[module objects]] in $([Sym,sSet^{\ast/}], \otimes_{Day})$ over the [[monoid object]] $\mathbb{S}_{Sym}$, according to def. \ref{SphereSpectrumAsDayConvolutionMonoidOverSym}:

$$
  SymSpec(sSet)
  \simeq
  \mathbb{S}_{Sym}Mod_r
  \,.
$$

=--

This point of view was highlighted and almost made explicit in ([Mandell-May-Schwede-Shipley 01](#MandellMaySchwedeShipley01)).

+-- {: .proof}
###### Proof

By the discussion [there](Day+convolution#Monoids), right $\mathbb{S}_{Sym}$-modules with respect to [[Day convolution]] are equivalently right [[modules over monoidal functors]] over the monoidal functor corresponding to $\mathbb{S}_{Sym}$ as in def. \ref{SphereSpectrumAsDayConvolutionMonoidOverSym}. This means that they are functors $X \colon Sym \longrightarrow sSet^{\ast/}$ equipped with [[natural transformations]]

$$
  X_p \wedge S^{q}  \longrightarrow X_{p+q}
$$

satisfying the evident [[categorification|categorified]] [[action]] property. In the present case this action property says that these morphisms are determined by 

$$
  X_p \wedge S^1 \longrightarrow X_{p+1}
$$

under the isomorphisms $S^p \simeq S^1 \wedge S^{p-1}$. Naturality of all these morphisms as functors on $Sym$ is the equivariance under the symmetric group actions in def. \ref{SymmetricSpectrum}.


=--

For more on this see at _[[Model categories of diagram spectra]] -- [part I](Model%20categories%20of%20diagram%20spectra#PartI)_.

## Properties

### Smash product
 {#SmashProduct}

[[smash product of spectra]] modeled on symmetric spectra

e.g. ([Schwede 12, I.3](#Schwede12))

### Homotopy groups
 {#HomotopyGroups}

The main technical issue with symmetric spectra is that the evident definition of [[stable homotopy groups]] of symmetric spectra $X$ as 

$$
  \pi_n(X) = \underset{\longrightarrow}{\lim}_k \pi_{k+n}(X_k)
$$

does _not_ in general come out in the homotopy correct way; instead one needs to replace by a "semistable symmetric spectrum" first, which however is hard to control ([Hovey-Shipley-Smith 00, section 3.1](#HoveyShipleySmith00), [Schwede 12, chapter I, sections 2 and 6 and 8](#Schwede12)), survey includes ([Malkiewich 14, section 2.3](#Malkiewich14)). 

Among the various (now) common models for [[spectra]], this issue is unique to symmetric spectra, see also the comment in ([Mandell-May-Schwede-Shipley 01, p. 3](#MandellMaySchwedeShipley01)).

In particular, this problem goes away for the concept of [[orthogonal spectra]], which otherwise is very similar to that of symmetric spectra and shares most of its advantages (except that it does not admit a version based on [[simplicial sets]]).

Technically, the issue comes down to the fact that the [[quotients]] of [[symmetric groups]] $\Sigma_q/\Sigma_{q-n}$ do not become highly connected for large $q$ the way the quotients $O(q)/O(n-q)$ of [[orthogonal groups]] do ([Mandell-May-Schwede-Shipley 01, proof of lemma 8.6, top of p. 26](#MandellMaySchwedeShipley01)).

## Related concepts

[[model structure on spectra]], [[symmetric monoidal smash product of spectra]]

* **symmetric spectrum**, [[model structure on symmetric spectra]]

* [[orthogonal spectrum]], [[model structure on orthogonal spectra]]

* [[S-module]], [[model structure on S-modules]]

## References

The orginal article is

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))

A comprehensive textbook account is in 

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

Further discussion of the [[model structure on symmetric spectra]] beyond ([Hovey-Shipley-Smith 00](#HoveyShipleySmith00)) and [Schwede 12, part III](#Schwede12) includes

* {#MandellMaySchwedeShipley01} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))


More or less brief reviews include

* {#Malkiewich14} [[Cary Malkiewich]], section 2.3 of _The stable homotopy category_, 2014 ([pdf](http://math.stanford.edu/~carym/stable.pdf))

* [[Alexander Kupers]], _Symmetric spectra_ ([pdf](http://ncatlab.org/nlab/files/SymmetricSpectra.pdf))

* [[Mitya Boyarchenko]], _Introduction to symmetric spectra_ (prepared for a [Geometric Langlands Seminar](http://www.math.uchicago.edu/~mitya/langlands.html)) Part I ([pdf](http://www.math.uchicago.edu/~mitya/langlands/spectra/iss1.pdf)) and Part II ([pdf](http://www.math.uchicago.edu/~mitya/langlands/spectra/iss2.pdf)) 


[[!redirects symmetric spectra]]