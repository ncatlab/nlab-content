
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of an _elementary (∞,1)-topos_ is an analogue of the notion of _[[elementary topos]]_ in [[(∞,1)-category theory]].  This is in contrast to the notion of a _Grothendieck_ _[[(∞,1)-topos]] [[equivalence of (∞,1)-categories|equivalent]] to an [[(∞,1)-category of (∞,1)-sheaves]]_, the analogue of a [[sheaf topos]], which is more specific (see [[geometric homotopy type theory]]).

Note that every _Grothendieck_ [[(∞,1)-topos]] provides [[categorical semantics]] for [[homotopy type theory]] with [[univalence|univalent]] weakly-Tarskian [[types of types]] and also [[higher inductive types]] (HITs).  Elementary $(\infty,1)$-toposes ought to be roughly the larger class of *all* $(\infty,1)$-categories that provide [[categorical semantics]] for such homotopy type theory.  More precisely, we will define an elementary $(\infty,1)$-topos to have the $(\infty,1)$-categorical structure that ought to correspond to that type-theoretic structure; a coherence theorem making it *actually* model the corresponding type theory is still unknown.

In general, the problem with "elementary-izing" the notion of $(\infty,1)$-topos is that Grothendieck $(\infty,1)$-toposes have many properties that are not reflected in type theory due to the finitary nature of type theory; the question is to find appropriate "finitary shadows" of them.  For instance, one can construct initial algebras for endofunctors using a transfinite induction argument; thus in type theory we postulate the existence of inductive types.  Deciding what class of "infinitary constructions" that are available in Grothendieck $(\infty,1)$-toposes can be described finitarily by something that deserves the name "higher inductive type" is overall an open question, but we can obtain reasonable definitions by restricting the class of HITs we ask for.

## Definition

There are at least two ambiguities in the above sketch of a definition based on type theory: what exactly do we assume of the universes, and what general class of HITs do we ask for?  One reasonable answer to the universe question is that every object should be contained in a universe closed under all the relevant operations, and one reasonable answer to the HITs question is just the non-recursive ones.  This leads to the following definition.

+--{: .un_defn}
###### Definition
A **(predicative) elementary $(\infty,1)$-topos** is an $(\infty,1)$-category $E$ such that

* $E$ has finite [[(∞,1)-limit|limits and colimits]]
* $E$ is [[locally cartesian closed (∞,1)-category|locally cartesian closed]]
* For any morphism $p:Y\to X$ in $E$, there exists an [[object classifier]] in $E$ classifying a class of morphisms that (1) includes $p$ and (2) is closed under fiberwise finite limits and colimits, composition (i.e. dependent sums), and dependent products.

An elementary $(\infty,1)$-topos $E$...

* is **impredicative** if it has a classifier for *all* subobjects.
* has a **[[natural numbers object]] (NNO)** if the $(\infty,1)$-category of pointed objects in $E$ with an endomorphism (i.e. diagrams $1\to X \to X$) has an initial object.
* is an **$(\infty,1)$-W-topos** if every [[polynomial endofunctor]] of $E$ has an initial [[algebra for an endofunctor|algebra]].
=--

An impredicative elementary $(\infty,1)$-topos is thus an $(\infty,1)$-analogue of an [[elementary topos]]: the difference is that we also ask for sufficiently many object classifiers, not just subobject classifiers.  In an elementary 1-topos we can construct finite colimits and dependent exponentials from non-dependent exponentials and the subobject classifier (or equivalently from [[power objects]]), but in the $\infty$-case this seems unlikely to be true since subobjects tell us less about objects that are not 0-truncated.

Note that the existence of finite colimits and dependent exponentials is also asserted directly in the 1-categorical notion of [[predicative topos]].  There are different notions of predicative topos, some of which also ask for weak object classifiers (satisfying existence but not uniqueness of classifying maps), W-types, and/or a weak choice principle.  So we can say that a predicative elementary $(\infty,1)$-W-topos is a reasonable $(\infty,1)$-categorical generalization of a predicative 1-topos.  Again, in an (impredicative) elementary 1-topos we can construct all W-types once we have an NNO, but in the predicative or $\infty$-case this seems unlikely to be true.

It is reasonable to hope for a coherence theorem showing that any elementary $(\infty,1)$-topos in the above sense admits a model of homotopy type theory with non-recursive HITs (corresponding to the the finite colimits) and (perhaps only weakly Tarski) univalent universes, and that impredicativity, NNOs, and initial algebras for polynomials correspond to [[propositional resizing]], a [[natural numbers type]], and [[inductive types]] respectively.  See, for instance, [[homotopytypetheory:model of type theory in an (infinity,1)-topos]] and [relation between type theory and category theory -- Univalent homotopy type theory and infinity-toposes](relation+between+type+theory+and+category+theory#HomotopyWithUnivalence).  A great deal of [[homotopy type theory]] can be done with only non-recursive HITs plus a natural numbers type, and even in the absence of a general coherence theorem any particular result of HoTT could probably be explicitly written down in $(\infty,1)$-categorical language.  In particular, the [[(n-connected, n-truncated) factorization system]] should be constructible in any elementary $(\infty,1)$-topos with an NNO, by repeating in terms of constructions in [[category theory]] the argument of ([Rijke 17](#Rijke17)).

It is less clear what $(\infty,1)$-categorical structure should correspond to arbitrary [[higher inductive types]], not least because we lack an accepted general definition of an "arbitrary HIT".  However, note that not every elementary 1-topos in the usual sense, even one with an NNO, has arbitrary HITs.  For instance, with recursive HITs one can show that every algebraic theory has an initial algebra, whereas this is not true in every elementary 1-topos with NNO.  Thus, although this is an open question, it is arguably not a question about the definition of "elementary $(\infty,1)$-topos", or even "elementary $(\infty,1)$-W-topos", but some stronger notion, analogous to a stronger notion of 1-topos that lacks an accepted name.

## Related pages

* [[elementary topos]]
* [[predicative topos]]
* [[Grothendieck (∞,1)-topos]]
* [[homotopy type theory]]

## References

A vague version of the above proposed definition is on the very last slide of 

* {#Shulman12} [[Mike Shulman]], _Inductive and higher inductive types_ (2012) ([pdf](https://home.sandiego.edu/~shulman/hottminicourse2012/04induction.pdf))

See also

* [[Michael Shulman]], [[Peter Lumsdaine]], 2016, _Semantics and syntax of
higher inductive types_, ([slides](http://home.sandiego.edu/~shulman/papers/stthits.pdf))

* {#Joyal14} [[André Joyal]], _What is an elementary higher topos?_, talk at _[Reimagining The Foundations Of Algebraic Topology](https://www.msri.org/workshops/689)_ April 07, 2014 - April 11, 2014_ [web video](https://www.msri.org/workshops/689/schedules/18227) [PDF](https://www.msri.org/workshops/689/schedules/18227/documents/2046/assets/20468)

* [[Georg Hegel]], [book 2](Science+of+Logic#LehreVomWesen) of _[[Science of Logic]]_

A construction of $n$-truncations without recursive HITs is in

* {#Rijke17} [[Egbert Rijke]], *The join construction*, [arxiv](https://arxiv.org/abs/1701.07538)
 

[[!redirects elementary (∞,1)-topos]]

[[!redirects elementary (∞,1)-toposes]]
[[!redirects elementary (infinity,1)-toposes]]

[[!redirects elementary infinity-topos]]
[[!redirects elementary infinity-toposes]]
