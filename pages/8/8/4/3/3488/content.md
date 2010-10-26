

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
=--
=--
=--




#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[topos]] may be thought of as a generalized [[topological space]]. Accordingly, the notions of 

* [[locally connected space]]

* locally 2-connected space

* etc. ...

* [[locally contractible space]]

have analogs for [[topos]]es and [[(∞,1)-topos]]es

* [[locally connected topos]]
 
* **locally $n$-connected $(n,1)$-topos**

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



## Locally $n$-connected $(n,1)$-topos {#nCase}

> [[Urs Schreiber]]: I want to make the following

+-- {: .un_defn}
###### Definition

An [[(n,1)-topos]] $\mathbf{H}$ is **locally $n$-connected** if the [[global section]] [[geometric morphism]]  $\Gamma : \mathbf{H} \to n Grpd$ is an [[essential geometric morphism]]

$$
  (\Pi_n \dashv LConst \dashv \Gamma)\;\;\; :
  \;\;\;
  \mathbf{H} \stackrel{\overset{\Pi_n}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  n Grpd
  \,.
$$

=--

In this case we call for $X \in \mathbf{H}$ the [[n-groupoid]] $\Pi_n(X)$ the **fundamental $n$-groupoid** of $X$. See [[homotopy groups in an (∞,1)-topos]].


## Locally ∞-connected $(\infty,1)$-topos {#InfCase}

A locally $n$-connected $(n,1)$-topos for $n = \infty$ we call a **locally ∞-connected $(\infty,1)$-topos**. 

In this case $\Pi = \Pi_\infty$ is the [[schreiber:homotopy ∞-groupoid]] functor.



### Examples {#LocallyContractibleExamples}

This proposition gives a large supply of examples.

+-- {: .un_prop}
###### Proposition

Let $C$ be a [[site]] whose [[Grothendieck topology]] is generated from a given [[coverage]] of [[covering]] families,  such that its objects are **geometrically contractible**, meaning that all constant [[simplicial presheaf|simplicial presheaves]] satisfy [[descent]] on objects of $C$ with respect to these generating covering families.

Then the corresponding [[(∞,1)-category of (∞,1)-sheaves]] $\mathbf{H} = Sh_{(\infty,1)}(C)$ is a locally $\infty$-connected $(\infty,1)$-topos.

=--

+-- {: .proof}
###### Proof

The proof is currently at [[schreiber:homotopy ∞-groupoid]].

=--

In the literature this statement is known somewhat implicitly in slightly weaker form or in special cases:

* The old Artin-Masur result recalled at [[homotopy groups in an (∞,1)-topos]] (see there for the moment) says effectively that the old prescription for computing $\Pi$ gives the right answer over a topological space if that has a basis of locally contractible open subsets. But that just means that the condition of the above proposition is satisfied.

* [Proposition 2.18](http://math.berkeley.edu/~teleman/math/simpson.pdf#page=5) of

  * [[Carlos Simpson]], [[Constantin Teleman]], _de Rham's theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

  and the definition before that states essentially what the above proposition states at the level of [[homotopy category|homotopy categories]]: it asserts that if $C$ has contractible objects, that then there exists a left adjoint $Ho(\Pi):Ho(Sh_{(\infty,1)}(C)) \to Ho(\infty Grpd)$. They also give the explicit formula which is stated at [[schreiber:homotopy ∞-groupoid]].


### Properties {#LocInfConnProperties}

+-- {: .un_prop}
###### Observation

For $\mathbf{H}$ a locally $\infty$-connected $(\infty,1)$-topos, also all its objects $X \in \mathbf{H}$ are locally $\infty$-connected, in that their [[petit topos|petit]] [[over quasi-category|over-(∞,1)-toposes]] $\mathbf{H}/X$ are locally $\infty$-connected.

=--

+-- {: .proof}
###### Proof

By the general facts recalled at [[etale geometric morphism]] we have an [[essential geometric morphism]]

$$
  (\Pi \circ \pi_! \dashv \pi^*\circ L Const \dashv \Gamma \circ \pi_*) : 
  \mathbf{H}_{/X}
   \stackrel{\overset{\pi_!}{\to}}{\stackrel{\overset{\pi^*}{\leftarrow}}{\underset{\pi_*}{\to}}}
  \mathbf{H}
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{\L Const}{\leftarrow}}{\underset{\Gamma}{\to}}}  
   \infty Grpd
  \,.
$$

=--


### Further structures

The fact that the terminal geometric morphism is essential gives rise to various induced structures of interest. For instance it induces a notion of 

* [[Whitehead tower in an (∞,1)-topos]].

For a more exhaustive list of extra structures see 

* [[schreiber:structures in an (∞,1)-topos]].

### Locally $\infty$-connected and $\infty$-connected {#Contractible}

By analogy with the situation for [[connected topos]]es discussed [above](#Connected), an $(\infty,1)$-topos $\mathbf{H}$ is [[∞-connected (∞,1)-topos|∞-connected]] if and only if the left adjoint $\Pi$ preserves the terminal object.
In this case, the $(\infty,1)$-adjunction

$$
  \infty Grpd \stackrel{\overset{\Pi}{\leftarrow}}{\hookrightarrow} \mathbf{H}
$$

exhibits [[∞Grpd]] as a [[reflective sub-(∞,1)-category]] of $\mathbf{H}$. We may think then of [[∞Grpd]] as being the [[localization of an (∞,1)-category|localization]] of $E$ at those morphisms that induce equivalences on <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#GeomReal">intrinsic geometric realizations</a>, hence isomorphisms on _geometric_ [[homotopy groups in an (∞,1)-topos]].


#### Examples

All the locally connected $(\infty,1)$-toposes on sites with geometrically contractible objects given by the proposition [above](#LocallyContractibleExamples) are also $\infty$-connected.

In particular the $(\infty,1)$-topos $\infty LieGrpd := Sh_{(\infty,1)}(CartSp)$ over the site [[CartSp]] is $\infty$-connected. This is discussed in detail at

* [[∞-Lie groupoid]].

## Related concepts

* [[locally connected topos]] / **locally ∞-connected (∞,1)-topos**

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]





[[!redirects locally n-connected (∞,1)-topos]]
[[!redirects locally contractible (infinity,1)-topos]]
[[!redirects locally contractible (∞,1)-topos]]
[[!redirects n-connected (∞,1)-topos]]

[[!redirects locally infinity-connected (∞,1)-topos]]
[[!redirects locally ∞-connected (∞,1)-topos]]


[[!redirects contractible (infinity,1)-topos]]
[[!redirects contractible (∞,1)-topos]]
[[!redirects contractible (infinity,1)-toposes]]
[[!redirects contractible (∞,1)-toposes]]

[[!redirects locally n-connected (infinity,1)-topos]]
[[!redirects locally n-connected (infinity,1)-tops]]



[[!redirects locally connected (∞,1)-geometric morphism]]
[[!redirects connected (∞,1)-geometric morphism]]
[[!redirects essential (∞,1)-geometric morphism]]