
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

A "pure" *1-categorical* notion of embedding is as follows. 

+-- {: .num_defn} 
###### Definition 
An *embedding* of a category $C$ into a category $D$ is a [[functor]] $F: C \to D$ whose application to morphisms is an [[injective function]] $Mor(C) \to Mor(D)$. 
=-- 

This definition is adopted in [Adamek-Herrlich-Strecker](#AHS) and in [Riehl](#Riehl), for example. In this definition we accept that categories are [[strict categories]], where objects can be compared for [[equality]]. It follows that if $F(c) = F(c')$ for objects $c, c'$ of $C$, then $F(1_c) = F(1_{c'})$ and thus $1_c = 1_{c'}$ by injectivity on morphisms, whence $c = c'$. Thus, embeddings in this sense necessarily yield injective functions $Ob(C) \to Ob(D)$ on the object classes. 

Embeddings in this sense are straightforwardly the same thing as [[monomorphisms]] in the $1$-category [[Cat]]. They are also the same as [[faithful functors]] which are injective on objects. 

A *full embedding* in this sense is an embedding that is also a [[full functor]]. 

On the other hand, a "pure" *2-categorical* notion of embedding as follows. 

+-- {: .num_defn} 
###### Definition 
An *embedding* of a category $C$ into a category $D$ is a [[fully faithful functor]] $F: C \to D$. 
=-- 

## Related concepts

* [[Barr embedding theorem]]

* [[embedding]] 

## References 

* {#AHS} [[Jiří Adámek]], [[Horst Herrlich]], and [[George Strecker]], *Abstract and Concrete Categories: The Joy of Cats*, John Wiley and Sons 1990. ([Online edition](http://katmat.math.uni-bremen.de/acc/)) 

* {#Riehl} [[Emily Riehl]], *Category Theory in Context*, Dover Publications, Inc. 2016. ([pdf](http://www.math.jhu.edu/~eriehl/context.pdf)) 

[[!redirects embedding of categories]]