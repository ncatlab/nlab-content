#Idea#

For $X$ and $Y$ [[topological space]]s, a continuous map $X \to Y$ induces (in particular) two [[functor]]s

$$
  f^* : Sh(Y) \to Sh(X)
$$
$$
  f_* : Sh(X) \to Sh(Y)
$$
between the corresponding  [[Grothendieck topos|Grothendieck topoi]] of [[sheaf|sheaves]] on $X$ and $Y$, such that

* $f^*$ is [[adjoint functor|left adjoint]] to $f_*$

* $f^*$ is [[exact functor|left exact]] in that it preserves finite [[limit]]s.

Morever, if $X$ and $Y$ are 
[[sober space|sober]] [[topological space]]s
every pair of functors with these properties comes uniquely from a continuous map $X \to Y$.

A _geometric morphism_ between arbitrary [[topos|topoi]] is the direct generalization of this situation.

Another motivation of the concept comes from the the fact that a [[functor]] such as $f^*$ that preserves finite [[limit]]s and arbitrary [[colimit]]s (since it is a [[left adjoint]]) necessarily preserves all constructions in [[geometric logic]].  See also [[classifying topos]].



#Definition#

If $E$ and $F$ are [[topos|toposes]], a **geometric morphism** $f:E\to F$ consists of an pair of [[adjoint functor]]s $(f^*,f_*)$
$$
  f_* : F \to E
$$
$$
  f_* : E \to F
  \,,
$$

such that the left adjoint $f^*:F \to E$ preserves finite [[limit]]s.



#Remarks#

* Since [[Grothendieck topos]]es satisfy the (dual) hypotheses of Freyd's special [[adjoint functor theorem]], any functor $f^*$ between Grothendieck toposes which preserves all small colimits must have a right adjoint.  Therefore, a geometric morphism between Grothendieck toposes could equivalently be defined as a functor preserving finite limits and all small colimits.


#Surjections and embeddings#

A geometric morphism $f : E \to F$ is a **surjection** if $f^*$ is [[faithful functor|faithful]].

It is an **embedding** if $f_*$ is [[full and faithful functor|fully faithful]].

**Proposition**

Up to equivalence, every embedding of topoi is of the form 

$$
  Sh_j(E) \to E
  \,,
$$

where $Sh_j(E)$ is the topos of [[sheaf|sheaves]] with respect to a [[Lawvere-Tierney topology]] $j : \Omega \to \Omega$ on $E$.

This means in particular that fully faithful geometric morphisms into [[Grothendieck topos|Grothendieck topoi]] are an equivalent way of encoding a [[Grothendieck topology]]. 


#References#

Geoemtric morphisms are the topic of section VII of

* MacLan-Moerdijk, [[Sheaves in Geometry and Logic]].

Embeddings and surjections are discussed in section VII.4.