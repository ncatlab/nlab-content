
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Descent and locality
+-- {: .hide}
[[!include descent and locality - contents]]
=--
=--
=--

# Descent morphisms
* table of contents
{: toc}

## Idea

Given a [[fibered category]], a morphism along which the induced comparison functor between the category of the descent data and the codomain fiber is fully faithful (equivalence of categories) is said to be a descent morphism (resp. effective descent morphism). 


## The case of codomain fibration 

### Definition

Let $C$ be a [[category]] with [[pullbacks]].  For any [[morphism]] $p\colon A\to B$, we have an [[internal category]] $ker(p)$ defined by $A\times_B A \rightrightarrows A$ (the [[kernel pair]] of $p$).  The category of [[descent data]] for $p$ is the category $C^{ker(p)}$ (the "[[descent object]]") of internal diagrams on this internal category.  Explicitly, an object of $C^{ker(p)}$ is a morphism $C\to A$ together with an action $A\times_B C \to C$ satisfying suitable axioms.

The evident internal functor $ker(p) \to B$ (viewing $B$ as a [[discrete category|discrete]] internal category) induces a *comparison functor* $C^B \to C^{ker(p)}$.  We say that $p$ is:

* a **descent morphism** if this comparison functor is [[fully faithful functor|fully faithful]], and
* an **effective descent morphism** if this comparison functor is an [[equivalence of categories]].

It is a little unfortunate that the more important notion of *effective descent* has the longer name, but it seems unwise to try to change it (although the [[Elephant]] uses "pre-descent" and "descent").

### Properties

Let $C$ be a category with pullbacks.

+-- {: .un_theorem}
###### Theorem
$p\colon A\to B$ is a descent morphism if and only if $p$ is a [[pullback-stability|stable]] [[regular epimorphism]].
=--

In particular, descent morphisms are closed under [[pullback]] and [[composition]].  Moreover, in a [[regular category]], the descent morphisms are precisely the regular epimorphisms.

Perhaps more surprising is:

+-- {: .un_theorem}
###### Theorem
Effective descent morphisms are closed under pullback and composition.
=--

See ([ST](#ST)) and ([RST](#RST)) for proofs.

## General case

In general, [[descent]] is about higher [[sheaf]] conditions (i.e. [[stack]] conditions). More precisely, being an $n$-stack means that all
covers in the base are effective $n$-categorical descent morphism. Hence the morphism being of effective descent is a building block, the single morphism case of a stack condition. 

Thus, being an effective descent morphism says that the corresponding fibered category is a 1-stack ("2-sheaf") for the singleton covering family $p$.  Similarly, $p$ is a descent morphism iff the codomain fibration is a pre-stack (that is, a 2-separated 2-presheaf) for $p$.

More generally, we may use the terms "descent morphism" and "effective descent morphism" relativized to any [[fibration]] or [[indexed category]] rather than the codomain fibration.

We can also, of course, generalize to higher categories: an [[n-category]] with pullbacks has an analogue of a "codomain fibration", and we can ask for stack conditions on it.  This is most common in the case of [[(infinity,1)-categories]]; see the page [[descent]] for more information and links.

Descent can sometimes (for this we need to have also the direct image functor) be rephrased in terms of the [[monadicity theorem]]; see [[monadic descent]].

## Examples

If $C$ is [[exact category|exact]], or has stable [[reflexive coequalizers]], then every 
[[regular epimorphism]] is an effective descent morphism.  (See, for instance, section B1.5 of the [[Elephant]].)  In particular, this is the case for any [[topos]].

However, there are also important effective descent morphisms in non-exact categories.

* In [[Top]], there are characterizations of effective descent morphisms, see \cite{EDM}.

* In the category [[Loc]] of [[locales]], every [[triquotient map]] is an effective descent morphism.  These includes [[open map|open]] surjections and also [[proper map|proper]] surjections.

...

Of course, there are also many effective descent morphisms relative to fibrations other than the codomain fibration.  If $A$ is a [[stack]] for a particular [[Grothendieck topology]], then every singleton cover in that topology will be, by definition, an effective descent morphism relative to $A$.  A few important examples are:

* Every [[fpqc site|fpqc cover]] of [[schemes]] is an effective descent morphism relative to the indexed category $QCoh(-)$ of [[quasicoherent sheaves]].

...

## Related concepts

* [[descent]]

  * [[cover]]

  * [[cohomological descent]]

  * **descent morphism**

  * [[monadic descent]], 

    * [[Sweedler coring]]

    * [[higher monadic descent]]

    * [[descent in noncommutative algebraic geometry]]

* [[sheaf]], [[(2,1)-sheaf]], [[2-sheaf]] [[(∞,1)-sheaf]]


## References

* M. Sobral, [[Walter Tholen|W. Tholen]], _Effective descent morphisms and effective equivalence relations_, Category Theory 1991, CMS Conference Proceedings __13__ (1992), 421--433
 {#ST}

* J. Reiterman, M. Sobral, [[Walter Tholen|W. Tholen]], _Composites of effective descent maps_, Cahiers __34__ (1993), 193--207, [numdam](http://www.numdam.org/item?id=CTGDC_1993__34_3_193_0)
 {#RST}


\bibitem{EDM} [[Maria Manuel Clementino]], [[George Janelidze]],
_Another note on effective descent morphisms of topological spaces and relational algebras_.
Topology Appl. 273 (2020), 106961.
[DOI](https://doi.org/10.1016/j.topol.2019.106961).

[[!redirects descent morphism]]
[[!redirects descent morphisms]]
[[!redirects effective descent morphism]]
[[!redirects effective descent morphisms]]
[[!redirects descent map]]
[[!redirects descent maps]]
[[!redirects effective descent map]]
[[!redirects effective descent maps]]
