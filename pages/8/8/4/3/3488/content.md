[[!redirects locally n-connected (infinity,1)-tops]]
[[!redirects locally connected topos]]


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[topos]] may be thought of as a generalized [[topological space]]. Accordingly, the notions of 

* [[locally connected space]]

* locally 2-connected space

* etc. ...

* [[locally contractible space]]

have analogs for [[topos]]es and [[(∞,1)-topos]]es.

## Locally connected topos

Let $E$ be a [[topos]]. An object $A \in E$ is called a [[connected object]] if $\hom_E(A, -)$ preserves finite [[coproduct]]s. Equivalently, an object $A$ is connected if it is nonempty (non[[initial object|initial]]) and cannot be expressed as a coproduct of two nonempty [[subobject]]s. 

A [[Grothendieck topos]] $E$ is called a **locally connected topos** is every object $A \in E$ is a [[coproduct]] of connected objects $\{A_i\}_{i \in I}$, $A = \coprod_{i \in I} A_i$.  It follows that the index set $I$ is unique up to isomorphism, and we write

$$
  \pi_0(A) = I
  \,.
$$

A locally connected topos $E$ is called a **connected topos** if for $* \in E$ the [[terminal object]] we have $\pi_0(*) = *$.  (There is a more general notion of a [[connected topos]] which is not necessarily locally connected, but for locally connected topoi it is equivalent to this definition.)

This construction defines a functor $\Pi_0 : E \to Set : A \mapsto \pi_0(A)$ which is [[left adjoint]] to the [[constant sheaf]] functor, the [[left adjoint]] part of the [[global section]] [[geometric morphism]].  Thus, for a locally connected topos we have

$$
  (\Pi_0 \dashv Const \dashv \Gamma) : 
  E \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{Const}{\leftarrow}}{\overset{\Gamma}{\to}}}
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

This appears as Lemma C.3.3..6 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

=--


## Locally $n$-connected $(n,1)$-topos {#nCase}

> [[Urs Schreiber]]: I want to make the following

+-- {: .un_defn}
###### Definition

An [[(n,1)-topos]] $\mathbf{H}$ is **locally $n$-connected** if the [[global section]] [[geometric morphism]]  $\Gamma : \mathbf{H} \to n Grpd$ is an [[essential geometric morphism]]

$$
  (\Pi_n \dashv LConst \dashv \Gamma)\;\;\; :
  \;\;\;
  \mathbf{H} \stackrel{\overset{\Pi_n}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  n Grpd
  \,.
$$

=--

In this case we call for $X \in \mathbf{H}$ the [[n-groupoid]] $\Pi_n(X)$ the **fundamental $n$-groupoid** of $X$. See [[homotopy groups in an (∞,1)-topos]].


## Locally contractible $(\infty,1)$-topos {#InfCase}

A locally $n$-connected $(n,1)$-topos for $n = \infty$ we call a **locally contractible $(\infty,1)$-topos**. 

In this case $\Pi = \Pi_\infty$ is the [[schreiber:homotopy ∞-groupoid]] functor.



### Examples

This proposition gives a large supply of examples.

+-- {: .un_prop}
###### Proposition

Let $C$ be a [[site]] with **geometrically contractible objects**, meaning that all constant [[simplicial presheaf|simplicial presheaves]] satisfy [[descent]] on objects of $C$.

Then $\mathbf{H} = Sh_{(\infty,1)}(C)$ is a locally contractible $(\infty,1)$-topos.

=--

+-- {: .proof}
###### Proof

The proof is currently at [[schreiber:homotopy ∞-groupoid]].

=--

In the literature this statement is known somewhat implicitly in slightly weaker form or in special cases:

* The old Artin-Masur result recalled at [[homotopy groups in an (∞,1)-topos]] (see there for the moment) says effectively that the old prescription for computing $\Pi$ gives the right answer over a topological space if that has a basis of locally contractible open subsets. But that just means that the condition of the above proposition is satisfied.

* [Proposition 2.18](http://math.berkeley.edu/~teleman/math/simpson.pdf#page=5) of

  * [[Carlos Simpson]], [[Constantin Teleman]], _de Rham's theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

  and the definition before that states essentially what the above proposition states at the level of [[homotopy category|homotopy categories]]: it asserts that if $C$ has contractible objects, that then there exists a left adjoint $Ho(\Pi):Ho(Sh_{(\infty,1)}(C)) \to Ho(\infty Grpd)$. They also give the explicit formula which is is stated at [[schreiber:homotopy ∞-groupoid]].


[[!redirects locally connected topos]]
[[!redirects connected topos]]
[[!redirects locally n-connected (∞,1)-topos]]
[[!redirects locally contractible (infinity,1)-topos]]
[[!redirects locally contractible (∞,1)-topos]]
[[!redirects n-connected (∞,1)-topos]]
[[!redirects contractible (infinity,1)-topos]]
[[!redirects contractible (∞,1)-topos]]
