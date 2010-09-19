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

On the other hand, there are many co-cartesian *[[coclosed monoidal category|co-closed]]* categories, namely the [[opposite category]] of any [[cartesian closed category]]. Any category which is both cartesian closed and co-cartesian co-closed is a preorder, though it may not be the terminal category (e.g., any Boolean algebra is such a category).
+--{: .proof}
###### Proof
Let a category be given which is both cartesian closed and co-(cartesian closed). Cartesian closure tells us that the product of any object with the initial object $0$ will be itself initial (as left adjoints preserve colimits). Furthermore, given any morphism from an object $A$ to $0$, we can pair this with the identity function on $A$ to obtain a morphism from $A$ into $A \times 0$ with a left inverse given by projection, thus identifying $A$ as a retract of an initial object, and therefore as an initial object itself. It follows immediately that any two parallel maps to $0$ are equal; equivalently, by the dual reasoning, any two parallel maps out of $1$ are equal. But this means any two parallel maps in general are equal, as maps from $X$ to $Y$ can be identified with maps from $1$ to $Y^X$; accordingly, the category must be a preorder.
=--