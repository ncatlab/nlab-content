#Idea#

A $cat^2$-group is a [[double groupoid]] (or, equivalently, [[double category]]) [[internal category|internal]] to the category [[Grp]] of groups. It is a $cat^1$-object in the category of $cat^1$-groups. It is a group with two _independent_ $cat^1$-group structures.

In the same 'mode' as the detailed algebraic definition of [[cat-1-group]] we have the following:

#Algebraic definition#

A **$cat^2$-group** is a quintuple, $(G,s_1,s_2, t_1,t_2)$, where $G$ is a [[group]] and $s_i,t_i$, $i = 1,2$, are [[endomorphism]]s of $G$ satisfying conditions

1. $s_i t_i = t_i$ and $t_i s_i = s_i$, for $i = 1,2$ whilst $s_i s_j = s_j s_i$, $t_i t_j = t_j t_i$ and $s_i t_j = t_j s_i$ for $i \neq j$;
1. $[Ker\,s_i, \,Ker\,t_i ] = 1$, for $i = 1,2$.

#Remarks#

$cat^2$-groups are equivalent to [[crossed square]]s. 

* Note that to calculate a [[colimit]] it is better to work with crossed squares, but to prove something is a colimit, it is better to work with $cat^2$-groups. 

* $cat^2$-groups are a special case of [[cat-n-group|cat-n-groups]], which are $n$-[[n-fold category|fold groupoids]] in the $Grp$.

* The use of $n$-fold groupoids in $Grp$ rather than $(n+1)$-[[n-groupoid|groupoids]] means that information contained in the 'model' is more 'spread out', but is often *repeated* in different forms in different parts of the model.

* The homotopical example found by Loday can be seen as follows. Let $(X;A,B)$ be a pointed triad, so that $A,B \subseteq X$. Let $\Phi$ be the space of maps $I^3 \to X$ which map the faces of direction $1$ to the base point, the faces of direction $2$ into $A$ and the faces of direction $3$ into $B$. Let $G = \Pi'(X;A,B)= \pi_1(\Phi,*)$. Then $G$ is certainly a group. The surprise is that the compositions of cubes in directions $2$ and $3$ are inherited by $G$ to make it a $cat^2$-group. The equivalent [[crossed square]] is the classical one $\Pi(X;A,B)$ involving triad homotopy groups.

Loday gives the more general description in terms of squares of spaces and the [[fundamental group]]s of the associated fibration sequences, and the proof of the $cat^2$-structure uses bisimplicial methods. This generalises nicely to the $n$-fold case.

It is not completely clear how best to deal with the many-pointed case, but working within categories of groupoids with a given set, $O$,  of objects is one possibility. There are then change of 'object' functors between the categories, leading to a [[fibered category]] situation.

#References#

* J.-L. Loday,  Spaces with finitely many homotopy groups,
J.Pure Appl.  Alg., 24 (1982), 179&#8211;202.

* R. Brown and J.-L. Loday,  Van Kampen theorems for diagrams of spaces,   Topology, 26 (1987), 311&#8211;337.


[[!redirects cat 2-group]]