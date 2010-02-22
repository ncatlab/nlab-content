
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **topological localization** is a special kind of left exact [[localization of an (∞,1)-category]]: 

a topological localization of an [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$ is precsisely a localization at [[Cech cover]]s for a given [[Grothendieck topology]] on $C$, yielding the corresponding [[(∞,1)-topos]] [[(∞,1)-category of (∞,1)-sheaves|of (∞,1)-sheaves]].

$$
  Sh_{(\infty,1)}(C) \hookrightarrow PSh_{(\infty,1)}(C)
$$

and in fact equivalence classes of such topological localizations are in bijection with [[Grothendieck topology|Grothendieck topologies]] on $C$.

Notice that in general a topological localization is not a [[hypercomplete (∞,1)-topos]]. That in general requires localization further at [[hypercover]]s.



## Definition

+-- {: .un_def }
###### Definition

Call a morphism $f : X \to Y$ in an [[(∞,1)-category]] $C$ a **monomorphism** if it is a [[n-truncated object of an (infinity,1)-category|(-1)-truncated object]] in the [[overcategory]] $X_{/Y}$.

Equivalently: if for every object $A \in C$ the induced morphism in the [[homotopy category]] of [[∞-groupoid]]s

$$
   C(A,f) : C(A,X) \to C(A,Y)
$$

exhibits $C(A,X)$ as a [[direct sum|direct summand]] of $C(A,Y)$.

=--

This is [[Higher Topos Theory|HTT, p. 460]]

+-- {: .un_example }
###### Example

The standard example to keep in mind is that of a [[Cech nerve]]. In fact, as the propositions below will imply, this is for the purposes of localizations of an [[(∞,1)-category of (∞,1)-presheaves]] the _only_ kind of example.

Let [[Diff]] be the category of smooth manifolds and $PSh_{(\infty,1)}(Diff)$ the [[(∞,1)-category of (∞,1)-presheaves]] on $Diff$, which may be modeled by the global [[model structure on simplicial presheaves]] on $Diff$.

For $X \in Diff$ a [[manifold]], let $\{U_i \hookrightarrow X\}$ be an open cover. Let $Y(U)$ be the [[Cech nerve]] of this cover, the [[simplicial object]] of presheaves

$$
  Y(U) = 
  \left(
     \cdots
     \coprod_{i j} U_i \cap U_j  \stackrel{\to}{\to}\coprod_{i} U_i   
  \right)
  \,.
$$

which we may regard as a [[simplicial presheaf]] and hence as an object of $PSh_{(\infty,1)}(Diff)$.

Then for $V$ any other manifold, we have that

$$
  PSh_{(\infty,1)}(V, Y(U))
$$

is the [[∞-groupoid]] whose

* objects are maps $V \to X$ that factor through one of the $U_i$;

* there is a unique morphism between two such maps precisely if they factor through a double intersection $U_{i} \cap U_j$;

* and so on.

In the [[homotopy category of an (∞,1)-category|homtoopy category]] of [[∞-groupoid]]s, this is equivalent to the [[0-groupoid]]/[[set]] of those maps $V \to X$ that factor through one of the $U_i$. This is a subset the 0-groupoid of $PSh_{(\infty)}(V,X)$, hence a [[direct sum]]mand.

=--

+-- {: .un_def }
###### Definition
**topological localization**

Let $C$ be a [[presentable (∞,1)-category]] and 

$$
  D \hookrightarrow C
$$

a [[localization of an (∞,1)-category]] with respect to a [[localization of an (∞,1)-category|strongly saturated class]] $\bar S$ of morphisms in $C$ such that

* there is a subclass $S \subset \bar S$ of monomorphisms that generates $\bar S$;

* under [[pullback]] in $C$ elements in $\bar S$ pull back to elements in $\bar S$.

Then $D \hookrightarrow C$ is called a **topological localization** of $C$.

=--

This is [[Higher Topos Theory|HTT, def. 6.2.1.5]]


+-- {: .un_def }
###### Definition
**$(\infty,1)$-sheaves**

Let $C$ be a [[small category|small]] [[(∞,1)-category]] with a [[Grothendieck topology]]. 

Let $S$ be the collection of all monomorphisms $U \to Y(c)$ that correspond to covering [[sieve]]s in $C$. Say an object $C \in PSh_{(\infty,1)}(C)$ in the [[(∞,1)-category of (∞,1)-presheaves]] on $C$ is an **$(\infty,1)$-sheaf** if it is an $S$-[[local object]] (i.e. if it satisfies [[descent]] along all morphisms $U \to Y(c)$ coming from covering sieves).

Write

$$
  Sh_{(\infty,1)}(C)  \hookrightarrow PSh_{(\infty,1)}(X)
$$

for the full subcategory spanned by $(\infty,1)$-sheaves.

=--

This is [[Higher Topos Theory|HTT, def. 6.2.2.6]]

## Properties

+-- {: .un_prop }
###### Proposition
**sheaves form a topological localization**

Let $C$ be a small [[(∞,1)-category]] with a [[Grothendieck topology]]. Then the inclusion

$$
  Sh_{(\infty,1)}(C)  \hookrightarrow PSh_{(\infty,1)}(X)
$$

from above is a topological localization

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, Lemma 6.2.2.7]]

=--

+-- {: .un_prop }
###### Proposition
**all topological localizations arise this way**

Let $C$ be a small [[(∞,1)-category]]. There is a bijection between [[Grothendieck topology|Grothendieck topologies]] on $X$ and equivalence classes of topological localizations of $PSh_{(\infty,1)}(C)$.


=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 6.2.2.9]]

=--


+-- {: .un_prop }
###### Proposition
**(localizations of presentable $n$-categories are topological)**

Let $C$ be a [[presentable (∞,1)-category|presentable]] [[(n,r)-category|(n,1)-category]] for $n \in \mathbb{N}$ finite with [[universal colimits]]. Then every left exact [[localization of an (∞,1)-category|localization of]] $C$ is a topological localization

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 6.4.3.9]].

=--

This means that every [[(n,1)-topos]] of $n$-sheaves is a localization at [[Cech nerve]]s of covers.

**Remark** Notice in this context the statement found for instance in 

* [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/)) 

that a [[simplicial presheaf]] that satisfies [[descent]] on all [[Cech cover]]s already satisfies descent for all _bounded_ hypercovers. If the simplicial presheaf is $n$-truncated for some $n$, then it won't "see" $k$-bounded hypercovers for large enough $k$ anyway, and hence it follows that truncated simplicial presheaces that satisfy Cech descent already satisfy hyperdescent. 

This is in line with the above statement that for $n$-toposes with finite $n$ there is no distinction between Cech descent and hyperdescent. The distinction becomes visible only for untruncated $\infty$-presheaves.