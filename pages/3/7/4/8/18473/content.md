
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In much of mathematics, certainly in the traditional treatment of mathematical [[structure in model theory|structures]] from the point of view of [[logic]] and [[model theory]], an "[[embedding]]" is typically a [[monomorphism]] between structures that preserves *and reflects* the structure specified within a given [[language]] or [[theory]]. Such a notion is often definable directly in terms of [[category theory]], i.e., in terms of properties of morphisms in the designated category of structures and structure-preserving maps. 

But for categories themselves, the situation and practice is more complicated, with no notion of "embedding of categories" that is universally accepted in the literature. A critical dividing line, leading to several distinct notions of embedding, lies in how one views the [[Cat|category of categories]]: 

* If we view categories as mathematical structures in the traditional sense, with central concepts being definable in the ordinary 1-category of categories and [[functors]] (which are the relevant structure-preserving maps), then notions of embedding tend to emphasize they should be [[injective maps]] on the classes of objects (and more besides). 

* If we view categories however as having a higher-dimensional aspect, i.e., if we view central concepts as being based rather on the [[2-category]] of categories, functors, *and* [[natural transformations]], then different notions of embedding come to the fore, where notably the assumption of injectivity on the object-classes clashes with the [[principle of equivalence]] (and is therefore rejected). 

In this article we survey the various notions of categorical embedding that have appeared in the literature, and try to describe some of the underlying contexts and rationales. 

## Definitions 

### 1-categorical definitions

Perhaps the most obvious 1-categorical definition of embedding is:

* a [[functor]] $F: C \to D$ that is both injective on objects and a [[faithful functor]].

This definition is adopted in [Adamek-Herrlich-Strecker](#AHS) and in [Riehl](#Riehl), for example.  In this definition we accept that categories are [[strict categories]], where objects can be compared for [[equality]].  Embeddings in this sense are straightforwardly the same thing as [[monomorphisms]] in the $1$-category [[Cat]].

If we define categories with [one collection of morphisms](/nlab/show/category#OneCollectionOfMorphisms), then this definition is equivalent to saying that the action of $F$ on morphisms is an [[injective function]] $Mor(C) \to Mor(D)$.  In particular, if this latter condition holds and $F(c) = F(c')$ for objects $c, c'$ of $C$, then $F(1_c) = F(1_{c'})$ and thus $1_c = 1_{c'}$ by injectivity on morphisms, whence $c = c'$.

However, as noted above, in many cases an "embedding" means something *stronger* than a mere monomorphism, being required to reflect "all the structure".  For instance, an embedding of [[topological spaces]] is a subspace inclusion, not merely an injective continuous map (the latter being the monos in [[Top]]).

In particular, the above definition of embedding does not even reflect the property of objects being isomorphic, so that it is not necessarily injective on isomorphism classes of objects!  This suggests that a (still 1-categorical) embedding of categories ought to be something stronger.  Some possibilities include:

* The [[regular monomorphisms]] or [[extremal monomorphisms]] in [[Cat]] (what are those?)
* Monomorphisms in $Cat$ that are also [[full functors]], hence [[fully faithful functors]].  These are sometimes called **full embeddings**.
* Monomorphisms in $Cat$ that are also injective on isomorphism classes of objects (this is used in [[Toposes, Triples, and Theories]]), or more strongly that are also [[pseudomonic functors]].

### 2-categorical definitions

Most of the above 1-categorical notions of embedding corresponds to a "pure" 2-categorical notion by simply removing the injectivity on objects.  Thus we have the following candidates:

* [[faithful functors]]
* [[fully faithful functors]]
* [[pseudomonic functors]]

The choice between these is closely related to the question of giving an equivalence-invariant notion of [[subcategory]].

### Relationship

Every fully faithful functor is *equivalent* to one that is fully faithful and injective on objects.  Let $f:C\to D$ be fully faithful, and let $E$ be the "mapping cylinder" category, whose objects are the disjoint unions of those of $C$ and $D$, with $C$ and $D$ embedded fully-faithfully (and of course injectively on objects), and $E(c,d) = D(f c,d)$ and $E(d,c) = D(d,f c)$.  Full-faithfulness of $f$ allow us to compose all arrows in $E$ making it a category.  There is a projection $E\to D$ that is the identity on $D$ and acts by $f$ on $C$, and which is an inverse equivalence to the inclusion $D\to E$.  Thus, $f:C\to D$ is equivalent, in the 2-category whose objects are functors and whose morphisms are pseudo-commutative squares, to the inclusion functor $C\to E$, which is fully faithful and injective on objects.

## Examples

### The Yoneda embedding

Probably the most common embedding of categories encountered is the [[Yoneda embedding]].  This is fully faithful, but whether or not it is always injective on objects depends on set-theoretic details of how we define categories.  If we use a definition of category with [a family of collections of morphisms](/nlab/show/category#AFamilyOfCollectionsOfMorphisms), then it might happen that two distinct (but necessarily isomorphic) objects $x$ and $y$ have $C(z,x) = C(z,y)$ as sets for all $z\in C$, so that the Yoneda embedding would take $x$ and $y$ to literally the same presheaf.  (Such an equality of hom-sets is not as weird as it might sound; for instance, when regarding a [[preordered set]] as a category it's natural to define every nonempty homset to be the *same* [[terminal set]].)

## Related concepts

* [[Barr embedding theorem]]

* [[embedding]] 

* [[subcategory]]

## References 

* {#AHS} [[Jiří Adámek]], [[Horst Herrlich]], and [[George Strecker]], *Abstract and Concrete Categories: The Joy of Cats*, John Wiley and Sons 1990. ([Online edition](http://katmat.math.uni-bremen.de/acc/)) 

* {#Riehl} [[Emily Riehl]], *Category Theory in Context*, Dover Publications, Inc. 2016. ([pdf](http://www.math.jhu.edu/~eriehl/context.pdf)) 

[[!redirects embedding of categories]]
