## Idea

Given a category $E$ with pullbacks, one can consider the [[bicategory]] $Cat(E)$ of [[internal categories]] in $E$, and thus [[internal functors]], which are the morphisms in $Cat(E)$. If $E = Set$ then one can consider not only functors among small categories but also functors of the type $F: C\to Set$ from a small category $C$ to a large category of sets. In that case one can describe $F$ as consisting of a $C_0$-indexed family of objects and an action of $C_1$ on the diagram.

Compare the ideas discussed on this page with those at [[internal profunctor]] and [[discrete fibration]].  All three notions intersect --- an internal diagram on $C$ is the same thing as an internal profunctor $1 &#8696; C$, which is the same thing as a discrete fibration in $Cat(E)$.  The three generalize the basic idea in different ways.

## Definition

Given $C\in Cat(E)$ an **internal diagram** $F$ on $C$ (or, of type $C$) consists of 

* a morphism $\lambda : F_0\to C_0$ in $E$
* a morphism $e : F_1 = F_0\times_{C_0} C_1\to C_1$

such that action axioms hold as well as the compatibility with "momentum" $\lambda$ i.e. $\lambda e = d_1 pr_2$.

It is clear how to define then the morphisms of internal diagrams. Internal diagrams in $E$ of type $C$ form a category denoted by $E^C$. 

## Characterization

From an internal diagram $(F,C,\lambda,e)$ one can equip $F =(F_0,F_1)$ with a strcuture of an internal category over $C$. In other words, there is a forgetful functor $E^C\to Cat(E)/C$ (where $Cat(E)/C$ is the corresponding [[slice category]]). This functor is fully faithful and its essential image consists precisely of all objects in $Cat(E)/C$ which are [[discrete fibration]]s. 

## Diagrams in an indexed category

An internal diagram as above may take values in any [[Grothendieck fibration]] over $S$.  Given a fibration in the guise of an [[indexed category]] $E : S^{op} \to Cat$, a **$C$-diagram in $E$** is given by

* an object $P \in E(C_0)$, together with
* a morphism $\phi : s^* P \to t^* P$ in $E(C_1)$

satisfying 'cocycle equations'

* $i^*\phi = 1_P$
* $c^*\phi = p_1^* \phi \circ p_2^* \phi$

modulo coherent isos, where the $p_i$ are the projections out of $C_2$.

By the [[Yoneda lemma for bicategories]], the object $P$ determines (up to canonical isomorphism) a pseudonatural $\alpha^0 : S(-,C_0) \to E_0$ in $[S^{op},Cat]$, where $S$ is considered as a locally discrete bicategory, and $E_0(X) = ob E X$ considered as a discrete category, such that $\alpha^0(f) \cong f^* P$.  Similarly, $\phi$ determines $\alpha^1 : S(-,C_1) \to E_1 = arr \circ E$, and $\alpha^1(g) \cong g^* \phi$.  It is not hard to check that the conditions above correspond to requiring that the $\alpha^i_X$ form a functor $S(X,C) \to E X$ for each $X$, and pseudonaturality then makes the $C$-diagram $(P,\phi)$ equivalent to an [[indexed functor]] $S(-,C) \to E$.  The category of $C$-diagrams in $E$ is then simply the hom-category $[S^{op},Cat](S(-,C),E)$.

### Examples

* An internal diagram on $C$ in the sense above is a $C^{op}$-diagram in the [[codomain fibration]] of $S$, that is the pseudofunctor $X \mapsto S/X$.

* If $S$ is equipped with a [[coverage]] and $C$ is the [[Cech nerve]] associated to a cover $p : U \to X$ in $S$, then the category of $C$-diagrams in $E$ is the [[descent]] category $Des_p(E)$.


## References

* [[P. T. Johnstone]], _Topos theory_, 1977, chapter 2 