
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
* automatic table of contents goes here
{:toc}

## Idea

The Eilenberg--Moore category of a [[monad]] is the category of its [[algebra for a monad|modules]] (aka algebras).

The category of its [[free functor|free]] modules is called the [[Kleisli category]].

## Definitions

Given a [[monad]] $\mathbf{T}=(T,\mu,\eta)$ in [[Cat]], where $T:C\to C$ is an endofunctor with multiplication $\mu:T T\to T$ and unit $\eta:Id_C\to T$, a $\mathbf{T}$-[[algebra for a monad|module]] (or $\mathbf{T}$-algebra) in $C$ is a pair $(M,\nu)$ of an object $M\in C$ and a morphism $\nu:T(M)\to M$ which is a __$T$-[[action]]__, namely $\nu\circ T(\nu)=\nu\circ\mu_{M} :T(T(M))\to M$ and $\nu\circ\eta_M = id_M$. 
A morphism of $\mathbf{T}$-modules $f:(M,\nu^M)\to (N,\nu^N)$ is a morphism $f:M\to N$ in $C$ such that it commutes with the action: $f\circ\nu^M=\nu^N\circ T(f):T(M)\to N$. The composition of morphisms of $\mathbf{T}$-modules is the composition of underlying morphisms in $C$.

$\mathbf{T}$-modules and their morphisms form a [[category]] $C^{\mathbf{T}}$ which is called the __Eilenberg--Moore category__ of the monad $\mathbf{T}$.  This may also be written $Alg(T)$, $T\,Alg$, etc.


## Remarks

Eilenberg-Moore category satisfies a 2-categorical universal property, formulated in

* [[Ross Street]], _Formal theory of monads_, JPAA 1972 

In that article, monads a general (strict but only for simplicity) [[2-category]] $K$ were considered, and the corresponding Eilenberg-Moore universal property defining __Eilenberg--Moore objects__ in $K$ were formulated. Not every 2-category admits Eilenberg--Moore objects. 

S. Lack has shown how the Eilenberg-Moore objects $C^{\mathbf{T}}$ can be obtained as combinations of certain simpler lax limits, when the 2-category $K$ in question is the 2-category of 2-algebras over a 2-monad $\mathbf{G}$ and lax, colax or pseudo morphisms of such: 

* [[Steve Lack]], _Limits for lax morphisms_ , Applied Categorical Structures __13__:3 (2005) , pp. 189--203(15) 

This encompasses for example the theory of (op)monoidal monads and corresonding monoidal Eilenberg--Moore categories.


[[!redirects Eilenberg–Moore category]]
[[!redirects Eilenberg--Moore category]]
[[!redirects Eilenberg-Moore object]]
[[!redirects Eilenberg–Moore object]]
[[!redirects Eilenberg--Moore object]]
[[!redirects Alg(T)]]
[[!redirects T-Alg]]
[[!redirects T-alg]]
[[!redirects T Alg]]
[[!redirects T alg]]
