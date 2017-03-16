
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

## Definition (impredicative case)

There are at least two ambiguities in the above sketch of a definition based on type theory: what exactly do we assume of the universes, and what general class of HITs do we ask for?  One reasonable answer to the universe question is that every object should be contained in a universe closed under all the relevant operations, and one reasonable answer to the HITs question is just the non-recursive ones.  This leads to the following definition.

+--{: .un_defn}
###### Definition
An **elementary $(\infty,1)$-topos** is an $(\infty,1)$-category $E$ such that

* $E$ has finite [[(∞,1)-limit|limits and colimits]]
* $E$ is [[locally cartesian closed (∞,1)-category|locally cartesian closed]]
* There exists a [[subobject classifier]] (an [[object classifier]] that classifies the collection of all [[monomorphisms in an (∞,1)-category]])
* For any morphism $p:Y\to X$ in $E$, there exists an [[object classifier]] in $E$ classifying a class of morphisms that (1) includes $p$ and (2) is closed under fiberwise finite limits and colimits, composition (i.e. dependent sums), and dependent products.
=--

Note that this definition is "impredicative" just like an [[elementary topos]], in that it has a classifier for *all* subobjects.  We can't categorify this to a classifier for all objects due to size paradoxes; the existence of "enough" object classifiers closed under all the basic operations is the "next best thing".  In an elementary 1-topos we can construct finite colimits and dependent exponentials from non-dependent exponentials and the subobject classifier (or equivalently from [[power objects]]), but in the $\infty$-case this seems unlikely to be true since subobjects tell us less about objects that are not 0-truncated.

## Properties

