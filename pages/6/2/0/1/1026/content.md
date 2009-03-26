A [[functor]] $F :  C \to D$ is **continuous** if it preserves all small ([[weighted limit|weighted]]) [[limit]]s that exist in $C$, i.e. if for 
every [[small category]] [[diagram]] $A : E \to C$ in $C$ there is an isomorphism

$$
  F(\lim A) \simeq \lim (F\circ A)
  \,.
$$


(... say more ...)

#Examples#

* The archetypical example is the [[Set]]-valued [[hom-functor]]: its continuity in both arguments is indeed equivalent to the very definition of [[limit]]: for 
$F : D^{op} \to C$ a diagram and $c \in C$, the covariant [[hom-functor]] $Hom_C(c,-) : C \to Set$ satisfies by definition of [[limit]]
$$
  Hom_C(c, \lim F)
  \simeq
  \lim Hom(c,F(-))
  \,.
$$
