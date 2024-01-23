
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

Given a [[monad]] $t \colon a \to a$ in a [[2-category]] $K$, the **Kleisli object** $a_t$ of $t$ is, if it exists, the [[universal property|universal]] right $t$-[[module over a monad|module]] or $t$-opalgebra.  Equivalently, $a_t$ [[representable functor|represents]] the [[functor]] $RMod(-,t)$ that takes an object $x$ of $K$ to the category of right $t$-modules $a \to x$.

This means that there is a "free" [[1-morphism]] $f_t \colon a \to a_t$ and a [[2-morphism]] $\alpha \colon f_t t \Rightarrow f_t$ that induce an [[isomorphism]] $K(a_t,x) \cong RMod(x,t)$: given a right $t$-module $r \colon a \to x, \rho \colon r t \to r$, there is a unique morphism $h \colon a_t \to x$ whose [[composition|composite]] with $f_t$ (respectively $\alpha$) is equal to $r$ (resp. $\rho$).
\begin{center}
\begin{tikzcd}
a 
\arrow[rrr, "r", bend left=60, "" {name=A, xshift=-6.5ex, below} ]
\arrow[rr, "f_t"', bend right=80, "" {name=B, above} ]
\arrow[r, "t"']
&a 
\arrow[Rightarrow, "\alpha", shorten >= 0.8ex, shorten <=0.4ex,  to=B]
\arrow[Rightarrow, "\rho", shorten >= 1ex, shorten <=0.4ex,  to=A]
\arrow[rr, "r", bend left ]
\arrow[r, "f_t"']
&a_t
\arrow[r, dashed, "h"']
& x
\end{tikzcd}
\end{center}

## Examples

\begin{example}
The motivating example is that of ordinary [[Kleisli categories]] $C_T$ for monads in the [[2-category]] [[Cat]], hence for ordinary monadic [[endofunctors]] $T$ on [[categories]] $C$.
\end{example}


\begin{example}
In a ([[locally ordered]]) [[bicategory of relations]], the Kleisli object of a monad $t$ is part of a [[splitting]] of $t$ as an [[idempotent]].
\end{example}

\begin{example}
For a monad $T \colon A &#8696; A$ in the bicategory [[Prof]] of [[profunctors]], its Kleisli object consists of a category $A_T$ equipped with a [[bijective-on-objects functor]] $A\to A_T$.  The category $A_T$ has the same objects as $A$, with [[hom-sets]] $A_T(a,b) = T(a,b)$.  Identities and composition are given by the [[monad unit]] and multiplication of $T$.

  Every functor $B \to A$ yields a monad $A(f,f)$ in $Prof$, whose Kleisli object is part of the (bijective on objects, fully-faithful) factorization $B \to A_{A(f,f)} \to A$ of $f$.

  Because of this, we can identify a monad on $A$ in $Prof$ with a bijective-on-objects functor $A \to B$.
\end{example}

## Properties

\begin{remark}
By 2-category theoretic [[formal duality]] (see at *[[opposite 2-category]]*):

1. Kleisli objects in a 2-category $K$ are equivalently [[Eilenberg-Moore objects]] in  $K^{op}$.  

1. Kleisli objects for monads in $K^{co}$ are equivalently Kleisli objects for [[comonads]] in $K$.

\end{remark}

\begin{remark}
Kleisli objects for a monad $t$ in $K$ are equivalently a particular sort of [[weighted limit|weighted]] [[2-colimits]], namely the [[lax colimits]] of the [[lax functor]] $\ast \to K$ corresponding to $t$.
\end{remark}

## Related concepts

* [[Eilenberg-Moore object]]

## References

An original article is

* {#Street72} [[Ross Street]], *The formal theory of monads*, Journal of Pure and Applied Algebra **2** 2 (1972) 149-168 &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90019-9">doi:10.1016/0022-4049(72)90019-9</a>&rbrack;

Generalization from [[monads]] to more general [[categories enriched in a bicategory]] (where "Kleisli objects" are then called "collages") is in 

* {#GarnerShulman13} [[Richard Garner]], [[Michael Shulman]], *Enriched categories as a free cocompletion*, 
Advances in Mathematics **289** (2016) 1-94
&lbrack;[arXiv:1301.3191](http://arxiv.org/abs/1301.3191), [doi:10.1016/j.aim.2015.11.012](https://doi.org/10.1016/j.aim.2015.11.012)&rbrack;
 

[[!redirects Kleisli objects]]