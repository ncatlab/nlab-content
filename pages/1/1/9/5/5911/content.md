
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Definition

An **infinitary [[coherent category]]** or **geometric category** is a [[regular category]] in which the [[subobject]] [[poset]]s $Sub(X)$ have all _small_ [[union]]s which are [[pullback stability|stable under pullback]].

More generally, for $\kappa$ a [[regular cardinal]], a _$\kappa$-geometric category_, or _$\kappa$-coherent category_, is a [[regular category]] with unions for $\kappa$-small families of [[subobjects]], stable under pullback. (For $\kappa = \omega$ this reduces to the notion of _[[coherent category]]_, called a _pre-logos_ by Freyd--Scedrov.)

[Makkai-Reyes](#MakkaiReyes) call this a _$\kappa$-[[logical category]]_, while [Shulman](#Shulman) calls it a _$\kappa$-[[k-ary regular category|ary regular category]]_.  See also ([Butz-Johnstone, p. 12](#ButzJohnstone)).

## Properties

See [[familial regularity and exactness]] for a general description of the spectrum from regular categories through finitary and infinitary coherent categories.

### Well-poweredness

Frequently, geometric categories are additionally required to be [[well-powered category|well-powered]].  If a geometric category is well-powered, then its subobject posets are [[complete lattices]], hence also have all intersections.  Moreover, by the [[adjoint functor theorem]] for posets, it is a [[Heyting category]].

However, since [[geometric logic]] does not include [[implication]] or infinite [[conjunction]], this categorical structure should not necessarily be expected to exist in a category called "geometric" (and when they do exist, they are not preserved by [[geometric functors]]).  A requirement of well-poweredness is also inconsistent with the spectrum of [[familial regularity and exactness]].

Note, however, that if a geometric category has a small [[generating set]], then it is necessarily well-powered.  In particular, this applies to the [[syntactic category]] of any (small) [[geometric theory]], and also to any [[Grothendieck topos]].


## Related concepts

[[!include categories and logic - table]]


## References

Around lemma A1.4.18 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

* {#MakkaiReyes} [[Michael Makkai]], [[Gonzalo Reyes]], _First Order Categorical Logic_, Lecture Notes in Math. 611 (Springer-Verlag, 1977).


* {#ButzJohnstone} Casten Butz, [[Peter Johnstone]], _Classifying toposes for first order theories_, [[BRICS]] Report Series RS-97-20
 

* {#Shulman} [[Mike Shulman]], _Exact completions and small sheaves_, TAC 27(7), 2012 ([link](http://www.tac.mta.ca/tac/volumes/27/7/27-07abs.html)).
  

[[!redirects geometric category]]
[[!redirects geometric categories]]
[[!redirects infinitary coherent category]]
[[!redirects infinitary coherent categories]]
[[!redirects infinitary-coherent category]]
[[!redirects infinitary-coherent categories]]

[[!redirects logical category]]
[[!redirects logical categories]]
