# Axioms of materialization

* table of contents
{: toc}

## Idea

An **axiom of materialization** states that every [[set]] is [[isomorphic]] to a [[pure set]] of a certain form.  They can be formulated either in [[structural set theory]] or [[material set theory]], and in reasonably strong set theories they are often provable.

## Versions

* The **axiom of well-founded materialization** says that every set is isomorphic to a well-founded pure set, or equivalently (at least in a strong enough set theory) that every set can be embedded into a well-founded extensional graph.  In material set theory this is also known as **Coret's Axiom B** ([Coret 64](#Coret64)).

* The **axiom of ill-founded materialization** says that every set can be embedded in an [[extensional relation|strongly extensional]] graph.

Since well-founded extensional graphs are strongly extensional, the well-founded axiom implies the ill-founded one.

## Provability

* The axiom of well-founded materialization follows from the [[axiom of choice]]: every [[well-ordered set]] is a well-founded extensional graph, so if every set is well-orderable then the axiom follows.

* In material set theory, the axiom of well-founded materialization follows from the  [[axiom of foundation]], since then every set *is already* a well-founded pure set.  Similarly, the axiom of ill-founded materialization follows from the [[axiom of anti-foundation]].

* In the presence of [[excluded middle]] and the [[axiom of replacement]], every strongly extensional graph can be embedded into a well-founded extensional graph.  Specifically, a graph is a coalgebra for the powerset functor, hence has a cone over the [[transfinite construction of free algebras|terminal coalgebra sequence]] for that endofunctor (which exists using the axiom of replacement, even though it does not converge to a terminal coalgebra).  The kernels of the maps in this cone are the approximations to the bisimilarity of the graph, and hence converge to it at some ordinal $\alpha$ (namely the [[Hartogs number]] of the lattice of binary relations; this uses excluded middle).  By strong extensionality, the bisimilarity is the identity, so the $\alpha^{\mathrm{th}}$ map in the cone is an injection into a well-founded set.

  Thus, given excluded middle and replacement, the axiom of ill-founded materialization implies the well-founded one, hence the two are equivalent.  In particular, if the axiom of foundation in ZF is replaced by the axiom of anti-foundation, then the axiom of *well-founded* materialization is also provable.

  It is unclear whether the two axioms of materialization are distinct in weaker theories such as [[IZF]] or [[Zermelo set theory]].

## Consequences

Either axiom of materialization implies that the [[category of sets]] is [[equivalence of categories|equivalent]] to its subcategory of the relevant kind of pure sets.  Thus, for instance, [[Scott's trick]] can be used to prove isomorphism-invariant properties (see for instance [this MO question](https://math.stackexchange.com/questions/305859/scotts-trick-without-the-axiom-of-regularity)).

## References

* {#Coret64} J. Coret, *Formules stratifides et axiome de fondation*, Comptes Rendus hebdomadaires des seances de l'Academie des Sciences de Paris serie A, vol. 264 (1964)

* {#Shulman19} [[Mike Shulman]], *Comparing material and structural set theories*. Annals of Pure and Applied Logic 170(4), 2019, p465–504, [arxiv](https://arxiv.org/abs/1808.05204v2)

category: foundational axiom

[[!redirects axiom of well-founded materialization]]
[[!redirects axiom of ill-founded materialization]]
[[!redirects axioms of materialization]]
[[!redirects Coret's axiom B]]
[[!redirects Coret's Axiom B]]

