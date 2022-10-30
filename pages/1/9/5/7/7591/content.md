
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The generalization in [[(∞,1)-category theory]] of the notion of _[[group of units]]_ in ordinary category theory.

## Definition

### Unaugmented definition

+-- {: .num_defn #PlainInfinityGroupOfUnits}
###### Definition

Let $A$ be an [[A-∞ algebra|A-∞]] [[ring spectrum]]. 

For $\Omega^\infty A$ the underlying [[A-∞ space]] and $\pi_0 \Omega^\infty A$ the ordinary [[ring]] of connected components, write $(\pi_0 \Omega^\infty A)^\times$ for its [[group of units]]. 

Then the [[∞-group of units]] 

$$
  A^\times \coloneqq GL_1(A)
$$

of $A$ is the [[(∞,1)-pullback]] $GL_1(A)$ in

$$
  \array{
    GL_1(A) &\to& \Omega^\infty A
    \\
    \downarrow && \downarrow
    \\
    (\pi_0 \Omega^\infty A)^\times &\to& \pi_0 \Omega^\infty A
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

In terms of [[derived algebraic geometry]] one has that 

$$
  GL_1(A) \simeq \mathbb{G}_m(A) = Hom(Spec A, \mathbb{G}_m)
$$

is the [[mapping space]] from $Spec A$ into the [[multiplicative group]].
This point of view is adopted for instance in ([Lurie, p. 20](#Lurie)).

=--

### Augmented definition
 {#AugmentedDefinition}

There is slight refinement of the above definition, which essentially adds one 0-th "grading" homotopy group to $B gl_1(E)$ and thereby makes the $\infty$-group of units of [[E-∞ rings]] be canonically [[augmented ∞-group|augmented]] over the [[sphere spectrum]] ([Sagave 11](#Sagave11)).

+-- {: .num_defn #AugmentedGroupOfUnits}
###### Definition

There is a functor

$$
  gl_1^J \colon CRing_\infty \to AbGrp_\infty/\mathbb{S}
  \,,
$$

given by ...

=--

([Sagave 11, def. 3.14](#Sagave11))

+-- {: .num_theorem}
###### Theorem

For $E$ an [[E-∞ ring]], there is a [[homotopy fiber sequence]] of [[abelian ∞-groups]]

$$
  gl_1(E) \to gl_1^J(E) \to \mathbb{S}
  \,,
$$

where on the left we have the ordinary $\infty$-group of units of def. \ref{PlainInfinityGroupOfUnits} and on the right we have the [[sphere spectrum]], regarded (being a [[connective spectrum]]) as an [[abelian ∞-group]].

=--

Here the existence of the map $gl_1(E) \to gl_1^J(E)$ is ([Sagave 11, lemma 2.12 + lemma 3.16 ](#Sagave11)). The fact that the resulting sequence is a homotopy fiber sequence is ([Sagave 11, prop. 4.1](#Sagave11)).


Using this, there is now a modified delooping of the ordinary $\infty$-group of units:

+-- {: .num_defn}
###### Definition

Write $bgl_1^\ast(E)$ for the [[homotopy cofiber]] of $gl_1^J(E) \to \mathbb{S}$ to yield

$$
  gl_1(E) \to gl_1^J(E) \to \mathbb{S} \to bgl_1^\ast(E)
  \,.
$$

=--

([Sagave 11, prop. 4.3](#Sagave11))


+-- {: .num_remark}
###### Remark

It ought to be true that the non-connective delooping $bgl_1^\ast(E)$ is equivalent to or at least closely related to the [[Picard ∞-group]] of $E Mod$. ([Sagave 11, remark 4.11](#Sagave11)).

See also at _[twisted cohomology -- by R-module bundles](twisted+cohomology#InfSections)_.


=--


## Properties
 {#Properties}

### Adjointness to $\infty$-group $\infty$-ring
 {#AdjointnessToGroupRing}

####  Unaugmented case

+-- {: .num_defn #GroupOfUnitsFunctor} 
###### Definition

Write

$$
  gl_1 \; \colon \;  CRing_\infty \to AbGrp_\infty
$$

for the [[(∞,1)-functor]] which sends a [[E-∞ ring|commutative ∞-ring]] to its [[∞-group of units]]. 

=--

+-- {: .num_theorem}
###### Theorem

The [[∞-group of units]] [[(∞,1)-functor]] of def. \ref{GroupOfUnitsFunctor} is a  right-[[adjoint (∞,1)-functor]]

$$
  CRing_\infty 
  \stackrel{\overset{\mathbb{S}[-]}{\leftarrow}}{\underset{gl_1}{\to}}
  AbGrp_\infty
  \,.
$$

=--

This is ([ABGHR 08, theorem 2.1/3.2, remark 3.4](#ABGHR08)).

+-- {: .num_remark} 
###### Remark

The [[left adjoint]]

$$
  \mathbb{S}[-] \colon AbGrp_\infty \to CRing_\infty
$$

is a higher analog of forming the [[group ring]] of an ordinary [[abelian group]] over the [[integers]] 

$$
  \mathbb{Z}[-] \colon Ab \to CRing
  \,,
$$

which is indeed [[left adjoint]] to forming the ordinary [[group of units]] of a ring.

We might call $\mathbb{S}[A]$ the spring **[[∞-group ∞-ring]]** of $A$ over the [[sphere spectrum]].

=--

####  Augmented case

Also the augmented $\infty$-group of units functor of def. \ref{AugmentedGroupOfUnits} is a homotopy right adjoint. ([Sagave 11, theorem 1.8](#Sagave11)).

### Homotopy groups

The [[homotopy groups]] of $GL_1(E)$ are

$$
  \pi_n(GL_1(E))
  = 
  \left\{
    \array{
       \pi_0(E)^\times & |\, n = 0
       \\
       \pi_n(E) & | \, n \geq 1
    }
  \right.
$$

### Cohomology and logarithm
 {#CohomologyAndLogarithm}

Given $E$ an [[E-∞ ring]], then write $gl_1(E)$ for its $\infty$-group of units regarded as a [[connective spectrum]]. For $X$ the [[homotopy type]] of a  [[topological space]], then the [[cohomology]] [[Brown representability theorem|represented]] by $gl_1(E)$ in degree 0 is the ordinary [[group of units]] in the [[cohomology ring]] of $E$:

$$
  H^0(X, gl_1(E))  \simeq (E^0(X))^\times
  \,.
$$

In positive degree the canonical map of pointed homotopy types $GL_1(E) = \Omega^\infty gl_1(E) \to \Omega^\infty E$ is in fact an [[isomorphism]] on all [[homotopy groups]]

$$
  \pi_{\bullet \geq 1} GL_1(E) \simeq \pi_{\bullet \geq 1} \Omega^\infty E
  \,.
$$

On cohomology elements this map

$$
  \pi_q(gl_1(E)) \simeq \tilde H^0(S^q, gl_1(E)) \simeq  (1+ \tilde R^0(S^q))^\times \subset (R^0(S^q))^\times
$$

is [[logarithm]]-like, in that it sends $1 + x \mapsto x$.

But there is not a homomorphism of [[spectra]] of this form. This only exists after [[K(n)-local stable homotopy theory|K(n)-localization]], where it is called then the [[logarithmic cohomology operation]], see there for more.

([Rezk 06](#Rezk06))

### Relation to Picard $\infty$-group and Brauer $\infty$-group

Given an [[E-∞ ring]] $E$, the [[looping]] of the Brauer $\infty$-group is the [[Picard ∞-group]] ([Szymik 11, theorem 5.7](#Szymik11)). 

$$
  \Omega Br(E) \simeq Pic(E).
$$

The [[looping]] of that is the ∞-group of units ([Sagave 11, theorem 1.2](#Sagave11)).

$$
  \Omega^2 Br(E) \simeq \Omega Pic(E) \simeq GL_1(E)
  \,.
$$

## Examples

### Snaith's theorem and the units of K-theory and complex cobordism
 {#SnatihTheorem}

[[Snaith's theorem]] asserts that 

1. the [[K-theory spectrum]] for [[complex K-theory]] is the [[∞-group ∞-ring]] of the [[circle 2-group]] localized away from the [[Bott element]] $\beta$:

   $$
     KU \simeq (\mathbb{S}[B U(1)])[\beta^{-1}]
     \,;
   $$

1. the [[periodic complex cobordism spectrum]] is the [[∞-group ∞-ring]] of the [[classifying space]] for stable [[complex vector bundles]] (the classifying space for [[topological K-theory]]) localized away from the [[Bott element]] $\beta$:

   $$
     MU \simeq (\mathbb{S}[B U])[\beta^{-1}]
     \,.
   $$

### Units of topological modular forms

Analysis of the $\infty$-group of units of [[tmf]] is in ([Ando-Hopkins-Rezk 10, from section 12 on](#AndoHopkinsRezk10)).

### Inclusion of circle $n$-bundles into higher chromatic cohomology

By [Snaith's theorem](#SnatihTheorem) above there is a canonical map

$$
  B U(1) \to \mathbb{S}[B U(1)] \to  KU
$$

that sends [[circle bundles]] to cocycles in [[topological K-theory]]. 

At the next level there is a canonical map

$$
  B^2 U(1) \to \mathbb{S}[B^2 U(1)] \to tmf
$$

that sends [[circle 2-bundles]] to [[tmf]]. See at _[tmf -- Inclusion of circle 2-bundles](tmf#InclusionOfCircle2Bundles)_.

Write $gl_1(K(n))$ for the [[∞-group of units]] of the (a) 
[[Morava K-theory]] spectrum.

+-- {: .num_prop}
###### Proposition

For $p = 2$ and all $n \in \mathbb{N}$, there is an [[equivalence in an (infinity,1)-category|equivalence]]

$$
  Maps(B^{n+1}U(1), B gl_1(K(n)))
  \simeq
  \mathbb{Z}/(2)
$$

between the [[mapping space]] from the [[classifying space]] for [[circle n-bundle|circle (n+1)-bundles]] to the [[delooping]] of the [[∞-group of units]] of $K(n)$.

=--

([Sati-Westerland 11, theorem 1](#SatiWesterland11))

+-- {: .num_remark}
###### Remark

By the discussion at [[(∞,1)-vector bundle]] this means that for each such map there is a type of [[twisted cohomology|twist]] of Morava K-theory (at $p = 2$).

=--



## Related concepts

* [[(∞,1)-vector bundle]]

## References

A notion of spectrum of units of an $E_\infty$-ring was originally described in 

* [[Peter May]], _$E_\infty$ ring spaces and $E_\infty$ ring spectra_  Lecture Notes in Mathematics, Vol. 577. Springer-Verlag, Berlin, 1977. With contributions by [[Frank Quinn]], Nigel Ray, and J&#248;rgen Tornehave.

One explicit model was given in

* Christian Schlichtkrull, _Units of ring spectra and their traces in algebraic K-theory_, Geom. Topol. 8(2004) 645-673 ([arXiv:math/0405079](http://arxiv.org/abs/math/0405079))
 {#Schlichtkrull04}

A general abstract discussion in [[stable (∞,1)-category]] theory is in

* {#Rezk06} [[Charles Rezk]], section II of _The units of a ring spectrum and a logarithmic cohomology operation_, J. Amer. Math. Soc. 19 (2006), 969-1014 ([arXiv:math/0407022](http://arxiv.org/abs/math/0407022))

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 {#ABGHR08}

Remarks alluding to this are also on p. 20 of 

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_
  {#Lurie}

Theorem 3.2 there is proven using classical results which are collected in

* [[Peter May]], _What precisely are $E_\infty$-ring spaces and $E_\infty$-ring spectra?_, Geometry and Topology Monographs 16 (2009) 215&#8211;282 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Final1.pdf))

A survey of the situation in [[(∞,1)-category theory]] is also in section 3.1 of 

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_

A construction in terms of a [[model structure on spectra]] is in

* John Lind, _Diagram spaces, diagram spectra, and spectra of units_ ([arXiv:0908.1092](http://arxiv.org/abs/0908.1092))


A refinement of the construction of $\infty$-groups of units to [[augmented ∞-groups]] over the [[sphere spectrum]], such as to distinguish $gl_1$ of a [[periodic E-∞ ring]] from its connective cover, is in

* {#Sagave11} [[Steffen Sagave]], _Spectra of units for periodic ring spectra_ ([arXiv:1111.6731](http://arxiv.org/abs/1111.6731))
 
based on ([Schlichtkrull 04](#Schlichtkrull04)). See also

* {#Szymik11} [[Markus Szymik]], _Brauer spaces for commutative rings and structured ring spectra_ ([arXiv:1110.2956](http://arxiv.org/abs/1110.2956))

* {#BakerRichterSzymik12} [[Andrew Baker]], [[Birgit Richter]], [[Markus Szymik]], _Brauer groups for commutative $\mathbb{S}$-algebras_, J. Pure Appl. Algebra 216 (2012) 2361&#8211;2376 ([arXiv:1005.5370](http://arxiv.org/abs/1005.5370))


The $\infty$-group of units of [[Morava K-theory]] is discussed in 

* [[Hisham Sati]], [[Craig Westerland]], _Twisted Morava K-theory and E-theory_ ([arXiv:1109.3867](http://arxiv.org/abs/1109.3867))
 {#SatiWesterland11}

The [[cohomology]] with coefficients in $gl_1(E)$ and the corresponding [[logarithmic cohomology operations]] are discussed in

* {#Rezk06} [[Charles Rezk]], _The units of a ring spectrum and a logarithmic cohomology operation_, J. Amer. Math. Soc. 19 (2006), 969-1014 ([arXiv:math/0407022](http://arxiv.org/abs/math/0407022))

The group of units of [[tmf]] is analyzed from section 12 on in 

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

[[!redirects ∞-group of units]]

[[!redirects ∞-groups of units]]
[[!redirects infinity-groups of units]]

[[!redirects ∞-group ∞-ring]]
[[!redirects ∞-group ∞-rings]]

[[!redirects ∞-group E-∞-ring]]
[[!redirects ∞-group E-∞-rings]]

[[!redirects ∞-group E-∞ ring]]
[[!redirects ∞-group E-∞ rings]]

[[!redirects ∞-group E-infinity-ring]]
[[!redirects ∞-group E-infinity-rings]]

[[!redirects ∞-group E-infinity ring]]
[[!redirects ∞-group E-infinity rings]]


[[!redirects ∞-group ring]]
[[!redirects ∞-group rings]]

[[!redirects group ∞-ring]]
[[!redirects group ∞-rings]]

[[!redirects infinity-group infinity-ring]]
[[!redirects infinity-group infinity-rings]]

[[!redirects infinity-group ring]]
[[!redirects infinity-group rings]]

[[!redirects group infinity-ring]]
[[!redirects group infinity-rings]]