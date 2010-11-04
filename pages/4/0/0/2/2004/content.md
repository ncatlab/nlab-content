
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

Let $(T,\eta,\mu)$ be a [[monad]] in [[Cat]], where $T \colon C\to C$ is an endofunctor with multiplication $\mu \colon T T\to T$ and unit $\eta \colon Id_C\to T$.  Recall that a (left) $T$-[[algebra for a monad|module]] (or $T$-algebra) in $C$ is a pair $(M,\nu)$ of an object $M$ in $C$ and a morphism $\nu\colon T(M)\to M$ which is a __$T$-[[action]]__, namely $\nu\circ T(\nu)=\nu\circ\mu_{M} \colon T(T(M))\to M$ and $\nu\circ\eta_M = id_M$, and that a morphism of $T$-modules $f\colon (M,\nu^M)\to (N,\nu^N)$ is a morphism $f\colon M\to N$ in $C$ that commutes with the action: $f\circ\nu^M=\nu^N\circ T(f)\colon T(M)\to N$. The composition of morphisms of $T$-modules is the composition of underlying morphisms in $C$.

$T$-modules and their morphisms thus form a [[category]] $C^T$ which is called the __Eilenberg--Moore category__ of the monad $T$.  This may also be written $Alg(T)$, $T\,Alg$, etc.  It comes equipped with a forgetful functor $U^T \colon C^T \to C$ which is the [[universal property|universal]] $T$-module, and has a [[left adjoint]] $F^T$ such that the monad $U^T F^T$ arising from the adjunction is equal to $T$

In general, if $t \colon a \to a$ is a monad in a [[2-category]] $K$, then the __Eilenberg--Moore object__ $a^t$ of $t$ is, if it exists, the universal (left) $t$-module.  That is, there is a morphism $u^t \colon a^t \to t$ and a 2-cell $t u^t \Rightarrow u^t$ that mediate a natural isomorphism $K(x, a^t) \cong LMod(x,t)$ between morphisms $x \to a^t$ and $t$-modules $(m \colon x \to a, \lambda \colon t m \Rightarrow m)$.  Not every 2-category admits Eilenberg--Moore objects.


## Universal properties

Apart from being the universal left $T$-module, the EM category of a monad $T$ in $Cat$ has some other interesting properties.

There is a [[full subcategory]] $RAdj(C)$ of the [[slice category]] $Cat/C$ on the functors $X \to C$ that have left adjoints.  For any monad $T$ on $C$ there is a full subcategory of this consisting of the adjoint pairs that compose to give $T$.  The functor $U^T \colon C^T \to C$ is the [[terminal object]] of this category.

If $C_T$ is the [[Kleisli category]] of $T$ and $F_T \colon C \to C_T$ the canonical functor, then the EM category $C^T$ can be constructed as the [[pullback]]
$$
\array{
  C^T & \to & [C_T^{op}, Set] \\
  \downarrow & & \downarrow \mathrlap{[F_T^{op},Set]} \\
  C & \underset{Y}{\to} & [C^{op}, Set]
}
$$
Thus a $T$-algebra may be regarded as a [[presheaf]] on the Kleisli category of $T$ whose restriction to $C$ is [[representable]].  This observation seems to be due to Linton.  Street--Walters show that it holds in any 2-category equipped with a [[Yoneda structure]].

Just as the [[Kleisli object]] of a monad $t$ in a 2-category $K$ can be defined as the [[lax colimit]] of the [[lax functor]] $\ast \to K$ [[monad|corresponding]] to $t$, the EM object of $t$ is its [[lax limit]].


## Remarks

S. Lack has shown how Eilenberg-Moore objects $C^T$ can be obtained as combinations of certain simpler lax limits, when the 2-category $K$ in question is the 2-category of 2-algebras over a 2-monad $\mathbf{G}$ and lax, colax or pseudo morphisms of such: 

* [[Steve Lack]], _Limits for lax morphisms_ , Applied Categorical Structures __13__:3 (2005) , pp. 189--203(15) 

This encompasses for example the theory of (op)monoidal monads and corresonding monoidal Eilenberg--Moore categories.

The paper of Melli&#232;s referenced below compares the Linton representability condition above with the [[Segal condition]] that distinguishes those [[simplicial sets]] that are the [[nerves]] of categories.

## References

* [[Ross Street]], _The formal theory of monads_, JPAA 2, 1972 
* [[Fred Linton]], _An outline of functorial semantics_, LNM 80, 1969
* [[Ross Street]] and [[Bob Walters]], _Yoneda structures_, J. Algebra 50, 1978
* [[Paul-André Melliès]], _Segal condition meets computational effects_, LICS 2010

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
