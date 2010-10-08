## Definition

Given a [[monad]] $t \colon a \to a$ in a [[2-category]] $K$, the **Kleisli object** $a_t$ of $t$ is, if it exists, the [[universal property|universal]] right $t$-[[module over a monad|module]] or $t$-opalgebra.  Equivalently, $a_t$ [[representable functor|represents]] the functor $RMod(-,t)$ that takes an object $x$ of $K$ to the category of right $t$-modules $a \to x$.

This means that there is a morphism $f_t \colon a \to a_t$ and a 2-cell $\lambda \colon f_t t \Rightarrow f_t$ that induce an [[isomorphism]] $K(a_t,x) \cong RMod(x,t)$: given a right $t$-module $r \colon a \to x, \alpha \colon r t \to r$, there is a unique morphism $a_t \to x$ whose composite with $f_t$ (repsectively $\lambda$) is equal to $r$ (resp. $\alpha$).

## Examples

* The motivating example is that of [[Kleisli categories]] for monads in [[Cat]].

* In a ([[locally ordered]]) [[bicategory of relations]], the Kleisli object of a monad $t$ is part of a [[splitting]] of $t$ as an [[idempotent]].

* In the bicategory [[Prof]] of [[profunctors]], a monad on a category $A$ consists of a category $B$ equipped with a [[bijective-on-objects functor]] $A\to B$.  Its Kleisli object in $Prof$ is simply the category $B$.

## Remarks

* A Kleisli object in a 2-category $K$ is the same as an [[Eilenberg-Moore object]] in $K^{op}$; see [[opposite 2-category]].  Kleisli objects for monads in $K^{co}$ can be identified with Kleisli objects for [[comonads]] in $K$.

* A Kleisli object can equivalently be defined as a particular sort of [[weighted limit|weighted]] [[2-colimit]].

## References

* [[R. Street]], _The formal theory of monads_, J. Pure Appl. Alg. __2__, 149&#8211;168 (1972)

[[!redirects Kleisli objects]]
