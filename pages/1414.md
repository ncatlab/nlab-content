#Idea#


The _homotopy cogerent nerve_  (also called _simplicial nerve of simplicial categories_ ) is a [[nerve]] operation of [[simplicially enriched category|simplicially enriched categories]] which sends an [[SimpSet|SSet]]-[[enriched category]] to a [[simplicial set]].

#Definition#



For $\Delta^n$ the standard [[simplicial set|simplicial]] $n$-[[simplex]], define the [[simplicially enriched category]] $S[\Delta^n]$ as follows:

* the objects of $S[\Delta^n]$ are $\{0,1, \cdots, n\}$;

* for $i, j \in \{0,1,\cdots, n\}$ define  $S[\Delta^n](i,j) = \left\lbrace \array{ \emptyset & if j \lt i \\ N(P_{i,j}) & if i \leq j }\right.$ where $P_{i,j}$ is the [[poset]]  $\left\{ I \subset J : (i,j \in I) \wedge (\forall k \in I) [i \leq k \leq j] \right\}$

* the composition operation is induced by ...


For $C$ a [[simplicially enriched category]], the **simplicial nerve**  $N(C)$ is the [[simplicial set]] uniquely characterized by the formula $ Hom_{SSet}(\Delta^n, N(C)) = Hom_{SSet-Cat}(S[\Delta^n], C)$.





#Remarks#

* The simplicial nerve, together with its [[adjoint functor|left adjoint]], serves to relate the two models of [[(infinity,1)-category|(infinity,1)-categories]] given by [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicially enriched categories]].

#References#

The simplicial nerve operation was introduced in

* J. M. Cordier, _Sur la notion  de diagramme homotopiquement coh6eacute;rent_, Cahier Top. et Geom. Diff. XXIII 1, 1982, 93-112

For the role played by the simplicial nerve in the context for relating quasi-categories to simplicially enriched categories as models for $(\infty,1)$-categories see section 1.1.5 of

* [[Jacob Lurie]], [[Higher Topos Theory]]