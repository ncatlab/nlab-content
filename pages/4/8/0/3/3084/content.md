Let $G$ be a group in some category $C$ of spaces. We assume that for every space $X$ in $C$ some category of sheaves $F_X$ is given, in a way making a [[fibered category]] $F$ over $C$. For example, we can consider sheaves of abelian groups over topological spaces. 

Consider a $G$-space $X$ with action $\rho: G\times X\to X$ and projection $p: G\times X\to X$: one associates to these data the simplicial object denoted by $[X/G]$ or sometimes $X//G$. 

An __equivariant sheaf__ over a $G$-space $X$ is a $G$-[[equivariant object]] in $F_G$. In other words, it is a sheaf $x$ over $X$ together with an isomorphism $\theta : p^* x \to \rho^* x$ of sheaves over $G\times X$ satisfying the usual cocycle condition on $G\times G\times X$. All equivariant sheaves form the equivariant fiber $F_X^G$ of $F$ over $X$. The equivariant fiber over $X$ is thought of as a fiber over the simplicial object $[X/G]$.

If the fibered category $F$ is a [[stack]] for some [[subcanonical topology|subcanonical Grothendieck topology]] on $C$ and $X$ a $G$-[[torsor]] over some true base space $X/G$ in $C$ then there is a descent along torsor: the equivariant fiber $F_X^G$ is canonically equivalent to the usual fiber over $X/G$. In other words the fibers over $[X/G]$ and $X/G$ are equivalent. 

If $F$ is not a stack one can instead of a Grothendieck topology in $C$ use the effective descent topology and include into the condition for a torsor instead of local triviality in a Grothendieck topology that $P$ over $X/G$ is an effective descent epimorphism relative to the fibered category $F$ over $C$. 

Notice that being an equivariant sheaf is an additional structure on a sheaf, rather than a property. Mumford introduced this notion in the geometric invariant theory under the name $G$-linearization of a sheaf. $G$-equivariant sheaves generalize (sheaves of sections of) $G$-equivariant bundles, as studied for example in representation theory earlier by Borel, Weil and Bott.