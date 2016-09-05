+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
A monster for a first-order theory $T$ is a sort of "equivariant Grothendieck universe" for the definable sets of that theory. The notion generalizes that of Weil's universal domain (which are just monster models of the theory [[theory of algebraically closed fields|ACF]] of algebraically closed fields.)

The idea, to quote Hrushovski (see more below) is to bring out the geometry of a situation with minimal intervention of particular algebraic structures, for example allowing us to avoid many base changes.

## Definition
The most important aspects of monster models are _saturation_ and _homogeneity_: all [[type (in model theory)|types]] over parameter sets of a certain size are realized, and all elementary embeddings of subsets can be extended to automorphisms. Most commonly the monster is assumed to be the size of an inaccessible cardinal $\kappa$, with $\kappa$-saturation (all types over parameter sets of size less than $\kappa$ are realized) and $\kappa$-homogeneity (all elementary embeddings of subsets of size less than $\kappa$ are extended by automorphisms).

## Facts about monsters

* Compactness and saturation yield, in the monster, that:

1. families of definable sets (definable over a small parameter set) with nonempty finite intersections have nonempty total intersection,

2. small unions of definable sets (definable over a small parameter set) are finitely supported, and

3. small intersections of definable sets (definable over a small parameter set) are finitely supported.

* All small ($ &lt; \kappa = \mathbb{M} \models T$) models of $T$ elementarily embed into $\mathbb{M}$.

* Two tuples $a,b$ will have the same type $\operatorname{tp}(a/A) = \operatorname{tp}(b/A)$ over a small parameter set $A$ if and only if they are $\operatorname{Aut}(\mathbb{M}/A)$-conjugate.

* Sometimes it is useful to talk about large types, particularly those over all of $\mathbb{M}$ as a parameter set. These are called _global [[type (in model theory)|types]]_, and are usually not realized.

## Examples
Monster models in general tend to be hard to explicitly describe, except when theories are "well-behaved", e.g. stable (when type spatn the number of isomorphism classes of models in a certain cardinality is $1$). For example, both are true for $\mathsf{ACF}$.

By a back-and-forth argument (e.g. the one used by Cantor to prove the uniqueness of the countable dense linear order without endpoints), one can show that any two monster models are well-defined up to isomorphism, up to cardinality.

## Comparison with scheme approach to algebraic geometry
From Appendix B of Ehud Hrushovski's _Computing the Galois group of a linear differential equation_:

_"The distinctions between [treating formulas as primary objects, or taking seriously abstract algebraic structures to the point of ignoring formulas, or treating formulas as representable functors, or just working in a universal domain] relate to the revolution of schemes only at its surface. Grothendieck's real contribution, in this respect, was no the change of language, but the incorporation of infinitesimals, and of homological algebra, as intrinsic parts of the geometry. These go beyond Weil's original universal domain, not because it is a universal domain, but because it is a universal domain for the wrong class of structures (rings, and without nilpotents)...

The most serious objection to universal domains is that they apply only when the structures in question admit amalgamation; and preferably a certain finiteness property allowing a model companion. Do these properties hold for an appropriate presentation of schemes with infinitesimals, or for varieties with coherent sheaves over them? There has been little work on these questions; perhaps because of the view, widely held and published by model-theorists, that [[ACF]] remains the first-order theory underlying algebraic geometry; that Grothendieck somehow changed the logical way of looking at it, rather than the theory itself. The answer to the second question appears to be positive. For the firs, Cherlin showed that commutative rings with infinitesimals do not have a model companion in the language of rings, essentially because the order of infinitesimals must be taken seriously. But once this is done, a positive answer may exist (Truncated valuation rings have a good model theory, and give a partial response.)"_

## Related concepts
* [[type (in model theory)]]
## References
- John Baldwin, _The Monster Model_ [(pdf)](http://homepages.math.uic.edu/~jbaldwin/pub/monster.pdf)

- John Baldwin, _How big should the monster model be? [(pdf)](http://homepages.math.uic.edu/~jbaldwin/pub/monster4.pdf)