
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Categories of categories
+-- {: .hide}
[[!include categories of categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

$\mathbf{Prof}$ is the [[2-category]] of [[categories]], [[profunctors]], and [[natural transformations]].  

Recall that a profunctor from $A$ to $B$ is a functor $B^{op}\times A\to Set$.  Composition of profunctors in $Prof$ is by the "tensor product of functors" [[coend]] construction: if $H\colon A\to B$ and $K\colon B\to C$, their composite is given as a functor $C^{op}\times A \to Set$ by
$$(c,a)\mapsto \int^{b\in B} H(b,a)\times K(c,b).$$
The identity on a category $A$ is its hom-functor $Hom_A(-,-)$.



## Properties

If profunctors are [[categorification|categorified]] [[binary relations]], then $Prof$ is a categorification of [[Rel]].

Note that as defined here, $Prof$ is a weak $2$-[[2-category|category]] or [[bicategory]].  A naturally defined equivalent [[strict 2-category]] has the same objects, but the morphisms $A\to B$ are [[cocontinuous functor]]s $P A \to P B$, where $P A$ is the [[presheaf category]] of $A$.  This is equivalent because a profunctor $A\to B$ can equivalently be regarded as a functor $A\to P B$, and $P A$ is the [[free cocompletion]] of $A$.  This equivalence is an instance of [[Lack's coherence theorem]].

Note that every functor $f\colon A\to B$ gives two [[representable functor|representable]] profunctors $B(f-,-)$ and $B(-,f-)$.  This defines two [[2-functors]] $Cat \to Prof$ that are  the identity on objects.  The relationship between [[Cat]] and $Prof$ encoded in this way makes them into an [[equipment]].

$Prof$ is a sort of classifying object for arbitrary functors; see [[displayed category]].

There are also [[enriched category|enriched]] and [[internal category|internal]] versions of $Prof$. These accordingly refine [[categories of enriched categories]].

$Prof$ is a [[locally cocomplete bicategory]].

## Related concepts

* [[Pos]]

* [[Set]]

  * [[Rel]], [[Span]], **Prof**

* [[Grpd]], [[∞Grpd]]

* [[Cat]], 

  * [[Operad]]

  * [[VCat]]

* [[2Cat]]

* [[(∞,1)Cat]]

  * [[(∞,1)Operad]]

* [[(∞,n)Cat]]

## References


* [[Maren Justesen]], *Bikategorien af Profunktorer*, Aarhus 1968 ([pdf](https://ncatlab.org/nlab/files/Justesen_Profunktoren.pdf))


category: category