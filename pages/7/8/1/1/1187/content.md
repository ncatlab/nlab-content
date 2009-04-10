#Idea#

In the category [[Top]] of [[topological space]]s one has the following equivalent definitions of when a [[topological space]] $X$ is _compact_ in that every open cover of it has a finite subcover:

$X$ is compact precisely if the [[hom-functor]] $Top(X,-) : Top \to Top$ commutes with [[filtered category|filtered]] [[colimit]]s.

Conversely, for $C$ any category and $X \in C$, the condition that $C(X,-) : C \to C$ preserves [[filtered category|filtered]] [[colimit]]s imposes  some kind of finiteness condition on $X$. For instance 

* in $C = $ [[Set]] this is the case if the set $X$ is finite;

* in $C =$ [[Grp]] this is the case if the group $X$ is finitely presented as a group.

#Definition#

The general definition has a bit of cumbersome fine print, see definition 5.3.4.5  in

* [[Jacob Lurie]], [[Higher Topos Theory]]

It becomes simpler in [[stable (infinity,1)-category|stable (infinity,1)-categoris]]:

An object $X$ in a [[stable (infinity,1)-category]] is **compact** if the $(\infty,1)$-functor

$$
  C(X,-) : C \to C
$$

commutes with all [[limit in quasi-categories|colimit]].


#Remarks#

* For more discussion of the relevance of compact objects, see also [[geometric infinity-function theory]].