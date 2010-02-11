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

Let $E$ be a [[topos]]. An object $A \in E$ is called a **connected object** if there do not exist two nontrivial objects $A_1, A_2 \neq \emptyset$ such that a is given by their [[coproduct]] as $A \simeq A_1 \coprod A_2$.

The topos $E$ is called a **locally connected topos** is every object $A \in E$ is a [[coproduct]] of connected objects $\{A_i\}_{i \in I}$, $A = \coprod_{i \in I} A_i$. 

The index set $I$ is unique up to isomorphism and we write

$$
  \pi_0(A) = I
  \,.
$$

The topos $E$ is called a **connected topos** if for $* \in E$ the [[terminal object]] we have $\pi_0(*) = *$.


This constructoin defines a functor $\Pi_0 : E \to Set : A \mapsto \pi_0(A)$ which is [[left adjoint]] to the [[constant sheaf]] functor, the [[left adjoint]] part of the [[global section]] [[geometric morphism]], so that for a locally connected topos we have

$$
  (\Pi_0 \dashv LConst \dashv \Gamma) : 
  E \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  Set
  \,.
$$

This left adjoint $\Pi_0$ is the lowest degree incarnation of a general construction of [[homotopy groups in an (∞,1)-topos]].

## More...

...to come.

[[!redirects locally connected topos]]
[[!redirects connected topos]]
[[!redirects locally n-connected (∞,1)-topos]]
[[!redirects locally contractible (infinity,1)-topos]]
[[!redirects locally contractible (∞,1)-topos]]
[[!redirects n-connected (∞,1)-topos]]
[[!redirects contractible (infinity,1)-topos]]
[[!redirects contractible (∞,1)-topos]]
