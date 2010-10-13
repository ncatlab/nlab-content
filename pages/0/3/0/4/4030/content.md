
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc} 

## Idea

A [[topos]] may be thought of as a generalized [[topological space]]. Accordingly, the notions of 

* [[locally connected space]]

* locally 2-[[connected]] space

* etc. ...

* [[locally contractible space]]

have analogs for [[topos]]es and [[(∞,1)-topos]]es

* **locally connected topos**

* [[locally n-connected (n,1)-topos]] 

* etc. ...

## Locally connected topos

Let $E$ be a [[topos]]. An object $A \in E$ is called a [[connected object]] if $\hom_E(A, -)$ preserves finite [[coproduct]]s. Equivalently, an object $A$ is connected if it is nonempty (non[[initial object|initial]]) and cannot be expressed as a coproduct of two nonempty [[subobject]]s. 

### Definition

A [[Grothendieck topos]] $E$ is called a **locally connected topos** is every object $A \in E$ is a [[coproduct]] of connected objects $\{A_i\}_{i \in I}$, $A = \coprod_{i \in I} A_i$.  It follows that the index set $I$ is unique up to isomorphism, and we write

$$
  \pi_0(A) = I
  \,.
$$

This construction defines a functor $\Pi_0 : E \to Set : A \mapsto \pi_0(A)$ which is [[left adjoint]] to the [[constant sheaf]] functor, the [[left adjoint]] part of the [[global section]] [[geometric morphism]].  Thus, for a locally connected topos we have

$$
  (\Pi_0 \dashv LConst \dashv \Gamma) : 
  E \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{Const}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
  \,.
$$

This left adjoint $\Pi_0$ is the lowest degree incarnation of a general construction of [[homotopy groups in an (∞,1)-topos]].

+-- {: .un_prop}
###### Proposition

A topos $E$ is locally connected precisely if the [[global section]] [[geometric morphism]] $\Gamma : E \to Set$ is an [[essential geometric morphism]]. 

=--

+-- {: .proof}
###### Proof

This appears as Lemma C.3.3.6 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

=--

However, this doesn't mean that essential geometric morphisms are the "relative" analog of locally connected toposes; in general one needs to impose an additional condition, which is automatic in the case of the global sections morphism, to obtain the notion of a [[locally connected geometric morphism]].


### Locally connected and connected {#Connected}


A [[topos]] $E$ is called a [[connected topos]] if the [[right adjoint]] $LConst : Set \to E$ is a [[full and faithful functor]].


+-- {: .un_prop}
###### Proposition
If $\Gamma \colon E\to Set$ is a locally connected, topos, then it is als a [[connected topos]] -- in that $LConst$ is full and faithful -- if and only if the left adjoint $\Pi_0$ of the inverse image functor preserves the terminal object.
=--
+-- {: .proof}
###### Proof
This is C3.3.3 in the [[Elephant]].
=--

Notice that for a locally connected topos that is also a connected topos the adjunction

$$
  Set \stackrel{\overset{\Pi_0}{\leftarrow}}{\hookrightarrow} E
$$

exhibits [[Set]] as a [[reflective subcategory]] of $E$. We may think then of [[Set]] as being the [[localization]] of $E$ at those morphisms that induce isomorphisms of connected components.


## Examples {#Examples}

* For $X$ a [[topological space]], the [[category of sheaves]] $Sh(X) := Sh(Op(X))$ is a locally connected topos precisely if $X$ is a [[locally connected space]]. The functor $\Pi_0$ sends a sheaf $F \in Sh(X)$ to the set of connected components of the coresponding [[etale space]].

* For $C = $ [[CartSp]] the [[site]] of [[Cartesian space]] with their [[good open cover]] [[coverage]], we have that $Sh(CartSp)$ is locally connected.  An arbitrary $X \in Sh(CartSp)$ is sent to the [[colimit]] $\lim_\to X \in Set$. If $X$ is a [[diffeological space]] or even a [[smooth manifold]], then this is the set of connected components of the underlying topological space.

* Generally, if $C$ is a [[site]] such that constant [[presheaves]] on $C$ are [[sheaves]], then the left adjoint $\Pi_0$ exists and is given by the [[colimit]] functor, by the defining property of the colimit as a left [[Kan extension]] of presheaves:

  Write $L : PSh(C) \to Sh(C)$ for [[sheafification]] and assume that 
  constant presheaves are sheaves. Then

  $$
    Hom_{Sh(C)}(X, L Const S)
    \simeq
    Hom_{PSh(C)}(X, L Const S)
    \simeq
    Hom_{PSh(C)}(X, Const S)
    \simeq
    Hom_{Set}(\lim_\to X, S)
    \,.
  $$


=--

## Related entries


* **locally connected topos** / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]



[[!redirects locally connected topoes]]