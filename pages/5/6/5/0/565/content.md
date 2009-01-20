#Idea#

A _concrete category_ is a category that looks like a category of "sets with extra structure".

#Definition#

A _concrete category_ is a category $C$

* equipped with a [[faithful]] functor 
$$
  U : C \to Set
$$
to the category [[Set]];

* such that $U$ is [[representable]], $U \simeq C(c_0,-)$

## Remarks ##

* Sometimes (often?) the term "concrete category" is used without implying the second condition of representability. This second condition however is important for the statment of concrete [[duality|dualities]] induced by [[dual adjunction]]s.


#Examples#

* $C = Set$ itself with $c_0 = \{\bullet\}$ the singleton set;

* $C$ any category which has an object $c_0$ which is "free on one generator", i.e which is the image under a functor $F : Set \to C$ [[left adjoint]] to $U$ of the singleton set. 
Then by definition of [[left adjoint]] and the above example, we have $C(F(\{\bullet\}),d) \simeq Set(\{\bullet\}, U(d)) \simeq U(d)$, naturally in $d$.
This abstract nonsense indicates the usual collection of examples of concrete categories: for instance [[monoid]]s, [[group]]s, [[ring]]s, [[algebra]]s, etc. (... many more examples...)