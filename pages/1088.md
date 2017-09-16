WARNING: this entry is incomplete and incoherent -- to be continued tomorrow...

#Idea#

For $S$ a [[category]] equipped with a [[Grothendieck topology]], i.e. a $S$ [[site]], there is a collection of [[morphism]]s in the [[presheaf]] category $[S^{op}, Set]$ -- called the _local isomorphisms_ -- such that the [[category of sheaves]] $Sh(S)$ on $S$ is [[equivalence|equivalent]] to the [[homotopy category]] of $[S^{op}, Set]$  with respect to local isomorphisms as [[category with weak equivalences|weak equivalences]].

#Definition#

Recall that a collection of [[local epimorphism]]s on $[S^{op}, Set]$ is equivalent to a [[Grothendieck topology]] on $S$.

A **local monomorphism** with respect to this topology is a morphism $f : A \to B$ in $[S^{op}, Set]$ such that the canonical morphism $A \to A \times_B A$ is a [[local epimorphism]].

A **local isomorphism** with respect to a Grothendieck topology is a morphism in $[S^{op}, Set]$ that is both a [[local epimorphism]] as well as a local monomorphism in the above sense.

#Properties#

* Local isomorphisms form a left saturated [[multiplicative system]].


# Sheafification #

Write $Ho := Ho_{[S^{op}, Set]}$ for the [[homotopy category]] induced by letting weak equivalences be the local isomorphisms with respect to a Grothendieck topology on $S$. 

Let $F \in [S^{op}, Set]$ be a [[presheaf]] on $S$. Its **sheafification** is the presheaf

$$
  \bar F : U \mapsto Hom_{Ho}(Y(U), F)
  \,,
$$

where $Y$ denotes the [[Yoneda embedding]]. This can be computed explciitly as

$$
  \bar F(U) 
  =
   \colim_{ \hat U \stackrel{local iso}{\to} U } 
   Hom_{[S^{op}, Set]}(\hat U, F)
  \,,
$$


#Characterization and relation to sieves#

(...)




#References#

Sections 16 and 17 of

* Kashiwara-Schapira, [[Categories and Sheaves]]