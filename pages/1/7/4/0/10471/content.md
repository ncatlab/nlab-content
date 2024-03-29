
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Orthogonal spectra are one version of [[highly structured spectra]] that support a [[symmetric monoidal smash product of spectra]]. An orthogonal spectrum is a sequence of [[pointed topological spaces]] $\{X_n\}_{n \in \mathbb{N}}$ equipped with maps $X_n \wedge S^1 \longrightarrow X_{n+1}$ from the [[suspension]] of one into the next, but such that the $n$th [[topological space]] is equipped with an [[action]] of the [[orthogonal group]] $O(n)$ and such that the induced structure maps.
$X_n \wedge S^k \longrightarrow X_{n+k}$
are all $O(n)\times O(k)$-[[equivariance|equivariant]], hence are [[action]] [[homomorphisms]]. There is a natural [[homotopy theory]] of such orthogonal spectra and it is equivalent to the standard [[stable homotopy theory]] ([MMSS 98](#MMSS08)). 

The [[category]] of _orthogonal spectra_  is a [[presentable (∞,1)-category|presentation]] of the [[symmetric monoidal (∞,1)-category]] [[stable (infinity,1)-category of spectra|of spectra]], with the special property that it implements the [[smash product of spectra]] such as to yield itself a [[symmetric monoidal category|symmetric]] [[monoidal model category|monoidal]] [[model category of spectra]]: the _[[model structure on orthogonal spectra]]_. 

This implies in particular that with respect to this [[symmetric smash product of spectra]] an [[E-∞ ring]] is presented simply as a plain [[commutative monoid]] [[internalization|in]] orthogonal spectra ("[[highly structured ring spectrum]]"). See at _[[orthogonal ring spectrum]]_.

Other presentations sharing this property are _[[symmetric spectra]]_ and _[[S-modules]]_. In contrast to symmetric spectra, orthogonal spectra need to consist of [[topological spaces]] instead of [[simplicial sets]]. 

One advantages of orthogonal spectra over symmetric spectra is that for them the naive definition of [[homotopy groups]] comes out homotopically correct, while for symmetric spectra an intransparent replacement is needed first (see [symmetric spectrum -- Homotopy groups](symmetric+spectrum#HomotopyGroups)).

Another advantage is that orthogonal spectra support a similarly good model for [[equivariant stable homotopy theory]] with equivariance by [[compact Lie groups]], while [[symmetric spectra]] share this property only for equivariance under [[finite groups]].



## Definition
 {#Definition}

### Orthogonal spectra

+-- {: .num_defn #OrthogonalSpectrum}
###### Definition

An _orthogonal spectrum_ $X$ consists of for each $n \in \mathbb{N}$

1. a sequence of [[pointed topological spaces]] $X_n$ (the _$n$th level_);

1. a base-point preserving [[continuous function|continuous]] [[action]] of the [[topological group|topological]] [[orthogonal group]] $O(n)$ on $X_n$;

1. based-point preserving [[continuous functions]] $\sigma_n \colon X_n \wedge S^1 \longrightarrow X_{n+1}$ from the [[smash product]] with the [[1-sphere]] (the _$n$th structure map_)

such that for all $n,k \in \mathbb{N}$ with $k \geq 1$

* the [[continuous functions]] $\sigma^k \colon X_n \wedge S^k \longrightarrow X_{n+k}$ given as the [[compositions]]

  $$
    \sigma^k \colon
    X_n \wedge S^k  
     \stackrel{\sigma_n \wedge S^{k-1}}{\longrightarrow}
    X_{n+1} \wedge S^{k-1}
     \stackrel{\sigma_{n-1} \wedge S^{k-2}}{\longrightarrow}
    X_{n+2} \wedge S^{k-2}
     \stackrel{\sigma_{n-2} \wedge S^{k-3}}{\longrightarrow}
     \cdots
     \stackrel{\sigma_{n+k-2} \wedge S^{1}}{\longrightarrow}
   X_{n+k-1} \wedge S^1
     \stackrel{\sigma_{n+k-1} }{\longrightarrow}
    X_{n+k}  
  $$

  is $O(n) \times O(k)$-equivariant

  (with respect to the $O(k)$-[[action]] on $S^k$ regarded as the [[representation sphere]] of the defining action on $\mathbb{R}^k$ and via the diagonal embedding $O(n)\times O(k) \hookrightarrow O(n+k)$).

A [[homomorphism]] $f \colon X \longrightarrow Y$ of orthogonal spectra is a sequence of $O(n)$-equivariant based continuous functions $f_n \colon X_n \longrightarrow Y_n$ [[commuting diagram|commuting]] with the structure maps

$$
  \array{
    X_n \wedge S^1 & \stackrel{\sigma_n^X}{\longrightarrow} & X_{n+1}  
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow^{\mathrlap{f_{n+1}}}
    \\
    Y_n \wedge S^1 & \stackrel{\sigma_n^Y}{\longrightarrow} & Y_{n+1}      
  }
  \,.
$$

We write $OrthSpectra$ for the [[category]] of orthogonal spectra with homomorphisms between them.

=--




### Homotopy groups and Weak homotopy equivalences
 {#HomotopyGroups}

+-- {: .num_defn #StabilizationMap}
###### Definition

Given an orthogonal spectrum $X$, def. \ref{OrthogonalSpectrum},
then for $n,k \in \mathbb{N}$ the _stabilization map_ $\iota_{n,k}$ on [[homotopy groups]] $\pi_\bullet(X_\bullet)$ of the level spaces $X_\bullet$ is 

$$
  \iota_{n,k}
    \;\colon\;
  \pi_{n+k} X_n
    \stackrel{(-)\wedge S^1}{\longrightarrow}
  \pi_{n+k+1}(X_n \wedge S^1)
    \stackrel{(\sigma_n)_\ast}{\longrightarrow}
  \pi_{n+k+1} X_{n+1}
  \,.
$$

=--

+-- {: .num_defn #StableHomotopyGroup}
###### Definition

Given an orthogonal spectrum $X$, def. \ref{OrthogonalSpectrum}, then for $k \in \mathbb{Z}$ its $k$th _stable [[homotopy group]]_ is the [[colimit]]

$$
  \pi_k X 
  \;\coloneqq\;
  \underset{\longrightarrow}{\lim}_n
  \pi_{n+k} X_n
$$

of the [[homotopy groups]] of the level spaces, taken with respect to the stabilization maps, def. \ref{StabilizationMap}.

=--

+-- {: .num_defn #WeakHomotopyEquivalences}
###### Definition

A homomorphism $f\colon X \longrightarrow Y$ of orthogonal spectra, def. \ref{OrthogonalSpectrum}, is a _[[weak homotopy equivalence]]_ if it induces [[isomorphisms]] (of [[abelian groups]])

$$
  \pi_\bullet(f) \;\colon\;  \pi_\bullet(X) \longrightarrow \pi_\bullet(Y)
$$

on all stable homotopy groups, def. \ref{StableHomotopyGroup}.

=--

+-- {: .num_remark}
###### Remark

The [[simplicial localization]] of the category of orthogonal spectra, def. \ref{OrthogonalSpectrum}, at the weak homotopy equivalences, def. \ref{WeakHomotopyEquivalences}, is [[equivalence of (infinity,1)-categories|equivalent]] to the [[(infinity,1)-category of spectra]]:

$$
  L_{whe} OrthSpectra \simeq Spectra
  \,.
$$

See at _[[model structure on orthogonal spectra]]_.

=--

### Smash product
 {#SmashProduct}

+-- {: .num_defn #SmashProduct}
###### Definition

Given two orthogonal spectra $X,Y\in OrthSpectra$, def. \ref{OrthogonalSpectrum}, their _[[smash product of spectra]]_ is the orthogonal spectrum

$$
  X \wedge Y \in OrthSpectra
$$

whose $n$th level space is the [[coequalizer]] 

$$
  \left(
    \underset{p+1+q = n}{\bigvee}
     O(n)_+  \underset{O(p)\times 1 \times O(q)}{\wedge} X_p \wedge S^1 \wedge Y_q
  \right)
  \stackrel{\overset{}{\longrightarrow}}{\underset{}{\longrightarrow}}
  \left(
   \underset{p+q = n}{\bigvee}
    O(n)_+ \underset{O(p)\times O(q)}{\wedge} X_p \wedge Y_q
   \right)
   \longrightarrow
   \left(X\wedge Y\right)_{n}
$$

of the two maps whose components are $\sigma_p^X \wedge Y_q$ and $X_p \wedge \sigma_q^Y \circ X_p \wedge braid_{S^1, Y_q}$, respectively, and whose structure maps are induced, under the coequalizer, by the component maps $X_p\wedge \sigma_q^Y$.

=--

+-- {: .num_prop }
###### Proposition

The [[smash product of spectra]] from def. \ref{SmashProduct} naturally extends to a [[functor]]

$$
  (-)\wedge (-)
  \;\colon\;
  OrthSpectra \times OrthSpectra
  \longrightarrow
  OrthSpectra
$$

which makes $OrthSpectra$ into a [[symmetric monoidal category]] with [[unit]] the orthogonal [[sphere spectrum]] $\mathbb{S}$, example \ref{OrthogonalSphereSpectrum}.

=--

+-- {: .num_defn #BilinearHomomorphisms}
###### Definition

For $X,Y,Z \in OrthSpectra$, def. \ref{OrthogonalSpectrum}, a _[[bilinear map|bilinear]]-homomorphism_ 
$$
  b 
    \;\colon\;
  (X,Y)
   \longrightarrow
  Z
  \,,
$$

is a collection of, for each $p,q\in \mathbb{N}$, base-point preserving $O(p) \times O(q)$-equivariant [[continuous functions]]

$$
  b_{p,q}
   \;\colon\;
  X_p \wedge Y_q 
    \longrightarrow
  Z_{p+q}
$$

(out of the [[smash product]] of [[pointed topological spaces]]) which are _[[bilinear map|bilinear]]_ in that the following [[diagrams]] [[commuting diagram|commutes]]:

$$
  \array{
    X_p \wedge Y_q \wedge S^1
     &\stackrel{b_{p,q} \wedge S^1}{\longrightarrow}&
    Z_{p+q} \wedge S^1
    \\
    \downarrow^{\mathrlap{X_p \wedge \sigma_q}} 
      && 
    \downarrow^{\mathrlap{\sigma_{p+q}}}
    \\
    X_p \wedge Y_{q+1}
     &\stackrel{b_{p,q+1}}{\longrightarrow}&
    Z_{p+q+1}
  }
  \;\;\;\;,\;\;\;\;\;
  \array{
    X_p \wedge Y_q \wedge S^1
     &\stackrel{b_{p,q} \wedge S^1}{\longrightarrow}&
    Z_{p+q} \wedge S^1
    \\
    \downarrow^{\mathrlap{X_p \wedge braid_{Y_q, S^1}}}
     &&
    \downarrow^{\mathrlap{\sigma_{p+q}}}
    \\
    X_p \wedge S^1 \wedge Y_q 
     &&
    Z_{p+q+1}
    \\
    \downarrow^{\mathrlap{\sigma_{p} \wedge Y_q}} 
      && 
    \downarrow^{\mathrlap{id \times \chi_{1,q}}}
    \\
    X_{p+1} \wedge Y_{q}
     &\stackrel{b_{p+1,q}}{\longrightarrow}&
    Z_{p+1+q}
  }
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The smash product of orthogonal spectra $X \wedge Y$, def. \ref{SmashProduct}, is the [[universal construction|universal]] recipient in $OrthSpectra$ of bilinear maps, def. \ref{BilinearHomomorphisms}, out of $(X,Y)$.

=--

## Examples

+-- {: .num_example #OrthogonalSphereSpectrum}
###### Example

The canonical incarnation of the [[sphere spectrum]] $\mathbb{S}$ as an orthogonal spectrum, def. \ref{OrthogonalSpectrum}, has $n$th level space

$$
  \mathbb{S}_n = S^n
$$

the [[representation sphere]] of the defining [[linear representation]] of $O(n)$ on $\mathbb{R}^n$, and as structure maps the canonical [[smash product]] [[isomorphisms]] ([[homeomorphisms]])

$$
  S^p \wedge S^1  \longrightarrow S^{p+1}
  \,.
$$

=--


## Properties


### Relation to the J-homomorphism

relation to the [[J-homomorphism]]:

see ([Schwede 15, example 4.22](#Schwede15))


### Relation to the cobordism hypothesis

> check

A [[connective spectrum]] is equivalently a grouplike [[E-∞ space]], hence a [[Picard ∞-groupoid]]. As such it is an [[(∞,0)-category]] of [[fully dualizable objects]]. By the [[cobordism hypothesis]] this means that it is equipped with an $O(n)$-[[∞-action]] for all $n$, coming from the action $O(n)$ on the [[framed manifold|n-framings]] of the point in the [[(∞,n)-category of cobordisms]]. This $O(n)$-action is that which is encoded by the definition of orthogonal spectrum ([Lurie 09, example 2.4.15](#Lurie09)).




### Relation to global equivariant stable homotopy theory

Since orthogonal spectra are by definition equipped with orthogonal group [[actions]], they serve as models for [[equivariant homotopy theory]] "for all groups at once", called _[[global stable homotopy theory]]_.

## Related concepts

* [[free orthogonal spectrum]]

* [[orthogonal ring spectrum]]

[[model structure on spectra]], [[symmetric monoidal smash product of spectra]]

* [[symmetric spectrum]], [[model structure on symmetric spectra]]

* **orthogonal spectrum**, [[model structure on orthogonal spectra]]

* [[S-module]], [[model structure on S-modules]]


* [[global equivariant stable homotopy theory]]

## References

Reviews include

* Knut Berg, _Orthogonal spectra_ ([pdf](http://folk.uio.no/rognes/theses/orthogonal.pdf))

* {#Malkiewich14} [[Cary Malkiewich]], section 2.3 of _The stable homotopy category_, 2014 ([pdf](https://people.math.binghamton.edu/malkiewich/stable.pdf), [[MalkiewichStableHomotopyCategory.pdf:file]])

Lecture notes include

* {#Schwede12} [[Stefan Schwede]], chapter I, section 7.1 of _[[Symmetric spectra]]_ (2012)

* {#Schwede14} [[Stefan Schwede]], section 1 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2014 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

and ([Schwede 15](#Schwede15)) (take throughout $\mathcal{F} = \{1\}$ there to be the trivial family to restrict to the non-equivariant case).

Orthogonal spectra were introduced around

* {#MMSS98a} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _Diagram spaces, diagram spectra, and FSP's_, 1998 ([KTheory:0319](http://www.math.uiuc.edu/K-theory/0319/))

and their [[homotopy theory]] and [[Quillen equivalences]] of [[model categories of spectra]] were discussed in

* [[Michael Mandell]], [[Peter May]], _Orthogonal spectra and $S$-modules_ ([K-theory:0318](http://www.math.uiuc.edu/K-theory/0318/), [pdf](http://www.math.uchicago.edu/~may/PAPERS/mmLMSDec30.pdf))

* {#MMSS98b} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]],  _[[Model categories of diagram spectra]]_, 1998 ([KTheory:0320](http://www.math.uiuc.edu/K-theory/0320/))


and for [[equivariant spectra]] in

* {#MandellMay00} [[Michael Mandell]], [[Peter May]], _Equivariant orthogonal spectra and $S$-modules_, 2000 [KTheory:0408](http://www.math.uiuc.edu/K-theory/0408/)

and for [[operads]] enriched over orthogonal spectra in

* [[Tore Kro]], _Model structure on operads in orthogonal spectra_, Homology Homotopy Appl. Volume 9, Number 2 (2007), 397-412.([Euclid](http://projecteuclid.org/euclid.hha/1201127343))

and in the context of [[equivariant stable homotopy theory]] in ([Schwede 14](#Schwede14)) and in

* {#MMSS00} [[Michael Mandell]], [[Peter May]], _Equivariant orthogonal spectra and S-modules_. Preprint, April 29, 2000, ([KTheory:0408](http://www.math.uiuc.edu/K-theory/0408/))

and in [[global equivariant stable homotopy theory]]:

* {#Schwede15} [[Stefan Schwede]], _[[Global homotopy theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/global.pdf))


See also

* {#Lurie09} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_, Current Developments in Mathematics Volume 2008 (2009), 129-280 ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))


[[!redirects orthogonal spectra]]