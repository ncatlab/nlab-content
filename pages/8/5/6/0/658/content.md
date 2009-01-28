Let $V$ be a symmetric [[closed monoidal category]] and $C$, $C$, [[enriched category|enriched categories]] over $V$. Then a _distributor_ or _profunctor_ or _[[bimodule|(bi)module]]_ from $C$ to $D$ is a $V$-functor

$$
  F : C \stackrel{|}{\to} D : C^{op}\otimes D \to V
  \,.
$$

Such distributors are composed by using a [[end|coend]] to "trace out" the middle variable:

for $F : C \stackrel{|}{\to} D$ and $G : D \stackrel{|}{\to} E$ distributors, their composite  $G \circ F: C \stackrel{|}{\to} E$ is defined to be

$$
  G \circ F := \int^{d \in D} F(-,d)\otimes G(d,-)
  \,.
$$

This yields a [[bicategory]] $V-Mod$ with

* objects are $V$-enriched categories;

* morphisms are distributors with the above compositio;

* 2-morphisms are natural transformations.

#Related entries#

* [[module]]

* [[2-vector space]]

#References#

_(what is a good  comprehensive reference?)_