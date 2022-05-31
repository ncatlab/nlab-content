
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[Lawvere-Tierney topology]] on a [[topos]] defines naturally a certain closure operation on [[subobjects]]. A subobject inclusion is called _dense_ (a _dense monomorphism_) if its closure is an [[isomorphism]].  In other words, a _dense subobject_ of an object $B$ is a subobject whose closure is all of $B$.



## Definition

Let $E$ be a [[topos]] equipped with a [[Lawvere-Tierney topology]] $j : \Omega \to \Omega$.

For every [[subobject]] $A \hookrightarrow B$ in the [[topos]] classified by $char A : B \to \Omega$, let its **closure**

$$
  \bar A \hookrightarrow B
$$

be the subobject classified by $char \bar A := B \stackrel{char A}{\to} \Omega \stackrel{j}{\to} \Omega$.

The monomorphism $A \hookrightarrow B$ is called a **dense monomorphism** if $\bar A = B$, that is if $\bar A \hookrightarrow B$ is an [[isomorphism]].


## Relation to other concepts


### To local isomorphisms


Recall that when $E$ is a [[presheaf]] [[Grothendieck topos]] $E = PSh(S) = [S^{op}, Set]$ then [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] on $E$ are in bijection with [[Grothendieck topology|Grothendieck topologies]] on $S$ (making $S$ a [[site]]).
In this case there is the notion of [[local epimorphism]] and [[local isomorphism]] in $PSh(S)$ with respect to this topology. 

We have in this case:

the dense monomorphisms in $PSh(S)$ are precisely the [[local isomorphisms]] that are at the same time ordinary [[monomorphisms]].

###  To sheafification ##

A [[presheaf]] $F \in PSh(S)$ is a [[sheaf]] with respect to the given topology if $Hom_{PSh(S)}(-, F)$ sends all dense monomorphisms to [[isomorphisms]].


Since Lawvere-Tierney topologies make sense for every [[topos]] (not necessarily a [[presheaf]]  [[Grothendieck topos]]) this provides a general notion of [[Lawvere-Tierney topology|sheafification in a Lawvere-Tierney topology]].

## Related concepts

* [[dense]]

## References

Dense monomorphisms appear around p. 223 of

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

[[!redirects dense monomorphisms]]

[[!redirects dense subobject]]
[[!redirects dense subobjects]]