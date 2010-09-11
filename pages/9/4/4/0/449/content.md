+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[geometric definition of higher categories]]

* **algebraic definition of higher categories**

***

# Contents
* automatic table of contents goes here
{:toc}

## Idea 

In an _algebraic definition_ of [[(n,r)-categories]] [[composition]] of [[higher morphism]]s is a genuine algebraic operation. As opposed to a _geometric model_ where composites are only guaranteed to exist, in an algebraic model there is prescription for finding these composites.

These choice may be given in an elementary way as binary composition operations as in an ordinary [[category]], or the composition operation may be controled by sophisticated algebraic structures such as [[operad]]s that, while keeping track of all specified composites, may allow large of possible composition operations.

The composition operation in an algebraic model for an $(n,r)$-category are subject to [[associativity]]  [[coherence law]]s. On the geometric size these reflect the fact that the spaces of possible choices of composites are contractible.

Typically an algebraic model for higher categories admits a [[nerve]] operation that turns it into an equivalent geometric model. Conversely, typically one can obtain an algebraic model form a geometric model by making _choices_ of composites.


## Examples 

* The series of notions

  * [[category]], [[groupoid]]

  * [[bicategory]]

  * [[tricategory]]

  * [[tetracategory]]

  are algebraic models for [[n-categories]] with $1 \leq n \leq 4$ given in terms of direct explicit operations: no [[operad]]s or other tools are used but all the possible compossition operations are defined elementarily and all the relevant [[coherence law]]s are demanded explcitly. This makes these models very concrete and hands-on. But it also has the disadvantage that beginning with tricategories these definitions become quite unwieldy.

* For [[strict n-categories]] all subtleties with [[associator]]s and [[coherence law]]s are absent (by definition) and therefore there are straightforward algebraic models for these See [[strict omega-category]], [[strict omega-groupoid]] and [[n-fold category]]. The drawback is of course that these strict models capture only a very restricted part of higher category theory.

* The [[Michael Batanin|Batanin]]/[[Tom Leinster|Leinster]] approach to higher categories involves algebraic structure imposed all at once (using higher [[operad|operads]]) on a globular set. See [[Batanin omega-category]].

* The [[Todd Trimble|Trimble]]/[[Peter May|May]] approach to higher categories involves algebraic structure imposed in stages by a process of iterative enrichment. See also [[Trimble n-category]].  

* Using the tool of [[model structure on algebraic fibrant objects]] many geometric models for higher categories may be realized equivalently as algebraic models. This is notably true for [[∞-groupoid]]s and [[(∞,1)-categories]]. See [Algebraic  fibrant models for higher categories](http://ncatlab.org/nlab/show/model+structure+on+algebraic+fibrant+objects#AlgebaicHigherCategories).

## Properties

When an [[(∞,1)-category]] of [[(n,r)-categories]] is presented by a [[model category]], then algebraic models tend to be fibrant objects (while geometric models tend to be cofibrant objects). For instance in all the [[folk model structure]] on algebraic higher categories and groupoids, all objects are fibrant.


[[!redirects algebraic definition of higher categories]]
[[!redirects algebraic definition of higher category]]
[[!redirects algebraic model of higher categories]]
[[!redirects algebraic model of higher category]]
