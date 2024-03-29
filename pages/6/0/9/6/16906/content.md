A __right semiquantale__ is a [[complete lattice]] $Q$ with an associative binary operation $\bullet$ satisfying

$$ a\bullet  \Vee_\alpha b_\alpha = \Vee_\alpha (a \bullet b_\alpha),\,\,\,\,\,a, b_\alpha\in Q.$$

Symmetrically, a left semiquantale is a complete lattice $P$ with an associative binary operation $\bullet$ satisfying

$$  \left(\Vee_\alpha b_\alpha\right)\bullet c= \Vee_\alpha (b_\alpha \bullet c),\,\,\,\,\,c, b_\alpha\in P.$$

The main example of a right semiquantale is the lattice of the [[topologizing filter]]s of right (or left) ideals. 
These are the filters $\mathcal{F}\subset I_r R$ such that for all $I\in\mathcal{F}$
$$
   (I:r) := \{s\in R \,|\, r s\in I\}
$$
is also in $\mathcal{F}$ (i.e. $\mathcal{F}$ is a [[uniform filter]]) and if $J\in \mathcal{F}$ and $(I:r)\in I$ for all $r\in J$ then $I\in \mathcal{F}$.

The ordering is the reverse inclusion, thus the intersection is the supremum. The intersection of topologizing filters is topologizing, the lattice is complete and the product is the [[Gabriel multiplication]]

$$\mathcal{F}\bullet \mathcal{G} = \{ K\in I_r R\,|\,\exists L\in\mathcal{G}, K\subset L, \forall r\in K, (K:r)\in\mathcal{F}\} $$

The operation $\bullet$ preserves arbitrary intersections in the right variable. 

[[!redirects semiquantales]]
[[!redirects right semiquantale]]
[[!redirects left semiquantale]]