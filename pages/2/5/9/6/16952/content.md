
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[equivariant stable homotopy theory]] a _[[genuine G-spectrum]]_  has [[homotopy groups]] [[grading|graded]] not just by the [[integers]], but by the (additive group underlying) the [[representation ring]] of $G$. This is often called _$RO(G)$-grading_. 

## Motivation

### Suspension by representation spheres

Since a [[cohomology theory]] is, in particular, a functor

$$
  E^\bullet \colon BasedSpaces^{op} \longrightarrow GradedAbelianGroups
$$

satisfying some axioms, then naively a $G$-equivariant cohomology theory could be defined to be a functor

$$
  E_G^\bullet\colon Based G Spaces^{op} \longrightarrow GradedAbelianGroups
  \,.
$$

This implies in particular the [[suspension isomorphism]]: for  $n\in \mathbb{N}$ there is, for each $G$-space $X$, an identification 

$$
   E_G^\bullet(X) \simeq  E_G^{\bullet + n}(S^n \wedge X)
  \,,
$$

where in the smash product $S^n \wedge X$ the group $G$ is to be taken to act trivially on the [[sphere]] $S^n$. From this perspective it is desirable to have an analogous relation also for smashing with spheres on which the group $G$ acts nontrivially. Since we may think of $S^n$ as being the [[representation sphere]] of the trivial action of $G$ on $\mathbb{R}^n$, this leads one to demand that $E^\bullet$ is graded not just by the integers, but by any [[linear representation]] $V$, so that one has _equivariant [[suspension isomorphisms]]_

$$
  E_G^\bullet(X) \simeq E_G^{\bullet + V}(S^V \wedge X)
  \,,
$$

where now $S^V$ denotes the [[representation sphere]] of $V$. This more general grading is, for historical reasons, called "[[RO(G)-grading]]", and an equivariant cohomology theory equipped with this extra structure is called _genuine_ (as opposed to the "naive" case with grading just over the integers).

### Representation by $G$-spectra

Since by the [[Brown representability theorem]], in the absence of a group action a cohomology theory is [[representable functor|represented]] by a [[spectrum]], it is natural to construct a category in which genuine $G$-equivariant cohomology theories also become representables. This is the [[equivariant stable homotopy theory]] of [[genuine G-spectra]].


### Induced transfer and Mackey functors

(...)

## Definition

For $G$ a [[finite group]], $X$ a $G$-[[equivariant spectrum]] modeled as an [[orthogonal spectrum]] equipped with a $G$-[[action]], and for $V$ a linear $G$-[[linear representation|representation]] on a [[real vector space]] of [[dimension]] $n$, the value of $X$ in $RO(G)$-degree $V$ is

$$
  X(V)
  \coloneqq
  \mathbf{L}(\mathbb{R}^n, V)_+ \wedge_{O(n)} X_n
  \,,
$$

where

* $\mathbf{L}(\mathbb{R}^n, V)$ is the linear [[isometries]] $\mathbb{R}^n \to V$ ([[orthogonal bases]]);

(e.g. [Schwede 15 (2.2)](#Schwede15))

The _$RO(G)$-graded [[equivariant homotopy group]]_ of $X$ is (in the notation used there)

$$
  \pi_V^G(X)  \coloneqq
  \underset{\longrightarrow_{\mathrlap{n}}}{\lim}
  [S^{V + n \rho_G}, X(n \rho_G)]_G
  \,.
$$

(e.g. [Schwede 15, p. 40](#Schwede15))

## Properties

### Relation to intrinsic twisting

>  In equivariant cohomology theory, the use of $RO(G)$ is a great convenience, but it is not the thing most intrinsic to the mathematics.  Ignore the multiplication on $RO(G)$,  which is irrelevant to its use for grading theories, and think of it just as an abelian group.  Send a representation $V$ to the isomorphism class of the suspension $G$-spectrum of the one-point compactification $S^V$.  This induces a homomorphism from $RO(G)$ into the Picard group $Pic(Ho G\mathcal{S})$ of the stable homotopy category of  $G$-spectra, namely the abelian group of equivalence classes of 
$G$-spectra that are invertible under the smash product.  That homomorphism  is neither a monomorphism nor an epimorphism.  See ([Fausk-Lewis-May 01](#FauskLewisMay01)) for a discussion of that Picard group.  Logically, equivariant cohomology theories really should be graded on $Pic(Ho G\mathcal{S})$, but that group is much less  convenient than $RO(G)$.  ([P. May, comment on MO, Jul 2014](http://mathoverflow.net/a/177154/381))

## Related concepts

* [[G-universe]]

## References

A standard reference is

* {#May96} [[Peter May]], chapters IX.5, X and XIII of _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))


* {#Schwede15} [[Stefan Schwede]], section 4 (from page 40 on) in _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

* {#FauskLewisMay01} [[Halvard Fausk]], [[L. Gaunce Lewis]], [[Peter May]],  _The Picard group of equivariant stable  homotopy theory_, Advances in Mathematics Volume 163, Issue 1, 15 October 2001, Pages 17&#8211;33  ([pdf](http://www.math.uchicago.edu/~may/PAPERS/FLMJan01.pdf))

* [[Justin Noel]], _Equivariant cohomology of representation spheres and $Pic(S_G)$-graded homotopy groups_, 2013 ([pdf](http://www.nullplug.org/talks/equivariant.pdf))

[[!redirects RO(G)-gradings]]

[[!redirects RO(G)-degree]]
[[!redirects RO(G)-degrees]]