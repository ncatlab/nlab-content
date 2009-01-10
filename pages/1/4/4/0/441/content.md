#Idea#

The _horn_ $\Lambda^k[n] \hookrightarrow \Delta^n$ is the [[simplicial set]] obtained from the boundary $\partial \Delta^n$ of the standard simplicial $n$-[[simplex]] $\Delta^n$ by discarding the $k$th face.

#Definition#

Set $\Delta[n] = \mathbf{\Delta}( -, [n]) \in  SimplicalSets$, then, or each $i$, $0 \leq i \leq n$, we can form, within $\Delta[n] $, a subsimplicial set, $\Lambda^i[n]$, called the **$(n,i)$-horn** or **$(n,i)$-box**, by discarding the top dimensional $n$-simplex (given by the identity map on $[n]$) and its $i^{th}$ face.  We must also discard all the degeneracies of those simplices.


#Relation to other concepts#

* A [[Kan fibration]] is a morphism of simplicial sets which has the right [[lifting property]] with respect to all horn inclusions $\Lambda^k[n] \hookrightarrow \Delta^n$.

* A [[Kan complex]] is a simplicial set in which "_all horns have fillers_": a simplicial set for which the morphism to the point is a Kan fibration.