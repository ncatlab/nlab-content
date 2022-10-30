# Unnatural isomorphisms #
* table of contents
{:toc}

## Idea

A [[natural isomorphism]] is the "correct" notion of [[isomorphism]] between [[functors]].  Informally, one sometimes speaks of two [[objects]] being "naturally isomorphic" if they are the images of two functors that are naturally isomorphic.  However, sometimes one encounters functors that are "pointwise isomorphic" but *not* naturally.  There is not much to say *mathematically* about such "unnatural isomorphisms", but some discussion of them can help the intuitive understanding of natural isomorphisms and their importance.

On this page we will adhere to the convention that an "unnatural isomorphism" means an isomorphism that is not *necessarily* natural (but might be), similarly to how a "noncommutative [[ring]]" might happen to be commutative.  The word "unnatural" is not to be taken perjoratively or as suggesting that unnatural isomorphisms are rare; in [[cardinality]] terms there are many more unnatural isomorphisms than natural ones, although in mathematical practice surprisingly many isomorphisms are indeed natural.  Other possible terms with the same meaning are "pointwise isomorphic" or "objectwise isomorphic".

The term "natural" is used for traditional reasons, cf. [EilenbergMac Lane45](#EilenbergMacLane45), and is an example of the common phenomenon that concepts branded _natural_, _normal_ or _regular_ tend to be rather non-generic or non-random.  In fact, [Eilenberg and MacLane](#EilenbergMacLane45) comment (cf. p. 233, first paragraph in loc. cit) on the term, associating it with an intuition of _simultaneity_, rather than genericity.  This intuition is in tune with conceiving of naturality as generalized _commutatitivity_.

## Definition

### Between functors

Let $F,G:C\to D$ be [[functors]].  An *unnatural isomorphism* between $F$ and $G$ consists of, for each [[object]] $c\in C$, an isomorphism $F(c) \cong G(c)$, satisfying no further conditions.

Note that if each component of a [[natural transformation]] is an isomorphism, then it is necessarily a natural isomorphism.  (Depending on the definition of "natural isomorphism", this could be a tautology; but the non-tautologous statement is that if each component of a natural transformation is an isomorphism then it is an isomorphism in the functor category.  This statement, though non-tautologous, is easy to prove for 1-categories, but more difficult for higher categories.)

More generally, an unnatural isomorphism (or transformation) might be natural with respect to only *some* morphisms in the domain, such as for instance the isomorphisms.  Some people have proposed calling transformations that are natural only with respect to isomorphisms "canonical".

### Between objects

If one says that two *objects* $A$ and $B$ are "unnaturally isomorphic", it might mean that they are the images of two functors that are unnaturally isomorphic, but it might also mean only that there is no obvious way even to make them the images of two functors. For instance, this seems to be the meaning in Section 1.1 of [Strickland](#Strickland1998). Somewhat relatedly, there is no way of making constructions such as "algebraic closure of a field" or "injective hull of an $R$-module" functorial, if the desired embeddings into these constructions are to be natural, and this precludes speaking of any two such constructions as "naturally isomorphic". We touch on this again below, but see [here](#AHRT). 

## Reasons for unnaturality

Intuitively, there are several reasons that an isomorphism might fail to be natural.

* Two functors of opposite variances (one covariant and one contravariant) *cannot* be naturally isomorphic in the usual sense.  However, they can be [[dinatural transformation|dinaturally isomorphic]], so this is not really a "reason for a failure of naturality".

* In defining an isomorphism, it may be necessary to make certain arbitrary choices.  If making these choices differently would yield a different isomorphism, then usually the isomorphism will not be natural.


## Making the unnatural natural

Unnatural isomorphisms are not very well-behaved mathematically, so if we have an unnatural isomorphism we may want to "make it natural".  There are several ways to do this:

1. Use a different definition that includes more structure, such as [[derivators]] instead of [[triangulated categories]].  See for instance this [Wikipedia discussion](https://en.wikipedia.org/wiki/Triangulated_category#Are_there_better_axioms.3F) on axioms for triangulated categories. 

2. Relatedly, pass to a [[higher categories|higher-categorical]] context in which a non-commuting square can commute up to a higher transformation; see [[pseudonatural transformation]] and [[lax natural transformation]].

3. Cut down to a smaller class of morphisms in the domain category for which the naturality square does commute.


## Natural, canonical, and functorial

The use of adjectives like _canonical_, _invariant_, _functorial_, _natural _ is sometimes satirized. For example, as quoted in [MO2010](#MathOverflow2010), Andr&#233; Weil writes:

> I can assure you, at any rate, that (...) my results are invariant, probably canonical, perhaps even functorial. (*Oeuvres*, vol. 2, page 558)

which may be subtly mocking. An influential German textbook also mocks one of the terms in a footnote. 

+--{: .query}
If we want to keep that remark, we should say something about what about them is being mocked and why.
=--

These three terms can be distinguished in the following way:

* The definition of a single function or operation is "canonical" if there are "no arbitrary choices" involved in it, or more precisely if the end result is independent of any arbitrary choices that we had to make in defining it.  In category theory, we generally consider something "canonical" if this independence is "up to unique isomorphism" in an appropriate sense, such as the definition of [[generalized the|the]] limit functor on a category with limits.
* The definition of a function taking the [[objects]] of a category into the objects of another is _functorial_ if we have also supplied a function on morphisms making it into a [[functor]], or more loosely uf such a function exists (although in practice one always has a particular such function in mind).
* The definition of a function taking the objects of one category into morphisms of another is _natural_ if it forms a natural isomorphism between two functors (generally assumed to be given).

## Examples

1. Let $U: Vect\to Aff$ be the functor taking the underlying [[affine space]] of a [[vector space]], and $D:Aff\to Vect$ the functor constructing the vector space of displacements of an affine space.  Then there is a *natural* isomorphism $D \circ U \cong Id_{Vect}$, but only an *unnatural* isomorphism "$U \circ D \cong Id_{Aff}$".  In particular, these functors do not form an [[equivalence of categories]]. A similar phenomenon occurs with [[groups]] and [[heaps]], and with [[torsors]] of groups.

1. As a particular example of the last phenomenon: there is a bijective correspondence between [[linear order|linear orderings]] of a set $S$ and [[permutations]] of $S$. Indeed, the set $Lin(S)$ is a [[torsor]] over $Perm(S)$: there is a group action $\alpha: Perm(S) \times Lin(S) \to Lin(S)$ such that for any *choice* of linear ordering $L$, the map $\alpha(-, L): Perm(S) \to Lin(S)$ is a bijection. But, there is no canonical choice of ordering $L$. 

1. [[species|Species]] are functors for which unnatural isomorphisms are sometimes discussed. For example, the species of linear orders is unnaturally isomorphic to the species of permutations; for a related example, see the commentary under this MathOverflow answer [MO2014](#GesselTrimble2014). [Yorgey2014](#Yorgey2014) explicitly uses the term: his definition 3.3.4 introduces an "equipotence between species (...) as an "unnatural" isomorphism between [the two species in question]". 

1. The term _unnatural isomorphism_ is often used in [[homological algebra]], in particular in discussions of splittings of exact sequences. An example is [Hilton-Stammbach, Theorem 4.3](#HiltonStammbach71), which explicitly uses the term to describe an isomorphism between Hom- and Ext-functors.  More generally, _unnatural transformations_ also often occur in homological algebra. 

* It is often said that while there is an isomorphism between the [[field]] of [[complex numbers]] $\mathbb{C}$ and the completion $\mathbf{C}_p$ (with respect to the canonical absolute value) of the algebraic closure of the [[p-adic numbers]] $\mathbb{Q}_p$, this isomorphism is not natural. This statement, while somewhat loose since there are no functors specified, can be made formally precise along the lines of [Ad&#225;mek, Herrlich, Rosick&#253;, and Tholen](#AHR). The abstract reads: 
> In a category with injective hulls and a cogenerator, the embeddings into injective hulls can never form a natural transformation, unless all objects are injective. In particular, assigning to a field its algebraic closure, to a poset or Boolean algebra its MacNeille completion, and to an $R$-module its injective envelope is not functorial, if one wants the respective embeddings to form a natural transformation.

* See [MathOverflow2013](#MathOverflow2013). 


## References

* {#AHRT} [[Adamek|Ji?í Adámek]], [[Horst Herrlich]], [[Rosicky|Ji?í Rosický]], and [[Walter Tholen]], *Injective Hulls are not Natural*, algebra universalis
Volume 48, Issue 4 (December 2002), 379&#8211;388. ([Citeseer link](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.8.194)) 

* {#EilenbergMacLane45} [[Samuel Eilenberg|S. Eilenberg]], [[Saunders Mac Lane|S. Mac Lane]], _General Theory of Natural Equivalences_,  Transactions of the American Mathematical Society Vol. 58, No. 2 (Sep., 1945), pp. 231-294 ([JSTOR](http://www.jstor.org/stable/1990284))

* {#HiltonStammbach71} [[Peter Hilton|P. Hilton]],  U. Stammbach, _A course in homological algebra_, Springer-Verlag, New York, 1971, Graduate Texts in Mathematics, Vol. 4.

* {#MathOverflow2010} Konrad Waldorf (https://mathoverflow.net/users/3473/konrad-waldorf), What is the definition of "canonical"?, URL (version: 2013-11-13): [https://mathoverflow.net/q/19644](https://mathoverflow.net/q/19644) 

* {#MathOverflow2013} Bugs Bunny (https://mathoverflow.net/users/5301/bugs-bunny), Example of an unnatural isomorphism, URL (version: 2013-08-14): [https://mathoverflow.net/q/139388](https://mathoverflow.net/q/139388)

* {#MathOverflow201308} Almeo Maus (https://mathoverflow.net/users/29853/almeo-maus), Unicity of Yoneda isomorphism, URL (version: 2013-08-24): [https://mathoverflow.net/q/140303](https://mathoverflow.net/q/140303) 

* {#GesselTrimble2014} [[Todd Trimble]] (https://mathoverflow.net/users/2926/todd-trimble), What are some examples of interesting uses of the theory of combinatorial species?, URL (version: 2011-03-23): [https://mathoverflow.net/q/59259](https://mathoverflow.net/q/59259) 

* {#Rezk16} [[Charles Rezk]], _Stuff about quasicategories_, Lecture Notes for course at University of Illinois at Urbana-Champaign, 2016, version May 2017,([pdf](http://math.uiuc.edu/~rezk/595-fal16/quasicats.pdf))

* {#Strickland1998} [[Neil Strickland|N. P. Strickland]], Morava E-Theory, Topology, Vol. 37, No. 5 (1998), 757--779

* {#Yorgey2014} [[Brent Yorgey|B. A. Yorgey]], Combinatorial Species and Labelled Structures,  Dissertation, University of Pennsylvania, 2014

[[!redirects unnatural isomorphism]]
[[!redirects unnatural isomorphisms]]
[[!redirects unnaturally isomorphic]]
[[!redirects unnaturally isomorphic functors]]
[[!redirects objectwise isomorphism]]
[[!redirects objectwise isomorphisms]]
[[!redirects pointwise isomorphism]]
[[!redirects pointwise isomorphisms]]
