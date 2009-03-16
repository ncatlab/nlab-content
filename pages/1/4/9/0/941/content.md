Given a fibered category $\pi=\pi_F: F\to C$, a presheaf of groups $\hat{G}:C^{\mathrm{op}}\to\mathrm{Grp}$ (possibly representable), an object $X$ in $C$, and action $\hat\nu: \hat{G}\times h_X\to h_X$ (generalizing action $G\times X\to X$ in the representable case) one says that the object $\rho$ in the fiber $F_X = \pi^{-1}(\mathrm{id}_X)$ is $\hat{G}$-equivariant if $\hat{G}\circ\pi$ is equipped with an action on $h_\rho$, i.e. it is equipped with a natural transformation $\sigma:(\hat{G}\circ\pi)\times h_\rho : F^{\mathrm{op}}\to\mathrm{Set}$ such that for any $\xi\in F$, $\sigma_\xi:\hat{G}(\pi(\xi))\times\mathrm{Hom}_F(\xi,\rho)\to\mathrm{Hom}_F(\xi,\rho)$ satisfies the action axiom of a group $\hat{G}(\pi(\xi))$ on set $\mathrm{Hom}_F(\xi,\rho)$, and such that $\pi(\sigma)=\hat\nu$. The $\hat{G}$-equivariant objects naturally form a fibered category $\pi^{\hat{G}}:F^{\hat{G}}\to C$  of equivariant objects. 

Alternatively, if $F$ and $C$ are complete and $\hat{G}$ is represented by $G$ in $C$, the equivariant fiber over a $G$-object $X$ is simply the fiber over the simplicial object $[ X/G ]$ (simplicial Borel construction), that is the category of Cartesian functors $(\sigma^F,\sigma^C):\mathrm{Id}_{\Delta^{\mathrm{op}}}\to\pi_F$ from the opposite of the category of simplices $\Delta^{\mathrm{op}}$ considered as a fibered category $\mathrm{Id}_{\Delta^{\mathrm{op}}}:\Delta^{\mathrm{op}}\to\Delta^{\mathrm{op}}$ to the fibered category $\pi_F:F\to C$, such that the bottom component $\sigma_C = [X/G]:\Delta^{\mathrm{op}}\to C$.

Equivariant objects in fibered categories generalize the [[equivariant sheaf|equivariant sheaves]] which in turn generalize (the sheaves of sections of) $G$-equivariant bundles. The description of $G$-equivariant sheaves via cartesian sections over the simplicial Borel construction translates into the statement that they form the category equivalent to the subcategory of category of Deligne sheaves over the simplicial Borel construction whose all structure morphisms are isomorphisms. Mumford has expressed $G$-equivariant sheaves over $G$-space $(X,\nu)$ as sheaves $\rho$ equipped with an isomorphism $\theta:\nu^*(\rho)\to p^*(\rho)$ where $p:G\times X\to X$ is the projection and $\nu:G\times X\to X$ is action, and such that $\theta$ satisfies certain cocycle condition, which is an identity of sheaves over $G\times G\times X$. 

For $G$-equivariant sheaves over *topological* $G$-space $(X,\nu)$ (as opposed to $G$-object $(X,\nu)$ in a Grothendieck site) one can extend the canonical equivalence between etale spaces over $X$ and sheaves over $X$ to a canonical equivalence between the etale $G$-spaces over $(X,\nu)$ and $G$-equivariant sheaves over $(X,\nu)$. 

##Literature##

P. Deligne, Th&#233;orie de Hodge : III. Publications Math&#233;matiques de l'IH&#201;S, 44 (1974), p. 5-77 
(<a href="http://www.numdam.org/item?id=PMIHES_1974__44__5_0">numdam link</a>)

S. MacLane, I. Moerdijk, Sheaves in geometry and logic, Springer 1992.

D. Mumford, Geometric invariant theory. Ergebnisse der Mathematik und ihrer Grenzgebiete, Neue Folge, Band 34. Springer 1965. 2nd edition with J. Fogarty, Springer 1982.

Z. &#352;koda, Some equivariant constructions in noncommutative algebraic geometry, accepted to Georgian Math. J., <a href="http://arxiv.org/abs/0811.4770"> arXiv:0811.4770</a>.

A. Vistoli, Grothendieck topologies, fibered categories and descent theory. Fundamental algebraic geometry, 1-104, Math. Surveys Monogr., 123, AMS 2005, <a href="http://front.math.ucdavis.edu/0412.5512">arXiv:math.AG/0412512</a>.
