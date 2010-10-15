
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _concrete category_' is a [[category]] that looks like a category of "[[set]]s with extra [[stuff, structure, property|structure]]".


## Definition

A __concrete category__ is a category $C$

* equipped with a [[faithful functor]]

$$
  U : C \to Set
$$

to the category [[Set]];

* such that $U$ is [[representable functor|representable]], $U \simeq C(c_0,-)$

The object $c_0$ is called a [[generator]] of the category.


+-- {: .un_remark}
###### Remark
Sometimes (often?) the term "concrete category" is used without implying the second condition of representability. This second condition however is important for the statement of concrete [[duality|dualities]] induced by [[dual adjunction]]s.
=--


## Examples

* $C = Set$ itself with $c_0 = \{\bullet\}$ the singleton set;

* $C$ any category which has an object $c_0$ which is "free on one generator", i.e which is the image under a functor $F : Set \to C$ [[adjoint functor|left adjoint]] to $U$ of the singleton set. 
Then by definition of left adjoint and the above example, we have $C(F(\{\bullet\}),d) \simeq Set(\{\bullet\}, U(d)) \simeq U(d)$, naturally in $d$.
This abstract nonsense indicates the usual collection of examples of concrete categories: for instance [[monoid]]s, [[group]]s, [[ring]]s, [[algebra]]s, etc. (... many more examples...)

* Take $ C $ is the category of [[Banach space]]s with morphisms those (everywhere-defined) linear transformations with norm bounded (above) by $ 1 $ (so $ \| T v \| \leq \| v \| $ for all $ v $ in the source).  Then there are two versions of $ U $ that one may use: one where $ U ( V ) $ (for $ V $ a Banach space) consists of *every* vector in $ V $, and one where $ U ( V ) $ consists of those vectors bounded by $ 1 $ (so the closed unit ball in $ V $).  The first may seem more obvious at first, but only the second is representable (by a $ 1 $-dimensional Banach space).

* A concrete category that is equipped with the structure of a [[site]] in a compatible way is a [[concrete site]].


## Generalisations

One can consider concrete categories over any base category $X$ instead of necessarily over $Set$.  This is the approach taken in _[[The Joy of Cats]]_.  Then the (small) concrete categories over $X$ form a [[2-category]] $Cat(X)$.


[[!redirects concrete category]]
[[!redirects concrete categories]]
[[!redirects CAT(X)]]
[[!redirects Cat(X)]]
