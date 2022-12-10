##Idea

We have some group, $H$, with a subgroup, $A$, together with a monomorphism, $\theta : A\to H$.   The **HNN-extension** $H\ast_A$ is obtained by adjoining an element $t$ to $H$
subject to the relations:
$$t^{-1}at= \theta(a)$$
for all $a\in A$.

The idea is thus that the two copies of $A$ in $H$ given by $A$ itself and $\theta(A)$ become conjugate subgroups in $H\ast_A$.

##Link with graphs of groups

Examine the [[fundamental group of a graph of groups|fundamental group]] of the [[graph of groups]], $\mathcal{G}$, with underlying graph the graph with one vertex, $v$ and one edge, $e$ and nothing else. Take the vertex group, $G_v$, to be $H$, the edge group, $G_e$, to be $A$, and the two morphisms from $G_e$ to $Gv$ are the inclusion of $A$ into $H$ and the given monomorphism, $\theta$, then $\Pi_1(\mathcal{G})(v) \cong H*_A$.

##As a 2-colimit

The functor $\mathbf{Grp} \to \mathbf{Grpd},G \mapsto BG$ allows us to view [[Grp|the category of groups]] as a 2-category. Explicitly, this means that for two morphisms $(\varphi,\theta):H \rightrightarrows G$, a 2-morphism $\varphi \to \theta$ is an element $g \in G$ such that $g\varphi g^{-1}=\vartheta$.

With this strict 2-category, one can describe a HNN-extension as a strict [[2-limit]]. If $\iota:K \to G$ denotes the subgroup inclusion and $\theta:K \to G$ is a monomorphism, then $G\ast_A$ is the [[inserter|coinserter]] of $(\theta,\iota):K \rightrightarrows G$.


##References

* J.-P. Serre, 1977, _Arbres, amalgames, $SL_2$_, volume 46 of _Ast&#233;risque , Soci&#233;t&#233; math&#233;matique 
de France.  

* J.-P. Serre, 2003, _Trees_ , Springer Monographs in Mathematics, Springer-Verlag Berlin.  
150, 157, 161 