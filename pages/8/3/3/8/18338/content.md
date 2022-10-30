Term which is often used, mostly informally, in mathematical discussions. 

There does not exist a standard precise meaning.
Unnatural isomorphisms _per se_ are not studied in category theory. 
They are sometimes considered either irrelevant, or seen as a reason to work with different definitions (see [comment to OP's question referring to triangulated categories](#MathOverflow2013)). 



Understanding and measuring underlying _reasons_ for failure  of naturality($\approx$commutativity) of correspondences can be instructive, however.  

Basic examples:

 *  The strong reason of functors not being naturally isomorphim for the sole reason of one being [[contravariant functor|contravariant]] _can_ be presented in expositions as the raison d'&#234;tre for the ${}^\mathrm{op}$ in the very definiton of [[presheaves]]: without the op, the natural isomorphism provided by the [[Yoneda lemma]] would be an unnatural isomorphism. (But unnatural for the definitional reason of wrong variances; the ${}^\mathrm{op}$ avoids this.)
* Whittling down the reservoir of morphisms available for deriving contradictions (from the hypothesis of naturality) until _no_ contradictions  can be derived anymore can sometimes lead to unexpected insights. One can in this way view the wide subcategory of finite-dimensional $K$-vector spaces with _morphisms only_ those $K$-linear maps which leave a bilinear form (fixed from the outset, kept behind the scenes, and not being _part_ of the category) invariant as the largest wide subcategory of $\mathcal{C}$ which makes the notoriously unnatural single-dual-endofunctor natural.  
* A systematic keeping track of higher morphisms between _unnequal_ compositions arising from _unnatural isomorphisms_ seems to call for methods of [[higher category theory]].

At a deeper level, both natural and unnatural isomorphisms are but two facets of the same logical principle.





The most important distinction is that _unnatural isomorphism_ is used both to refer to 

 * size: a perceived non-unicity of choices needed to build some isomorphism (one may call this _noncanonical_ isomorphism)
 * structure: a perceived non-commutativity of the isomorphism built, relative to a category (one may call this _unnatural isomorphism_)

This article is _not_ about the former informal meaning, which arguably is about size only (see [MO discussion](#MathOverflow2010) for a discussion of the adjective _canonical_ instead). Rather, it  focuses on the latter meaning only, and, more precisely, on the concept of unnaturally [[isomorphic functor]]s.  Understanding unnaturally isomorphic functors can help to better appreciate the important concept of [[natural isomorphism]].




# Contents #
* table of contents
{:toc}

## Ideas and intuitive introduction

The term _unnatural isomorphism_ is born of a wish to speak about things which appear very similar, but the similarity is less compelling than in other situations. Then, [[category theory]] is a useful tool to understnad the underlying reasons. Understanding situations of unnatural isomorphism can help to better appreciate [[natural isomorphism]]s, in particular, to appreciate that---contrary to what the adjective _natural_ may suggest---many isomorphisms that occur in nature are not natural in the technical sense, while many others are, and the natural ones are particularly efficient to work with.


## Terminology

The term _unnatural_ is not to be taken in a judgemental sense, nor as suggesting this kind of isomorphism would occur _rarely_.  The term is rather modelled on a standard term, [[natural isomorphism]], which in turn is used for traditional reasons, cf. [EilenbergMac Lane45](#EilenbergMacLane45). The term _natural_ is an example of the common phenomenon that concepts branded _natural_, _normal_ or _regular_ tend to be rather non-generic or non-random.

In fact, Eilenberg and Mac Lane in [EilenbergMac Lane45](#EilenbergMacLane45) comment (cf. p. 233, first paragraph in loc. cit) on the term, associating it with an intuition of _simultaneity_, rather than genericity. This intuition is in tune with conceiving of naturality as generalized_commutatitivity_.

In [comment to question](#MathOverflow2013), _pointwise isomorphic_ is being recommended as a synonym, which is a more descriptive, neutral and systematic term. In [Rezk2016, Section 17.2](#Rezk2016), the term _objectwise_ isomorphism is used to discuss the problem of whether pointwise isomorphic natural transformations between [[quasi-categories]] are natural isomorphisms.

Rezk stresses that 

> natural isomorphisms are natural transformations which are isomorphisms objectwise.

(For quasicategories, this is not a tautology.)

 
Another evocative term would be _statically isomorphic_: intuitively, two functors are unnaturally isomorphic they always (produce things which) look isomorphic---as long as you do not move in the source-category.


##### Canonical, functorial, invariant, natural

The (use of) the adjectives like _canonical_, _invariant_,  _functorial_, _natural _ is sometimes satirized although they are useful, when used with care. For example, an influential German textbook mocks one of the terms in a footnote, and (#MathOverflow2010) gives a citation which is another example of such mockery.

A more descriptive alternative for _natural_ can be  _equivariant_ (w.r.t. to _all_ relevant monoid actions). In mathematical practice, "relativized" formulations like _natural only w.r.t. the isomorphisms of the category_ are sometimes used.


A basic distinction is that 

* both terms _canonical_ and _functorial_ are properties defined for _a single class-function_, the former w.r.t. _number of choices_, the later w.r.t. compatibility with ambient _structure_,
* the term _natural_ is a property of a _pair_ of class-functions.

A basic instructive example of the usefulness of the terms _canonical_ and _functorial can be discussing [[limit]]s: let us recall that _functorial_ is a useful shorthand for: _is a functor, or, can be made a functor without changing the categories already fixed_. <sub>(If tampering with the categories is permitted, any assignment of objects can be made into a functor by making the source category discrete, needless to say.)</sub>
Now let $\mathsf{C}$ be a category, let $\mathsf{J}$ be a small category. Suppose that every functor $\mathsf{J}\rightarrow\mathsf{C}$ _has_ a limit in $\mathsf{C}$. 
Assuming some principle of choice if need be, there then exists an assignation 

$\mathrm{lim}_{\mathsf{J}}\colon\mathrm{Ob}( [\mathsf{J},\mathsf{C}] )\rightarrow\mathrm{Ob}(\mathsf{C})$

such that for each $F\in[\mathsf{J},\mathsf{C}]$ the object $\mathrm{lim}_{\mathsf{J}}(F)$ is a limit of $F$.

Now this assignation $\mathrm{lim}_{\mathsf{J}}$ is never uniquely determined except in degenerate situations, so it is _non-canonical_, but basic category theory teaches that this assignation is _functorial_:  $\mathrm{lim}_{\mathsf{J}}$ can be _extended_ to the class $\mathrm{Ob}(\mathsf{C})\cup\mathrm{Mor}(\mathsf{C})$ to become a functor $[\mathsf{J},\mathsf{C}] \rightarrow\mathsf{C}$. 

### Descriptions of the usage

##### A  non-example 

A kind of _non_-example is the use of the term _unnatural isomorphism_ in Section 1.1 of [Strickland](#Strickland1998); there, the term presumably refers to nothing else than there being as many isomorphisms between two finite fields of the same cardinality as there are field automorphisms of a finite field of that size, none of them meaningfully distinguished.
This is the use of _unnatural_ as a synonym for _non-canonical_, which this article is _not_ about. 


##### An indirect example 

There is a widespread usage "naturally isomorphic functors", somewhat pleonastic since [[isomorphic functors]] are usually assumed to be naturally isomorphic by default. 

##### Examples in mathematical discussions.

The term is discussed, and a definition proposed, in [MathOverflow2013](#MathOverflow2013).

The issue of _naturality versus canonicity_ comes up in[this MO question](#MathOverflow201308). The isomorphism in the [[Yoneda lemma]] is always natural, but not in general canonical (in the sense that there are categories whose identity functor has non-trivial automorphisms).


##### An example in a textbook

The term _unnatural isomorphism_ is often used in [[homological algebra]], in particular in discussions of splittings. An example is [Theorem 4.3](#HiltonStammbach71), which explictly uses the term to decribe an isomorphism between Hom- and Ext-functors.

##### An example in a recent thesis 


Species are functors for which unnatural isomorphisms are often discussed. Examples are [this MO comment](#GesselTrimble2014) and also [Definition 3.3.4](#Yorgey2014), which defines an equivalence relation on the class of all species by explicitly using the term, defining an "equipotence between species [...] as an "unnatural" isomorphism between [the two species in question]", however, in _another_ sense, which will not be spelled out here, than discussed in  [MathOverflow2013](#MathOverflow2013).


### A source of confusions

Confusions in teaching and discussions appear to arise from the  adjective _isomorphic_ being defined 

* between objects of one and the same category,

* between two categories, 

* between two functors.

At the face of it, discussions of unnatural isomorphisms are often about two _objects_ of a given category, such as in discussions of some vector space $V$ being unnaturally isomorphic to its dual $V^\ast$. (Cf example ($K$.dual) below.

This makes it seems as if there were a concept of unnaturally isomorphic _objects_. However, in a sense unnaturally _objects_ is a meaningless concept ( and so are _naturally_ isomorphic objects, for that matter): 

* on an elementary logical level, the language of 1-categories has but _one_ [[sort]] of _variables_ for (i.e. interpreted as) morphisms.

While, in a sense, there are several "derived" sorts (the most elementary being [[epi]], [[mono]] and [[iso]]) of morphisms, defined by first-order formulas in the language of 1-category theory, a definition of _unnatural_ isomorphism in a category, formally speaking, does simply _not_ exist. 




### Notational remarks

*  <sub>Text in small fontcan be skipped with little loss, providing an quicker route through the article.</sub> 
*   Here, $\mathrm{Ob}$ denotes the object function and $\mathrm{Mor}$ denotes the morphisms function (usual alternative for $\mathrm{Mor}$ is $\mathrm{Ar}$)
*     Here, we write endomorphism monoids of objects via the usual hom-set notation, that is, write $\mathcal{D}(O,O)$ instead of $\mathrm{End}_{\mathcal{D}}(O)$, since the former is more systematic and not longer than the latter.
* Here, objects of $\mathcal{C}$ are denoted by unprimed letters $O$, while objects of $\mathcal{D}$ are denoted by the primed letter $O'$. If we need several objects of the same category, lower _indices_ are used<sub> (and in the source code of this article, indices are used _after_ the prime ')</sub>. Generic objects in morphism definitions are then sometimes denoted by the unindexed letter $O$, a typical example of this convention being the definition of the usual  natural transformation $\mathsf{C}(O_0,-)\overset{(-)\circ f}{\longrightarrow}\mathsf{C}(O_1,-)$ induced by a morphism $O_1\overset{f}{\rightarrow}O_0$, which is given by $((-)\circ f)(O_0\overset{h}{\rightarrow}O)=O_1\overset{h\circ f}{\rightarrow}O$.
*  Here, the functors compared are invariably denoted $F_0$ and $F_1$, not $F$ and $G$, like in e.g. [MathOverflow2013](#MathOverflow2013), for one main reason: there is a long tradition of denoting functors in _opposite_ directions by $F$ and $G$, especially in discussions of adjunctions, but this is not what this article is about. 



In [MathOverflow2013](#MathOverflow2013), the following definition of _unnatural isomorphism_ was proposed. 

##### MO definition. 

Given categories $\mathcal{C}$ and $\mathcal{D}$, functors $\mathcal{C}\overset{F_0}{\rightarrow}\mathcal{D}$ and $\mathcal{C}\overset{F_1}{\rightarrow}\mathcal{D}$ being _unnaturally isomorphic_ means that there exists at least one assignation $\Phi\colon\mathrm{Ob}(\mathcal{C})\rightarrow\mathrm{Mor}(\mathcal{D})$
such that 

* (pointwise.iso) for each object $O$ of $\mathcal{C}$ the morphism $F_0(O)\overset{\Phi(O)}{\longrightarrow} F_1(O)$ is an [[iso]] of $\mathcal{D}$,

* (non.extendible) there does not exist any [[natural isomorphism]] $F_0\Rightarrow F_1$.

An _unnatural isomorphism on $\mathcal{C}$ into $\mathcal{D}$_ is any _pair $(F_0,F_1)$ of unnaturally isomorphic functors_ in the above sense.



## Examples

Many of these examples are based on [MathOverflow2013](#MathOverflow2013), please see there if interested in where some of the example come from. For readability, no separate attributions to references, let alone individual persons are made. 

The purpose of this article is not to duplicate, or present a digest of, the discussion in  [MathOverflow2013](#MathOverflow2013), rather to organize  and develop some of these example by 

* organizing them according to _reasons_ for nonnaturality,
*  within each reason, distinguish unnatural isomorphisms involving
* * one identity endofunctor,
* *  two non-identity endofunctors,
* *  two non-identity non-endofunctors.



+-- {: .query}
(here we could include examples, preferable with a uniform notation and keeping those examples using endofunctors separate from those involving categories which are "far" from each other 
=--



### Connections to equivariant semigroup actions

+-- {: .query}
(here we could systematically discuss the concept of equivariance)
=--

### Connections to [[higher category theory]]

+-- {: .query}
(here we coud include a look, from the point of view of higher category theory,  at unnatural isomorphisms, especially in situations where there is some reasonable notion of morphisms between _unequal_ compositions in the (non-)naturality-squares)
=--


## References

* {#EilenbergMacLane45} [[Samuel Eilenberg|S. Eilenberg]], [[Saunders Mac Lane|S. Mac Lane]], _General Theory of Natural Equivalences_,  Transactions of the American Mathematical Society
Vol. 58, No. 2 (Sep., 1945), pp. 231-294 ([JSTOR](http://www.jstor.org/stable/1990284))

* {#HiltonStammbach71} [[Peter Hilton|P. Hilton]],  U. Stammbach, _A course in homological algebra_, Springer-Verlag, New York, 1971, Graduate Texts in Mathematics, Vol. 4.

* {#MathOverflow2010} MathOverflow, _[What is the definition of "canonical"?](https://mathoverflow.net/questions/19644/what-is-the-definition-of-canonical)_ 

* {#MathOverflow2013} MathOverflow, _[Example of unnatural isomorphism](https://mathoverflow.net/questions/139388/example-of-an-unnatural-isomorphism)_ 


* {#MathOverflow201308} MathOverflow, _[Unicity of Yoneda isomophism](https://mathoverflow.net/q/140303)_ 

* {#GesselTrimble2014} MathOverflow, _[What are some examples of interesting uses of the theory of combinatorial species?](https://mathoverflow.net/q/59259)_

* {#Rezk16} [[Charles Rezk]], _Stuff about quasicategories_, Lecture Notes for course at University of Illinois at Urbana-Champaign, 2016, version May 2017,([pdf](http://math.uiuc.edu/~rezk/595-fal16/quasicats.pdf))

* {#Strickland1998} [[Neil Strickland|N. P. Strickland]], Morava E-Theory, Topology, Vol. 37, No. 5 (1998), 757--779

* {#Yorgey2014} [[B. A. Yorgey|B. A. Yorgey]], Combinatorial Species and Labelled Structures,  Dissertation, University of Pennsylvania, 2014