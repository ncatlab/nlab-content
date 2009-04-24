A **Boolean topos** is a [[topos]] that is also a [[Boolean category]].

There are several conditions on a topos that are necessary and sufficient to be boolean:
* Every [[subobject]] has a complement (the general definition of boolean category).
* Every [[subobject lattice]] is a [[Boolean algebra]].
* The [[subobject classifier]] $\Omega$ is an [[internalization|internal]] Boolean algebra.
* The maps $\top, \bot: 1 \to \Omega$ are a [[coproduct]] cone (so in particular, $\Omega \cong 1 + 1$, but this alone is not sufficient).

The [[internal logic]] of a boolean topos can serve as [[foundations]] for "ordinary" mathematics, except for that which relies on the [[axiom of choice]].

Every [[locally cartesian closed category|locally cartesian closed]] boolean [[pretopos]] (in fact, every [[cartesian closed category|cartesian closed]] pretopos) is in fact a topos.  This is why [[predicative mathematics|predicativism]] (in the constructive sense) is necessarily a feature of [[constructive mathematics]] only.

+--{: .query}
[[Mike Shulman|Mike]]: Something sounds circular about saying "predicativism in the constructive sense is a feature of constructive mathematics only."  What non-constructive sense of predicativism are you referring to?
=--