It is reasonable to hope for a coherence theorem showing that any elementary $(\infty,1)$-topos in the above sense admits a model of homotopy type theory with non-recursive [[higher inductive type|HITs]] (corresponding to the the finite colimits), univalent [[type of types|universes]] (perhaps only weakly Tarski ones), and [[propositional resizing]].  See, for instance, [[homotopytypetheory:model of type theory in an (infinity,1)-topos]] and [relation between type theory and category theory -- Univalent homotopy type theory and infinity-toposes](relation+between+type+theory+and+category+theory#HomotopyWithUnivalence).  Furthermore, although not present explicitly in the definition, the following additional structure comes for free:

1. Universe cumulativity: for any object classifier $p:V\to U$, there is an object classifier $p':V'\to U'$ such that (1) $p$ is a pullback of $p'$, and also (2) $U\to 1$ is a pullback of $p'$.  To see this, apply the assumption about existence of object classifiers to the coproduct map $V+U \to U+1$.

1. A [[natural numbers object]].  Intuitively, it seems as if $\Omega(S^1)$ (which can be constructed using finite limits and colimits) ought to be the [[integers]] and we should be able to construct the natural numbers from it; but it is unclear to the authors of this page how to do that.  Instead, we can (using the impredicative subobject classifier) define the smallest subobject of an object classifier $p:V\to U$ that contains the initial object and is closed under taking coproducts with the terminal object.  This is almost right, but it is not 0-truncated.  We could 0-truncate it, but to get a universal property relative to all objects rather than only 0-truncated ones, we can instead impose structure making the objects rigid, such as a partial order or a graph.  This argument is formalized in type theory [here](#ConstructingNat); to be precise either it would have to be translated manually into category-theoretic language, or the above conjecture about interpreting type theory in an elementary $(\infty,1)$-topos would have to be proven.

1. The [[(n-connected, n-truncated) factorization system]].  The case $n=-1$ can be constructed impredicatively using the subobject classifier: internally, $\Vert A \Vert$ is the smallest [[truth value]] implied by $A$.  Then we can induct on *external* natural numbers, defining $\Vert A \Vert_{n+1}$ to be the $(-1)$-image of the composite $A \to U^A \to (U')^A$, where the second map is the $n$-truncation.  Note that in general it "goes up a universe level", so that the $n$-truncation "goes up $n+2$ universe levels".  However, unlike type theory, an elementary $(\infty,1)$-topos has no globally chosen tower of universes, so this doesn't literally make sense to say.  What we can say is that with this construction, it is not clear whether we can find object classifiers that are *closed* under the $n$-truncation.

   However, [(Rijke17)](#Rijke17) shows (again in type theory) that using finite colimits and the natural numbers, the $(-1)$-truncation can be constructed without raising the universe level.  Assuming (as always) that this can be translated into $(\infty,1)$-category theory, it implies that we *can* find object classifiers closed under the $(-1)$-truncation, and hence (by induction) under the $n$-truncation for all $n$.  Moreover, with a natural numbers object this induction can be performed internally, obtaining in particular object classifiers closed under the $n$-truncation for all $n$ at once.

1. It seems likely that the construction of [[W-types]] in any elementary 1-topos can be repeated in the $(\infty,1)$-case.

There is some structure that the definition probably does not imply, namely a semantic counterpart of arbitrary *recursive* [[higher inductive types]], such as arbitrary [[localization]].  It is certain that these cannot always be constructed in an elementary 1-topos: for instance, HITs imply that all (even infinitary) [[algebraic theories]] have initial algebras, whereas this cannot be proven in [[ZF]] without the [[axiom of choice]] (under appropriate [[large cardinal]] hypotheses).  Thus, it seems very unlikely that they can be constructed in an elementary $(\infty,1)$-topos.  Moreover, it is even unclear exactly what $(\infty,1)$-categorical structure should correspond to arbitrary [[higher inductive types]], not least because we lack an accepted general definition of an "arbitrary HIT".

However, although this is an open question, it is arguably not a question about the definition of "elementary $(\infty,1)$-topos", or even "elementary $(\infty,1)$-topos", but some stronger notion, analogous to a stronger notion of 1-topos that lacks an accepted name.  Moreover, a great deal of [[homotopy type theory]] (including synthetic homotopy theory) can be done with only non-recursive HITs, truncations, and a natural numbers type, and even in the absence of a general coherence theorem any particular result of HoTT could probably be explicitly written down in $(\infty,1)$-categorical language.


## Definition (predicative case)

Since there is no consensus even on the definition of [[predicative topos|predicative 1-topos]], it seems less likely that there is a definitive answer for a predicative $(\infty,1)$-topos.  However, it should probably include *at least* the following axioms:

* $E$ has finite [[(∞,1)-limit|limits and colimits]]
* $E$ is [[locally cartesian closed (∞,1)-category|locally cartesian closed]]
* For any morphism $p:Y\to X$ in $E$, there exists an [[object classifier]] in $E$ classifying a class of morphisms that (1) includes $p$ and (2) is closed under fiberwise finite limits and colimits, composition (i.e. dependent sums), and dependent products.
* $E$ has a [[natural numbers object]], and perhaps also [[W-types]].

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

The construction of $n$-truncations without recursive HITs is in

* {#Rijke17} [[Egbert Rijke]], *The join construction*, [arxiv](https://arxiv.org/abs/1701.07538)

The construction of natural numbers from propositional resizing and univalence is in

* {#ConstructingNat} HoTT/Coq library, &lt;https://github.com/HoTT/HoTT/pull/858>
 

[[!redirects elementary (∞,1)-topos]]
[[!redirects elementary (infinity,1)-topos]]
[[!redirects elementary (∞,1)-toposes]]
[[!redirects elementary (infinity,1)-toposes]]
[[!redirects elementary infinity-topos]]
[[!redirects elementary infinity-toposes]]

[[!redirects predicative elementary (∞,1)-topos]]
[[!redirects predicative elementary (infinity,1)-topos]]
[[!redirects predicative elementary (∞,1)-toposes]]
[[!redirects predicative elementary (infinity,1)-toposes]]
[[!redirects predicative elementary infinity-topos]]
[[!redirects predicative elementary infinity-toposes]]
