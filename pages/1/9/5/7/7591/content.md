
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

+-- {: .num_defn}
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

## Properties
 {#Properties}

### Adjointness to $\infty$-group $\infty$-ring

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

which is indeed [[right adjoint]] to forming the ordinary [[group of units]] of a ring.

We might call $\mathbb{S}[A]$ the *$\infty$-group $\infty$-ring of $A$ over the [[sphere spectrum]].

=--

## Examples

### Snaith's theorem
 {#SnatihTheorem}

[[Snaith's theorem]] asserts that 

1. the [[K-theory spectrum]] for [[complex K-theory]] is the [[∞-group ∞-ring]] of the [[circle 2-group]] localized at the [[Bott element]] $\beta$:

   $$
     KU \simeq (\mathbb{S}[B U(1)])[\beta^{-1}]
     \,;
   $$

1. the [[periodic complex cobordism spectrum]] is the [[∞-group ∞-ring]] of the [[classifying space]] for stable [[complex vector bundles]] (the classifying space for [[topological K-theory]]) localized at the [[Bott element]] $\beta$:

   $$
     MU \simeq (\mathbb{S}[B U])[\beta^{-1}]
     \,.
   $$

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

A general abstract discussion in [[stable (∞,1)-category]] theory is in

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 {#ABGHR08}

Theorem 3.2 there is proven using classical results which are collected in

* [[Peter May]], _What precisely are $E_\infty$-ring spaces and $E_\infty$-ring spectra?_, Geometry and Topology Monographs 16 (2009) 215&#8211;282 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Final1.pdf))

A construction in terms of a [[model structure on spectra]] is in

* John Lind, _Diagram spaces, diagram spectra, and spectra of units_ ([arXiv:0908.1092](http://arxiv.org/abs/0908.1092))

The $\infty$-group of units of [[Morava K-theory]] is discussed in 

* [[Hisham Sati]], [[Craig Westerland]], _Twisted Morava K-theory and E-theory_ ([arXiv:1109.3867](http://arxiv.org/abs/1109.3867))
 {#SatiWesterland11}

See also

* Steffen Sagave, _Spectra of units for periodic ring spectra_ ([arXiv:1111.6731](http://arxiv.org/abs/1111.6731))


[[!redirects ∞-group of units]]

[[!redirects ∞-groups of units]]
[[!redirects infinity-groups of units]]

[[!redirects ∞-group ∞-ring]]
[[!redirects ∞-group ∞-rings]]

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


