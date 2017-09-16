#Idea#

A [[Lawvere-Tierney topology]] on a [[topos]] defines naturally a certain closure operation on every object. A subobject inlcusion is called a _dense monomorphism_ if after taking the closure of its domain it becomes an isomorphism.



#Definition#

Let $E$ be a [[topos]] equipped with a [[Lawvere-Tierney topology]] $j : \Omega \to \Omega$.

For every [[subobject]] $A \hookrightarrow E$ in the [[topos]] classified by $char A : E \to \Omega$, let its **closure**

$$
  \bar A \hookrightarrow E
$$

be the subobject classified by $char \bar A := E \stackrel{char A}{\to} \Omega \stackrel{j}{\to} \Omega$.

The monomorphism $A \hookrightarrow E$ is called a **dense monomorphism** if $\bar A = E$.





#Relation to local isomorphism#

Recall that when $E$ is a [[presheaf]] [[Grothendieck topos]] $E = PSh(S) = [S^{op}, Set]$ then [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] on $E$ are in bijection with [[Grothendieck topology|Grothendieck topologies]] on $S$ (making $S$ a [[site]]).
In this case there is the notion of [[local epimorphism]] and [[local isomorphism]] in $PSh(S)$ with respect to this topology. 

We have in this case:

the dense monomorphisms in $PSh(S)$ are precisely the [[local isomorphism]]s that are at the same time ordinary [[monomorphism]]s.

##  Relation to sheafification ##

A [[presheaf]] $F \in PSh(S)$ is a [[sheaf]] with respect to the given topology if $Hom_{PSh(S)}(-, F)$ sends all dense monomorphisms to [[isomorphism]]s.


Since Lawvere-Tierney topologies make sense for every [[topos]] (not necessarily a [[presheaf]]  [[Grothendieck topos]]) this provides a general notion of [[Lawvere-Tierney topolog|sheafification in a Lawvere-Tierney topology]].


#References#

Dense monomorphisms appear around p. 223 of

* MacLane, Moerdijk, [[Sheaves in Geometry and Logic]]