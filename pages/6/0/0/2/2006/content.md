
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




# Kleisli category
* table of contents
{: toc}

## Idea

The __Kleisli category__ of a [[monad]] is the category of its free [[algebra for a monad|modules]]; compare the [[Eilenberg–Moore category]].


## Definitions

Given a [[monad]] $\mathbf{T}=(T,\mu,\eta)$ in [[Cat]], where $T:C\to C$ is an endofunctor with multiplication $\mu:T T\to T$ and unit $\eta:Id_C\to T$, a __free $\mathbf{T}$-[[module]]__ (or free $\mathbf{T}$-algebra) is a $\mathbf{T}$-module (algebra) of the form $(T(M),\mu_M)$, where the [[action]] is the component of multiplication transformation $\mu_M : T(T(M))\to T(M)$. The category of free $\mathbf{T}$-algebras is a [[subcategory]] of the [[Eilenberg–Moore category]] $C^{\mathbf{T}}$ called the __Kleisli category__ $C_{\mathbf{T}}$ of the monad $\mathbf{T}$. If $U:C^{\mathbf{T}}\to C$ is the [[forgetful functor]] and $F: C\to C^{\mathbf{T}}$ is the [[free functor|free algebra functor]] $F: M\mapsto (T M,\mu_M)$, then the Kleisli category is simply the full subcategory of $C^{\mathbf{T}}$ containing those objects in the image of $F$.


## Remarks

As another way of looking at this, we can keep the same objects as in $C$ but redefine the morphisms. This was the original Kleisli construction: the objects of $C_{\mathbf{T}}$ are simply the objects of $C$ and the morphisms $M\to N$ in $C_{\mathbf{T}}$ are the elements of $C(M,T(N))$
with the composition rule $g\circ_{Kleisli} f = \mu_P\circ T(g)\circ f$ like in the [[Grothendieck construction]] (here $M\stackrel{f}\to N\stackrel{g}\to P$).

In more general 2-categories the universal properties of [[Kleisli object]]s are dual to the universal properties of [[Eilenberg–Moore object]]s.


[[!redirects Kleisli category]]
[[!redirects Kleisli categories]]
