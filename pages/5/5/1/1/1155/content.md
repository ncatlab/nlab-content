#Idea#

A _combinatorial spectrum_ is to a [[spectrum]] of [[topological space]]s as a [[simplicial set]] is to a [[topological space]]: it is a graded set that behaves like a set of simplices constituting a space, where the special property is that the simplices are not just in non-negative degree $n \in \mathbb{N}$ but in all integral degrees $n \in \mathbb{Z}$.

#Definition#

A **simplicial spectrum** is 

* a sequence $E = \{E_n\}_{n \in \mathbb{Z}}$ of [[pointed set]]s 

* equipped for each $n \in \mathbb{Z}$ and $i \in \mathbb{N}$ with

  * morphisms of [[pointed set]]s $d_i : E_n \to E_{n-1}$ called **face maps**;

  * morphisms of [[pointed set]]s $s_i : E_n \to E_{n+1}$ called **degeneracy maps**

* such that

  * the usual [[simplicial set|simplicial identities]] are satisfied;

  * each face map sends only finitely many elements not to the point.

+--{: .query}
[[Mike Shulman|Mike]]: Are you sure about that last condition?  I remember a condition more like "for each $x\in E_n$ there is some finite $m \lt n$ such that all faces of $x$ in $E_m$ are the basepoint.
=--


#Examples#

...

#References#

Part II, section 7 of 

* Ken Brown, [[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]




