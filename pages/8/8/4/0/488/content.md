A **Boolean topos** is a [[topos]] that is also a [[Boolean category]].

There are several conditions on a topos that are necessary and sufficient to be boolean:
* Every [[subobject]] has a complement (the general definition of boolean category).
* Every [[subobject poset|subobject lattice]] is a [[Boolean algebra]].
* The [[subobject classifier]] $\Omega$ is an [[internalization|internal]] Boolean algebra.
* The maps $\top, \bot: 1 \to \Omega$ are a [[coproduct]] cone (so in particular, $\Omega \cong 1 + 1$, but this alone is not sufficient).

The [[internal logic]] of a boolean topos with [[natural numbers object]] can serve as [[foundations]] for "ordinary" mathematics, except for that which relies on the [[axiom of choice]].  If you add the axiom of choice, then you get (an internal version of) [[ETCS]]; conversely, if you use an arbitrary topos, then you get [[constructive mathematics]].  (For some high-powered work, you may also need to add a version of the [[axiom of replacement]] or an axiom of [[Grothendieck universe]]s.)

Every [[cartesian closed category|cartesian closed]] boolean [[pretopos]] is in fact a topos.  This is why [[predicative mathematics|predicativism]] (in our sense) is necessarily a feature of [[constructive mathematics]] only.

+--{: .query}
[[Mike Shulman|Mike]]: Something sounds circular about saying "predicativism in the constructive sense is a feature of constructive mathematics only."  What non-constructive sense of predicativism are you referring to?

_Toby_:  I just mean that the term is used in other senses.  Compare the 'classical predicativism' at [PlanetMath's article](http://planetmath.org/encyclopedia/Predicativism.html) or the (somewhat related) [discussion](http://plato.stanford.edu/entries/philosophy-mathematics/#Pre) in the Stanford Encyclopedia.
=--
