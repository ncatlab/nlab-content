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

If one says that two *objects* $A$ and $B$ are "unnaturally isomorphic", it might mean that they are the images of two functors that are unnaturally isomorphic, but it might also mean only that there is no obvious way even to make them the images of two functors.  For instance, this seems to be the meaning in Section 1.1 of [Strickland](#Strickland1998).

## Reasons for unnaturality

Intuitively, there are several reasons that an isomorphism might fail to be natural.

* Two functors of opposite variances (one covariant and one contravariant) *cannot* be naturally isomorphic in the usual sense.  However, they can be [[dinatural transformation|dinaturally isomorphic]], so this is not really a "reason for a failure of naturality".

* In defining an isomorphism, it may be necessary to make certain arbitrary choices.  If making these choices differently would yield a different isomorphism, then usually the isomorphism will not be natural.


## Making the unnatural natural

Unnatural isomorphisms are not very well-behaved mathematically, so if we have an unnatural isomorphism we may want to "make it natural".  There are several ways to do this:

1. Use a different definition that includes more structure, such as [[derivators]] instead of [[triangulated categories]].  For instance, see [comment to OP's question referring to triangulated categories](#MathOverflow2013).

2. Relatedly, pass to a [[higher categories|higher-categorical]] context in which a non-commuting square can commute up to a higher transformation; see [[pseudonatural transformation]] and [[lax natural transformation]].

3. Cut down to a smaller class of morphisms in the domain category for which the naturality square does commute.


## Natural, canonical, and functorial

The use of adjectives like _canonical_, _invariant_,  _functorial_, _natural _ is sometimes satirized.  For example, an influential German textbook mocks one of the terms in a footnote, and (#MathOverflow2010) gives a citation which is another example of such mockery.

+--{: .query}
If we want to keep that remark, we should say something about what about them is being mocked and why.
=--

These three terms can be distinguished in the following way:

* The definition of a single function or operation is "canonical" if there are "no arbitrary choices" involved in it, or more precisely if the end result is independent of any arbitrary choices that we had to make in defining it.  In category theory, we generally consider something "canonical" if this independence is "up to unique isomorphism" in an appropriate sense, such as the definition of [[generalized the|the]] limit functor on a category with limits.
* The definition of a function taking the [[objects]] of a category into the objects of another is _functorial_ if we have also supplied a function on morphisms making it into a [[functor]], or more loosely uf such a function exists (although in practice one always has a particular such function in mind).
* The definition of a function taking the objects of one category into morphisms of another is _natural_ if it forms a natural isomorphism between two functors (generally assumed to be given).

## Examples

* The term _unnatural isomorphism_ is often used in [[homological algebra]], in particular in discussions of splittings. An example is [Theorem 4.3](#HiltonStammbach71), which explictly uses the term to decribe an isomorphism between Hom- and Ext-functors.

* Species are functors for which unnatural isomorphisms are often discussed. Examples are [this MO comment](#GesselTrimble2014) and also [Definition 3.3.4](#Yorgey2014), which defines an equivalence relation on the class of all species by explicitly using the term, defining an "equipotence between species [...] as an "unnatural" isomorphism between [the two species in question]", however, in _another_ sense, which will not be spelled out here, than discussed in  [MathOverflow2013](#MathOverflow2013).

* See [MathOverflow2013](#MathOverflow2013). 


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

[[!redirects unnatural isomorphism]]
[[!redirects unnatural isomorphisms]]
[[!redirects unnaturally isomorphic]]
[[!redirects unnaturally isomorphic functors]]
[[!redirects objectwise isomorphism]]
[[!redirects objectwise isomorphisms]]
[[!redirects pointwise isomorphism]]
[[!redirects pointwise isomorphisms]]
