It is often natural that a symmetry object acting on some space is in the category of spaces itself. For example, algebraic groups acts on varieties, topological groups on topological spaces, and group schemes over $S$ act on $S$-schemes. 

Suppose now we want to define an action of a Hopf $k$-algebra $H$ on a noncommutative $k$-scheme, where we view a Hopf algebra as a dual to a noncommutative analogue of an affine group object over $Spec(k)$. In nonaffine situations noncommutative schemes are glued from algebras, but they are not described by a single algebra, but by a system of algebras; in fact a more canonical object is the category of quasicoherent sheaves which localizes to categories of modules over each of the algebras of the cover; these categories of modules are monadic over the category $V = {}_{k}Mod$
which is the category of quasicoherent sheaves over $Spec(k)$. The Hopf algebra, to be considered as a noncommutative space, has to be replace by the *monoidal* category $\mathcal{M} = {}_{H}Mod$ which comes equipped with a canonical action on $V$: tensor and forget the additional structure. The Hopf algebra should be reconstructed from the forgetful functor to $V$; it is itself a comonoid in $M$. What does it mean that $H$ acts on some noncommutative space represented by a category $C$ ? Well it has no meaning unless $C$ has a forgetful functor to $V$ as well (like in the case of possibly noncommutative $k$-schemes). Now the action of $Spec(H)$ corresponds to the action of the monodial category $M$ on $C$. But not any action: the action which is compatible with the action of $M$ on $V$. Such actions are called __geometrically admissible actions__ of monoidal category. Admisibility is a notion relative to the action of the same monoidal category on the base category. In other words admissible actions are the actions of monoidal categories on categories which lift the defining action on the base. In special cases, the liftings correspond to the distributive laws. This is the origin of appearance of coalgebra bundles in noncommutative geometry: [[entwining structure]]s induce lifts to admissible actions; however there are other cases of distributive laws and more general lifts which are not coming from entwinings between coalgebras and algebras. 

Another example is given by the action of the monoidal category of sheaves on a topological group $G$ on a topological $G$-space $X$. The action $Sh(G)$ on $Sh(X)$ is given by the pushforward along the action $G\times X\to X$ of the external tensor product of sheaves $Sh(G)\times Sh(X)\to Sh(G\times X)$. 

As a general definition, we start with a fixed notion of a symmetry object as a monoidal category $M$ with distinguished action $\lozenge$ on the base category $V$. A geometrically admissible action $\tilde{\lozenge}$ in wider sense is any action of $M$ on some category $C$ over $V$ such that 

$$\array{
M\times C&\stackrel{\tilde{\lozenge}}\to& C\\
\downarrow && \downarrow\\
M\times V&\stackrel{\lozenge}\to& V
}$$ 

commutes.

> Remark: For admissible actions in much more narrow sense one also has a forgetful functor $M\to V$ and one requires that the action below is in the fact factoring through that functor. In other words, the tensor product of $V$ lifts to an action of $M$ in $Cat/V$.

* [[Z. Škoda]], _Some equivariant constructions in noncommutative algebraic geometry_, Georgian Mathematical Journal __16__ (2009), No. 1, 183--202, [arXiv:0811.4770](http://arxiv.org/abs/0811.4770).

[[!redirects geometrically admissible actions]]