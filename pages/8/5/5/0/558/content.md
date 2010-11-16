#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The _homotopy hypothesis_ states that [[n-groupoid]]s are combinatorial models for [[homotopy n-type]]s. As a slogan:

* [[∞-groupoid]]s are combinatorial models for [[topological space]]s.

At least when [[∞-groupoid]]s are modeled by [[Kan complex]]es the homotopy hypothesis is a _theorem_ .

+-- {: .num_theorem}
###### Theorem

There is a [[Quillen equivalence]]

$$
  \Pi(-) : Top \leftrightarrow SSet : |-|
$$

between the [[model structure on topological spaces]] and the [[model structure on simplicial sets]]. This is given by forming [[geometric realization]] $|-|$ and the [[fundamental ∞-groupoid]] $\Pi(-)$, respectively.

This induces an equivalence of the [[presentable (infinity,1)-category|presented]] [[(infinity,1)-categories|(∞,1)-category]] [[Top]] and [[∞-Grpd]] and hence in particular between [[CW-complex]]es (the fibrant-cofibrant objects in [[Top]]) and [[Kan complex]]es (the fibrant-cofibrant objects in [[SSet]].)

=--

To some extent the homotopy hypothesis is not a hypothesis but a _requirement_ on the definition of [[infinity-groupoid]]: for every "good" definition of $\infty$-groupoid there should be an "obvious" pair of functors relating the collection of all $\infty$-groupoids to the collection of (well behaved) topological spaces which form an [[equivalence]] in a "suitable" sense.  The functor from spaces to $\infty$-groupoids is generally called the [[fundamental infinity-groupoid]], and its inverse equivalence may be thought of as a form of [[geometric realization]].

The homotopy hypothesis is known to be true for some definitions of "$\infty$-groupoid".  For example, there is a good case to be made that a [[Kan complex]] is a notion of $\infty$-groupoid, and it's been known for a long time in [[homotopy theory]] that Kan complexes model spaces, homotopically speaking.  It is also known that $n$-groupoids model $n$-types for $n\le 3$, for the existing well-understood models of $n$-categories for low values of $n$ (namely [[category|categories]], [[bicategory|bicategories]], and [[Gray-category|Gray-categories]]).  However, for other notions of [[higher category theory|higher category]] and higher values of $n$, it remains a hypothesis/requirement.

The requirement to satisfy the homotopy hypothesis is one thing that forces us out of the domain of [[strict n-category|strict n-categories]] for $n\gt 2$.  It is known that not all homotopy 3-types can be modeled by strict 3-groupoids, but that [[Gray-category|Gray-categories]] ([[semi-strict infinity-category|semi-strict 3-categories]]) suffice; the obstruction is the [[Whitehead product]] which arises from a nontrivial [[interchanger]].

In analogy to the homotopy hypothesis, there are also attempts to relate general [[infinity-category|infinity-categories]] which need not be groupoidal to [[directed space]]s, in which a morphism which is not invertible would model a path in the space that can only be traversed in one direction.


## The meaning of "models" 

One has to be careful, in stating the homotopy hypothesis, to specify what one means by "models."  The usual, unstated, implication is that the notion of _equivalence_ of $n$-groupoids used to model $n$-types is the appropriate *$n$-category-theoretic* notion of [[equivalence of categories|equivalence]].  It is in this way that, for instance, it is known that 1-groupoids model 1-types; to be precise, the 2-category of groupoids, functors, and natural transformations is equivalent to the 2-category of 1-types, continuous maps, and homotopy classes of homotopies.

The reason this is important to specify is that there are other notions of equivalence on categorical structures which model homotopy types in other ways.  For example, if we declare a functor between categories to be a weak equivalence iff its [[nerve]] is a weak equivalence of [[simplicial set]]s, then _all_ homotopy types can be modeled by 1-categories in this way; see the [[Thomason model structure]] for 1-categories.


## The $n$-fold case 

It is also known since the work of Loday and Porter that _strict_ $n$-[[n-fold category|fold categories]] also model all homotopy $n$-types.  

Loday proved in

* J.-L. Loday, _Spaces with finitely many non-trivial homotopy groups_, J. Pure Appl. Algebra
24 (1982), 179-202.

that the homotopy category of [[cat-n-group]]s is equivalent to that of pointed connected homotopy $n$-types.

Regis Pellissier produces in his 2003 thesis a Quillen equivalence between Segal groupoids and Topological Spaces:

* [arXiv](http://arxiv.org/abs/math/0308246)

For reviews see for instance

* Ronald Brown, _Computing Homotopy Types Using Crossed $N$-Cubes of Groups_ ([arXiv](http://arxiv.org/abs/math/0109091))

* Simona Paoli, _Internal categorical structures in homotopical algebra_, to appear in _Towards Higher Categories_, eds. J. Baez and P. May.  ([pdf](http://www.maths.mq.edu.au/~simonap/paoli_IMA.pdf))

Strict $n$-fold categories can in fact be considered as modeling certain diagrams of spaces, or structured spaces, which is useful for computing with "[[higher van Kampen theorems]]."  In general, we have some functors
$$\Xi:({diagrams of spaces })\leftrightarrow ({higher groupoids}):B $$
such that:
1. $\Xi$ is homotopically defined and preserves certain colimits;
1. $\Xi \circ B$ is equivalent to Id;
1. There is a natural transformation $Id \rightarrow B \circ \Xi$ preserving some homotopical information. 

The purpose of 1. is to be able to calculate some homotopical information. The purpose of 2. is to show that the diagrams used reflect the algebraic structure of the higher groupoids. Detailed references can be found at the [Higher dimensional group theory](http://www.bangor.ac.uk/r.brown/hdaweb2.htm) web site. 

Trying to be more explicit about some colimits of certain higher groupoids has yielded some interesting algebraic constructions, for which some examples required computational group theory!

## References

* [[John Baez]], _The Homotopy Hypothesis_ ([web](http://math.ucr.edu/home/baez/homotopy/), [pdf](http://math.ucr.edu/home/baez/homotopy/homotopy.pdf))

* [[Ronnie Brown]], _Higher dimensional group theory_ ([web](http://www.bangor.ac.uk/r.brown/hdaweb2.htm). See there for further references. )



