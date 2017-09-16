#Idea#


The _homotopy cogerent nerve_ (also called _simplicial nerve_) of a [[simplicial category|simplicially enriched categories]] is its [[nerve]] as a [[simplicial set]].

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

# Discussion #

The following discussion was at [[simplicial nerve]] when this page was at [[simplicial nerve of simplicial categories]].
+-- {: .query}
Is there a simplicial nerve that\'s not of simplicial categories?  If not, I\'d put the article here instead of there.  ---Toby

[[Urs Schreiber|Urs]]: yes, it seems to be called just "simplicial nerve" in the literature, but I found that a bit undescriptive, since every nerve is "simplicial" and here the point is really that we take the nerve _of_ a simplicial category. I also seem to recall that [[Tim Porter|Tim]] said he doesn't like the term "simplicial nerve". Maybe Tim should decide, he is probably the one among us who has thought about this notion the most.

_Toby_:  Ah, I see how 'simplicial nerve' is confusing; so how about just [[nerve of a simplicial category]]?

[[Urs Schreiber|Urs]]: right, that might be the best option -- I have to run now, maybe you can implement that?

_Toby_:  I\'ll wait to hear from Tim.

[[Mike Shulman|Mike]]: Not all nerves are simplicial; it depends on what you are taking the nerve of.  The nerve of a multicategory is a dendroidal set (a presheaf on the category of trees).  The nerve of a compact symmetric multicategory is a presheaf on the category of Feynman graphs.  And an $n$-category has a nerve that is a simplicial set, but also one that is a $\Theta_n$-set and one that is an $n$-fold simplicial set.

FWIW, I have sometimes seen the "simplicial nerve of simplicial categories" called the "homotopy coherent nerve," which to me captures the intuition better.

[[Urs Schreiber|Urs]]: true, I actually know that not every notion of nerve is simplicial, should have thought before typing. 

Now that you mention it, maybe [[Tim Porter]] also said he favored "homotopy coherent nerve"? I'll send him an email.
=--