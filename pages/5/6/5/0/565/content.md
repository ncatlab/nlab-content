#Idea#

A concrete category is a [[category]] that looks like a category of "sets with extra structure".

#Definition#

A __concrete category__ is a category $C$

* equipped with a [[faithful functor]]
$$
  U : C \to Set
$$
to the category [[Set]];

* such that $U$ is [[representable functor|representable]], $U \simeq C(c_0,-)$

## Remarks ##

* Sometimes (often?) the term "concrete category" is used without implying the second condition of representability. This second condition however is important for the statement of concrete [[duality|dualities]] induced by [[dual adjunction]]s.


#Examples#

* $C = Set$ itself with $c_0 = \{\bullet\}$ the singleton set;

* $C$ any category which has an object $c_0$ which is "free on one generator", i.e which is the image under a functor $F : Set \to C$ [[adjoint functor|left adjoint]] to $U$ of the singleton set. 
Then by definition of left adjoint and the above example, we have $C(F(\{\bullet\}),d) \simeq Set(\{\bullet\}, U(d)) \simeq U(d)$, naturally in $d$.
This abstract nonsense indicates the usual collection of examples of concrete categories: for instance [[monoid]]s, [[group]]s, [[ring]]s, [[algebra]]s, etc. (... many more examples...)

* Take $ C $ is the category of [[Banach space]]s with morphisms those (everywhere-defined) linear transformations with norm bounded (above) by $ 1 $ (so $ \| T v \| \leq \| v \| $ for all $ v $ in the source).  Then there are two versions of $ U $ that one may use: one where $ U ( V ) $ (for $ V $ a Banach space) consists of *every* vector in $ V $, and one where $ U ( V ) $ consists of those vectors bounded by $ 1 $ (so the closed unit ball in $ V $).  The first may seem more obvious at first, but only the second is representable (by a $ 1 $-dimensional Banach space).


[[!redirects concrete categories]]