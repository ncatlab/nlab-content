The [[Yoneda embedding]]
$$y_S: S \to Set^{S^{op}}$$ 
of a [[small category]] $S$ into the category $Set^{S^{op}}$ of [[presheaf|presheaves]] on $S$ 
is universal among functors from $S$ into (small) [[cocomplete category|cocomplete categories]], in the sense that given a functor $F: S \to D$ where $D$ is cocomplete, there exists a unique (up to isomorphism) [[cocontinuous functor|cocontinuous]] extension 
$$\hat{F}: Set^{S^{op}} \to D,$$
meaning that $\hat{F} y_S \cong F$ and $\hat{F}$ preserves small colimits. Indeed, the desired $\hat{F}$ is [[adjoint functor|left adjoint]] to the functor 
$$D \to Set^{S^{op}}: d \mapsto \hom_D(F-, d)$$ 

An explicit formula for the left adjoint is given by the [[weighted colimit]] or [[end|coend]] formula 
$$\hat{F}(X) = X \otimes_S F = \int^{s: S} X(s) \cdot F(s)$$ 
where $S \cdot d$ is notation for [[power|copowering]] (or tensoring) an object $d$ of $D$ by a set $S$ (in this case, a coproduct of an $S$-indexed set of copies of $D$). This formula recurs frequently throughout this wiki; see also [[nerve]], [[Day convolution]]. 

This "free cocompletion" property generalizes to [[enriched category]] theory. If $V$ is complete, cocomplete, symmetric monoidal closed, and $S$ is (small) enriched in $V$, then the enriched presheaf category $V^{S^{op}}$ is a free $V$-cocompletion of $S$. The explicit meaning is analogous to the case where $V = Set$, where all ordinary category concepts are replaced by their $V$-enriched analogues; in particular, the notion of "$V$-cocontinuous functor" referes to preservation of enriched weighted colimits (not just ordinary conical colimits). 