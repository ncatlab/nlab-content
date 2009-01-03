+-- {: .un_defn}
###### Definition
Let $E$ be a [[topos]], with [[subobject classifier]] $\Omega$. A _Lawvere-Tierney topology_ is a map $j: \Omega \to \Omega$ which is internally a left exact monad (on the internal meet-semilattice $\Omega$). That is to say, where $j$ satisfies the following properties: 
$$1 \leq j: \Omega \to \Omega \qquad j \circ j = j: \Omega \to \Omega \qquad j(\wedge) = \wedge(j \times j): \Omega \times \Omega \to \Omega$$
where $\leq$ is the internal partial order on $\Omega$, and $\wedge: \Omega \times \Omega \to \Omega$ is the internal meet. 
=--


#Remarks#

* A special case of a Lawvere-Tierney topology is a [[Grothendieck topology]].