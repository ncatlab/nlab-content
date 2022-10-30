
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

## Related concepts

* [[(∞,1)-vector bundle]]

## References


* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 {#ABGHR08}

* [[Peter May]], _What precisely are $E_\infty$-ring spaces and $E_\infty$-ring spectra?_, Geometry and Topology Monographs 16 (2009) 215&#8211;282 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Final1.pdf))


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


