A **cocartesian closed category** is a [[cocartesian monoidal category]] which is a [[closed monoidal category]].  The notion is not very interesting, however, because of the following:

+--{: .un_theorem}
###### Theorem
Any cocartesian closed category is equivalent to the [[terminal category]].
=--
+--{: .proof}
###### Proof
Let $C$ be cocartesian closed.  Since it has an initial object, it is inhabited; thus it suffices to show that between any two objects there is a unique morphism.  But in any closed monoidal category, for any objects $x$ and $y$ the set $C(x,y)$ is in bijection with $C(I,[x,y])$ where $I$ is the unit object and $[-,-]$ the [[internal-hom]].  But since $I$ is an initial object, $C(I,[x,y])$ is a [[singleton]], hence so is $C(x,y)$.
=--

Note that the proof actually applies to any *semi*-cocartesian closed monoidal category, i.e. any closed monoidal category whose unit is an initial object.

## See also

* [[cartesian closed category]]

* [[cocartesian coclosed category]]