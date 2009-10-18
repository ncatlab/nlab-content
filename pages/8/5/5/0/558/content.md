# Idea #

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


# The meaning of "models" #

One has to be careful, in stating the homotopy hypothesis, to specify what one means by "models."  The usual, unstated, implication is that the notion of _equivalence_ of $n$-groupoids used to model $n$-types is the appropriate *$n$-category-theoretic* notion of [[equivalence of categories|equivalence]].  It is in this way that, for instance, it is known that 1-groupoids model 1-types; to be precise, the 2-category of groupoids, functors, and natural transformations is equivalent to the 2-category of 1-types, continuous maps, and homotopy classes of homotopies.

The reason this is important to specify is that there are other notions of equivalence on categorical structures which model homotopy types in other ways.  For example, if we declare a functor between categories to be a weak equivalence iff its [[nerve]] is a weak equivalence of [[simplicial set]]s, then _all_ homotopy types can be modeled by 1-categories in this way; see the [[Thomason model structure]] for 1-categories.


# The $n$-fold case #

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

#References#

* John Baez, _The Homotopy Hypothesis_ ([web](http://math.ucr.edu/home/baez/homotopy/), [pdf](http://math.ucr.edu/home/baez/homotopy/homotopy.pdf))

* Ronnie Brown, _Higher dimensional group theory_ ([web](http://www.bangor.ac.uk/r.brown/hdaweb2.htm). See there for further references. )

# Discussion #

## Why Seek Other Models for Homotopy Types? ##

_[[Tim Porter|Tim]]_: I would like to pose a question on the Homotopy Hypothesis.  Playing devil's advocate for the moment, since Kan complexes, and simplicially enriched categories, both satisfy the homotopy hypothesis, why bother to search for other models?  That is a bit severe of course so a more 'constructive' form of the question is what criteria should we be looking to be satisfied so as to say that a model of homotopy types is a good one?  (Perhaps things like that the basic homotopy operations, such as Whitehead or Samelson products, should have clear formulations and clear interpretations.  The higher operations could then be gradually required.  The relation between obstructions to interchange laws (interchangeator!) and the low dimensional Whitehead products are 'clear' even if not that immediately evident in most writing on the subject (and I include my own in that!), but in higher dimensions .... ?

_[[Mike Shulman|Mike]]_: My perspective is that we are looking for good notions of _$\infty$-category_ such that the _induced_ notion of $\infty$-groupoid satisfies the homotopy hypothesis.  If all you want is to do homotopy theory, then homotopy theorists have gotten along quite well for decades with topological spaces, Kan complexes, and the like (although one might certainly hope, as you suggest, to get information about homotopy operations out as well).  But as category theorists, we want a notion of $\infty$-category with not all cells necessarily invertible, which behaves well _categorically_ rather than homotopically, but whose induced notion of $\infty$-groupoid still satisfies the homotopy hypothesis as a "check" or "anchor."  It's hard to exhibit Kan complexes as the $(\infty,0)$-case of a notion of $\infty$-category; there are [[quasi-category|quasicategories]] for $(\infty,1)$-categories but beyond that it gets tricky (there is Street's original definition, but it's quite difficult to work with).

[[Urs Schreiber|Urs]]: Lurie is now talking in (electronic) print about $(\infty,n)$-categories, [here](http://www-math.mit.edu/~lurie/papers/cobordism.pdf).

_[[Mike Shulman|Mike]]_: When I glanced at that, it looked as though he was actually using [[Segal category|Segal categories]] for his $(\infty,n)$-categories rather than some generalization of quasicategories.

_[[Tim Porter|Tim]]_: I think, Mike, you are missing my point. You use the word 'good' with regard to notion. My point is that the higher homotopy operations ARE categorical structures that WILL  BE there in the various models. For instance, there are formulae given in Curtis's old survey article for the Samelson product in a simplicial group.  (No proof is available in the literature.) This uses shuffle products and various combinatorial ideas that fit well from the categorical viewpoint. As category theorists we can hope to find new understanding of what makes the infinity groupoid models work and hence what the infinity category models should be. As these products DO use inverses the problem of interpreting their analogue in an infinity category is not easy.  I feel it has, from my perspective, something to do with the basic homotopy coherent cube and the free simplicial cat resolution of a category, but I am not sure how to handle it. 

_[[Mike Shulman|Mike]]_: I think we are talking past each other.  I was trying to answer your question "why bother to search for other models?" by saying that from my perspective, what we're doing isn't just searching for new models for spaces, but rather searching for a good notion of $\infty$-category that still reduces to a model for spaces.  I took your mention of higher homotopy operations as a proposed answer to the first question "why bother to search for other models?"  So I wasn't addressing homotopy operations specifically -- I don't have any disagreement with it -- just pointing out that there are also other answers to the first question.

_[[Ronnie Brown|Ronnie]]_: What is wrong with strict $n$-fold groupoids as a model of homotopy $n$-types? This is a theorem, not an hypothesis! (Loday, Porter).  One advantage of these is that one can do some calculations with them, using a higher homotopy van Kampen theorem, which Grothendieck interpreted as integration of homotopy types. 

They are certainly a very rich structure, with other interpretations of special cases. My question is: what are the expected purposes of these other models? My aim since 1966 has been to find  models which seem to give a natural extension of group theory, and hence to work with strict structures. My hypothesis is that this can always be done, if you can find the means to make the lax conditions part of the algebra. 

What held me up for 9 years in constructing higher homotopy groupoids was to concentrate on spaces: when Philip Higgins and I started to look at pairs of spaces, then things quickly fell into place. Thus the clear functors from strict $n$-fold groupoids give rise to  _structured spaces_. What is wrong with that? 

_[[Mike Shulman|Mike]]_: I don't think anyone is saying that there is anything _wrong_ with strict $n$-fold groupoids as a model of homotopy $n$-types or structured spaces.  I certainly don't think there is.  I think that probably the feeling is that having a variety of different combinatorial models means having a variety of different tools, each of which may have its advantages and disadvantages.  Ordinary topological spaces and simplicial sets also have advantages and disadvantages.  Tim already mentioned some of the hopes that some people have for $n$-groupoids as a model of $n$-types: more insight into homotopy operations such as Whitehead products.  I'm not a calculational homotopy theorist myself, but it seems plausible.

And, as I said before, I think another purpose of the homotopy hypothesis is to use modeling of $n$-types by groupoids as a litmus test for a good notion of $n$-*category*, irrespective of whether this modeling gives us any new information about the $n$-types.  And I do personally feel that strict $n$-fold categories have something to tell us in this picture that has not been properly investigated (or, at least, if it has, I'm not aware of it).

_[[Ronnie Brown|Ronnie]]_: I entirely agree with Mike on _horses for courses_. It is helpful also to analyse what are and should be the _courses_!. There are and will be many of them. There is already a  description of Whitehead products $\pi_2 \times \pi_2 \to \pi_3$ in the classifying space of a crossed square, using the $h$ map.  
 
_[[John Baez]]_: Just to reiterate some of Mike Shulman's points:  

1) Weak $\infty$-categories are important in themselves, for a myriad of reasons.  

2) Any notion of weak $\infty$-category for which the corresponding weak $\infty$-groupoids don't model homotopy types is **wrong**.  

3) Therefore, for every proposed definition of weak $\infty$-category, we must check that the corresponding weak $\infty$-groupoids model homotopy types.  

Similar remarks apply to all proposed concepts of $n$-category and $(\infty,n)$-category.

## $cat^n$ groups ##

_[[Urs Schreiber|Urs]]_: I looked at Ronnie Brown's review article above, but didn't find Loday's '81 article yet. Maybe somebody can help me: what is the map from spaces to $cat^n$-groups which comes from the equivalence in Loday's theorem? I am asking because the natural guess would be that we send a space to its $n$-fold  fundamental groupoid $\Pi_{n-fold}(X)$ in what should be an obvious way. But that cubical $n$-groupoid $\Pi_{n-fold}(X)$ will have thin fillers ("connections") etc and hence be equivalent to a strict $n$-groupoid, which is known _not_ to model all homotopy types. How is this resolved?

_[[John Baez]]_: See Section 5 of [Simona Paoli's paper](http://www.maths.mq.edu.au/~simonap/paoli_IMA.pdf#). 

_[[Ronnie Brown|Ronnie]]_: This is a good question. The argument of Loday (1982) for getting a _cubical resolution_
of spaces was developed in 

R. Steiner,  Resolutions of spaces by $n$-cubes
of fibrations. J. London Math. Soc. (2) 34 (1986),
169-176.

It does not lead to an easily analysed functor $\Pi$! 

However since the models usually discussed have some kind of structure such as a filtration one would expect the spaces modelled to have an analogous structure. In particular, $n$-fold categories (groupoids) have a multiple filtered  structure. It may not be unexpected that there are problems in possible inverse functors or constructions to the forgetful functor (structured space) $\to$ (spaces).  

Analogously, squashing from a multiple strict structure to a globular structure may necessitate certain non-strictness; this has been analysed in some cases by Simona Paoli. 

It is interesting that Urs thinks there should be _obvious_ functors from spaces to the algebraic model. It was for us quite a sweat to produce the full structure of cubical $\omega$-groupoid with connections from a filtered space, the main problem being to prove the compositions are well defined on the appropriate homotopy classes. Even the existence of the functor 

$$ \Pi: (n-cubes of spaces) \to (cat^n-groups)$$

encapsulates a lot of information, as  is shown by the complications of the Ellis-Steiner crossed $n$-cubes of groups, and their nontrivial equivalence with [[cat-n-group]]s. 

_[[Mike Shulman]]_: I'm guessing that what Urs had in mind is more like "intuitively obvious."  Taking the example of [[Batanin ∞-categories]] with which I'm a little more familiar, the underlying globular set of the fundamental $\omega$-groupoid is certainly "obvious" but some work is required to produce the globular operad and its action.  (Perhaps the amount of work required is roughly proportional to the "algebraicity" of the definition of $\omega$-category in use?)

I now have to ask a possibly-controversial question that I've been sitting on for a while, namely "Are $cat^n$-groups really an instance of the homotopy hypothesis?"  (Or more precisely, a _relative_ of it, since the homotopy hypothesis proper deals only with $n$-groupoids.)  To me one of the essential aspects of the homotopy hypothesis is that $n$-groupoids are considered up to _categorical_ [[equivalence]] when modeling homotopy $n$-types.  The [[Thomason model structure]] whereby 1-categories model all homotopy types is _not_, in my view, an instance of the homotopy hypothesis, because the notion of "equivalence" used in $Cat$ is not the categorical one.  (Of course, this detracts nothing from the importance or usefulness of modeling homotopy types in this way; it is just a question of terminology and conceptual clarity.)  Thus, in order to consider Loday's result a relative of the homotopy hypothesis, I would like to know that the notion of "equivalence" of $cat^n$-groups that it uses is in some sense "categorical."  So is it?  I don't mean to imply that I think the answer is no; I really don't know the answer.  In fact, it's not even clear to me how to make the question precise.
