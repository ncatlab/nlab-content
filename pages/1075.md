#Idea#

For $S$ a [[category]], a 
system of _local epimorphisms_ is a system of [[morphism]]s in the [[presheaf]] category $[S^{op}, Set]$ that has the closure properties expected of [[epimorphism]]s under [[composition]] and under [[pullback]].

A specification of a system of _local epimorphisms_ 
is equivalent to giving a [[Grothendieck topology]]
and hence the structure of a [[site]] on $S$.

Moreover the [[local isomorphism]]s among the local epimorphisms constitute a [[multiplicative system]] which eqips $[S^{op}, Set]$ with the structure of a [[category with weak equivalences]]. The corresponding [[homotopy category]] is the category of [[sheaf|sheaves]] on the site $S$.

#Definition#

Let $S$ be a [[category]]. A system of **local epimorphisms** on the [[presheaf]] category $[S^{op}, Set]$ is a collection of morphisms satisfying the following axioms

**LE1** every epimorphism in $[S^{op}, Set]$ is a local epimorphism;

**LE2** the composite of two local epimorphisms is a local epimorphism;

**LE3** if the composite $A_1 \stackrel{u}{\to} A_2 \stackrel{v}{\to} A_3$ is a local epimorphism, then so is $v$;

**LE4** a morphism $U : A \to B$ is a local epimorphism precisely if for all $U \in S$ and morphisms $Y(U) \to B$ the [[pullback]] morphism $A \times_B U \to U$ is a local epimorphism.

#Relation to sieves#

The specification of a system of local epimorphisms is equivalent to a system of [[Grothendieck topology|Grothendieck covering]] [[sieve]]s.

To see this, translate between local epimorphisms to sieves as follows.

##From covering sieves to local epimorphisms##

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


##From local epimorphisms to covering sieves ##

Conversely, assume a system of local epimorphisms is given. 

Declare a [[sieve]] $F$ at $U$ to be a covering sieve precisely if the inclusion morphism $F \hookrightarrow U$ is a local epimorphism. Then this defines  Grothendieck topology enoced by the collection of local epimorphisms




#References#

Section 16 of

* Kashiwara-Schapira,  [[Categories and Sheaves]]