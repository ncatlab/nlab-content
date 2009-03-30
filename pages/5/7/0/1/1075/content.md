#Idea#

For $S$ a [[category]], a 
system of _local epimorphisms_ is a system of [[morphism]]s in the [[presheaf]] category $[S^{op}, Set]$ that have the closure properties expected of [[epimorphism]]s under [[composition]] and under [[pullback]].

A specification of a system of _local epimorphisms_ 
is equivalent to giving a [[Grothendieck topology]]
and hence the structure of a [[site]] on $S$.

A collection of local epimorphisms 
form a [[multiplicative system]]
of morphisms in the [[presheaf]] category
and the corresponding [[homotopy category]]
is the corresponding category of [[sheaf|sheaves]].

One useful aspect of local epimorphisms is that the [[local isomorphism]]s among them form a [[mutliplicative system]]. This allows to characterize the category of [[sheaf|sheaves]] on $S$ as the [[homotopy category]] with respect to local isomorphisms.


#Definition#

Let $S$ be a [[category]] equipped with a 
[[Grothendieck topology]], hence in particular
with a collection of covering [[sieve]]s
for each object $U \in S$.

For a morphism $f : A \to Y(U)$ in the [[presheaf]] category 
$[S^{op},Set]$ with $U \in S$ and $Y : S \to [S^{op}, Set]$ the
[[Yoneda embedding]], let $sieve_A \subset Y(U) \in [S^{op}, Set]$ be the
[[sieve]]  at $U$ 
$$
  sieve_f : V \mapsto \{ h : V \to U \in S \;|\; Y(h) = Y(V) \stackrel{\exists}{\to} A \to Y(U)\}
$$
which assigns to $V$ all morphisms from $V$ to $U$ that factor through $f$.

The morphism $f : A \to Y(U)$ is a **local epimorphism** if
$sieve_f$ is a covering sieve.

An arbitrary morphism $f : A \to B$ in $[S^{op}, A]$ is a 
**local epimorphism** if for every $V \in S$ and 
every $Y(V) \to B$ the morphism 
$A \times_{Y(U)} Y(V) \to Y(V)$
is a local epimorphism as above.


#References#

Section 16 of

* Kashiwara-Schapira,  [[Categories and Sheaves]]