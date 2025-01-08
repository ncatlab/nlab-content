## Idea

The abstract notion of a derivation corresponding to that of a [[Beck module]].

## Definition

Given a category $C$ with finite limits, a [[Beck module]] in $C$ over an object $A\in C$ is an abelian group object in the [[slice category]] $C/A$.

The forgetful functor from modules to rings is modeled by the forgetful functor
$$U_A\colon Ab(C/A)\to C/A.$$

Given $M\in Ab(C/A)$, a __Beck derivation__ $A\to M$ is a a morphism $id_A \to U_A(M)$ in $C/A$.

If $U_A$ has a [[left adjoint]] $\Omega_A$, then $\Omega_A$ is known as the __Beck module of differentials__ over $A$.
Thus, Beck derivations $A\to M$ are in bijection with morphisms of Beck modules
$$\Omega_A\to M,$$
generalizing the universal property of [[Kähler differentials]].

## Examples

For ordinary [[commutative algebras]], Beck derivations coincide with ordinary [[derivations]].

For [[C^∞-rings]], Beck derivations coincide with [[C^∞-derivations]].

## References

The original definition is due to [[Jon Beck]].
An exposition can be found in Section 6.1 of

* [[Michael Barr]], Acyclic models,  CRM Monograph Series 17 (2002), [PDF](https://www.math.mcgill.ca/barr/papers/acmod.pdf).