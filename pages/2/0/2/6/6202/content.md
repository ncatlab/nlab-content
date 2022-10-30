## Definition

Let $C$ and $D$ be [[monoidal categories]], and $F\colon C \leftrightarrows D : G$ a *comonoidal adjunction, i.e. an [[adjunction]] in the [[2-category]] of colax [[monoidal functors]].  (By [[doctrinal adjunction]], this implies that $G$ is a strong monoidal functor.)  This adjunction is a **Hopf adjunction** if the canonical morphisms

$$ F(x \otimes G y) \to F x \otimes y $$
$$ F(G y \otimes x) \to y \otimes F x $$

are isomorphisms for any $x\in C$ and $y\in D$.

Of course, if $C$, $D$, $F$, and $G$ are [[symmetric monoidal category|symmetric]], then it suffices to ask for one of these.  If $C$ and $D$ are moreover [[cartesian monoidal category|cartesian monoidal]], then any adjunction is comonoidal, and the condition is also (mis?)named [[Frobenius reciprocity]].

## Properties

* If $C$ and $D$ are closed, then by the calculus of [[mates]], saying that $F\dashv G$ is Hopf is equivalent to asking that $G$ be a [[closed monoidal functor]], i.e. preserve [[internal-homs]] up to isomorphism.

* If $F\dashv G$ is a Hopf adjunction, then its induced monad $G F$ is a [[Hopf monad]].  Conversely, the [[Eilenberg-Moore category|Eilenberg-Moore]] adjunction of a Hopf monad is a Hopf adjunction.

## References

* Alain Brugui&#232;resa, [[Steve Lack]], and Alexis Vireliziera, _Hopf monads on monoidal categories_.  Adv. Math. 227 No. 2, June 2011, pp 745--800.
