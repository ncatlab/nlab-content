
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

Given a [[monad]] $t \colon a \to a$ in a [[2-category]] $K$, the **Kleisli object** $a_t$ of $t$ is, if it exists, the [[universal property|universal]] right $t$-[[module over a monad|module]] or $t$-opalgebra.  Equivalently, $a_t$ [[representable functor|represents]] the functor $RMod(-,t)$ that takes an object $x$ of $K$ to the category of right $t$-modules $a \to x$.

This means that there is a morphism $f_t \colon a \to a_t$ and a 2-cell $\lambda \colon f_t t \Rightarrow f_t$ that induce an [[isomorphism]] $K(a_t,x) \cong RMod(x,t)$: given a right $t$-module $r \colon a \to x, \alpha \colon r t \to r$, there is a unique morphism $a_t \to x$ whose composite with $f_t$ (repsectively $\lambda$) is equal to $r$ (resp. $\alpha$).

## Examples

* The motivating example is that of [[Kleisli categories]] for monads in [[Cat]].

* In a ([[locally ordered]]) [[bicategory of relations]], the Kleisli object of a monad $t$ is part of a [[splitting]] of $t$ as an [[idempotent]].

* For a monad $T \colon A &#8696; A$ in the bicategory [[Prof]] of [[profunctors]], its Kleisli object consists of a category $A_T$ equipped with a [[bijective-on-objects functor]] $A\to A_T$.  The category $A_T$ has the same objects as $A$, with hom-sets $A_T(a,b) = T(a,b)$.  Identities and composition are given by the unit and multiplication of $T$.

  Every functor $B \to A$ yields a monad $A(f,f)$ in $Prof$, whose Kleisli object is part of the (bijective on objects, fully-faithful) factorization $B \to A_{A(f,f)} \to A$ of $f$.

  Because of this, we can identify a monad on $A$ in $Prof$ with a bijective-on-objects functor $A \to B$.

## Remarks

* A Kleisli object in a 2-category $K$ is the same as an [[Eilenberg-Moore object]] in $K^{op}$; see [[opposite 2-category]].  Kleisli objects for monads in $K^{co}$ can be identified with Kleisli objects for [[comonads]] in $K$.

* A Kleisli object for a monad $t$ in $K$ can equivalently be defined as a particular sort of [[weighted limit|weighted]] [[2-colimit]], namely the [[lax colimit]] of the [[lax functor]] $\ast \to K$ corresponding to $t$.

## References

* [[R. Street]], _The formal theory of monads_, J. Pure Appl. Alg. __2__, 149&#8211;168 (1972)

[[!redirects Kleisli objects]]
