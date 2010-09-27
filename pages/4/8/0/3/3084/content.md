
Let $G$ be a [[group object|group]] in some category $C$ of [[space]]s. We assume that for every space $X$ in $C$ some category of [[sheaf|sheaves]] $F_X$ is given, in a way making a [[fibered category]] $F$ over $C$. For example, we can consider sheaves of abelian [[group]]s over [[topological space]]s. 

Consider a $G$-space $X$ with [[action]] $\rho: G\times X\to X$ and projection $p: G\times X\to X$.  These data give rise to an [[action groupoid]] in the category of spaces, denoted by $[X/G]$ or sometimes $X//G$.  This groupoid can also be identified with its [[nerve]], which is a [[simplicial object]] in spaces.

An __equivariant sheaf__ over a $G$-space $X$ is a $G$-[[equivariant object]] in $F_X$. In other words, it is a sheaf $x$ over $X$ together with an isomorphism $\theta : p^* x \to \rho^* x$ of sheaves over $G\times X$ satisfying the usual cocycle condition on $G\times G\times X$. All equivariant sheaves form the equivariant fiber $F_X^G$ of $F$ over $X$. The equivariant fiber over $X$ is thought of as a fiber over the simplicial object $[X/G]$.

If the fibered category $F$ is a [[stack]] for some [[subcanonical topology|subcanonical Grothendieck topology]] on $C$ and $X$ a $G$-[[torsor]] over some true base space $X/G$ in $C$ then there is a descent along torsor: the equivariant fiber $F_X^G$ is canonically equivalent to the usual fiber over $X/G$. In other words the fibers over $[X/G]$ and $X/G$ are equivalent. 

If $F$ is not a [[stack]] one can instead of a [[Grothendieck topology]] in $C$ use the effective descent topology and include into the condition for a [[torsor]] instead of local triviality in a Grothendieck topology that $P$ over $X/G$ is an effective descent epimorphism relative to the fibered category $F$ over $C$. 

Notice that being an equivariant sheaf is an additional structure on a sheaf, rather than a property. Mumford introduced this notion in the geometric invariant theory under the name $G$-linearization of a sheaf. $G$-equivariant sheaves generalize (sheaves of sections of) $G$-equivariant bundles, as studied for example in representation theory earlier by Borel, Weil and Bott.

Note also that if "space" means [[topological space]] and $G$ is a [[topological group]] acting on the [[point]] $1$, then equivariant sheaves are just the same as continuous $G$-sets.  In particular, if $G$ is a discrete group, then equivariant sheaves are just the same as ordinary $G$-sets.

Observe that the definition of equivariant sheaf only depends on the [[action groupoid]], and thus can be generalized to equivariant sheaves on any internal groupoid in the category of spaces.  If "space" means [[locale]], then every [[Grothendieck topos]] can be presented as the category of equivariant sheaves on some [[localic groupoid]].  This is a theorem of [[André Joyal]] and [[Miles Tierney]], and can be found in chapter C5 of the [[Elephant]].

The appropriate notion of the "[[equivariant derived category]]" is in general not equal to the derived category of the [[abelian category]] of equivariant sheaves; one needs to resolve appropriately.  

[[!redirects equivariant sheaves]]