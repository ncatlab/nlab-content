#Idea#

[[Lawvere-Tierney topology|Lawvere-Tierney topologies]] generalize the notion of [[Grothendieck topology]] from [[presheaf]] [[Grothendieck topos|Grothendieck topoi]] of the form $E = PSh(S) = [S^{op}, Set]$ to general [[topos|topoi]]. 

By using [[dense monomorphism]]s in place of [[local isomorphism]]s, this induces a notion of [[sheafification]] on an arbitrary [[topos]] $E$ with [[Lawvere-Tierney topology]].

This sheafification is a [[functor]] 

$$
  \bar {(-)} : E \to Sh(E)
$$

to the [[subcategory]] $i : Sh(E) \hookrightarrow E$ of objects local with respect to [[dense monomorphism]]s which is

* [[exact functor|left exact]] (commutes with all small limits);

* [[left adjoint]] to $i$.

In the case that $E = PSh(S)$ and the Lawvere-Tierney topology is that corresponding to a Grothendieck topology on $S$, the two notions of [[sheafification]] coincide.

+--{: .query}
[[Mike Shulman|Mike]]: Why shouldn't all of this just be at [[Lawvere-Tierney topology]]?

Is "Lawvere-Tierney topos" supposed to mean "elementary topos?"  I've never heard that term before.
=--


#References#

section V.3 of

* MacLane, Moerdijk, [[Sheaves in Geometry and Logic]]
