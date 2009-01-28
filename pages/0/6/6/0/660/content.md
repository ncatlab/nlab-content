##Idea##

A $cat^2$-group is a [[double groupoid]] (or, equivalently, [[double category]]) [[internal category|internal]] to the category [[Grp]] of groups.


##Discussion##
$Cat^2$ groups are equivalent to [[crossed square]]s. 

* Note that to calculate a [[colimit]] it is better to work with crossed squares, but to prove something is a colimit, it is better to work with $cat^2$-groups. 

* $Cat^2$ groups are a special case of [[cat-n-group]]s, which are ... $n$-fold groupoids in the category of groups.

* The use of $n$-fold groupoids in [[Grp]] rather than $n+1$ groupoids means that information contained in the \model' is more 'spread out', but is often **repeated** in different forms in different parts of the model. 

* The homotopical example found by Loday can be seen as follows. Let $(X;A,B)$ be a pointed triad, so that $A,B \subseteq X$. Let $\Phi$ be the space of maps $I^3 \to X$ which map the faces of direction 1 to the base point, the faces of direction 2 into $A$ and the faces of direction 3 into $B$. Let $G= \Pi'(X;A,B)= \pi_1(\Phi,*)$. The $G$ is certainly a group. The surprise is that the compositions of cubes in directions 2 and 3 are inherited by $G$ to make it a cat^2-group. The equivalent crossed square is the classical one involving triad homotopy groups. 

Loday gives the more general description in terms of squares of spaces and the fundamental groups of the associated fibration sequences, and the proof of the cat^2-structure uses bisimplicial methods. This generalises nicely to the n-fold case. 

It is unclear how best to deal with the many pointed case! 


##References##

* J.-L. Loday,  Spaces with finitely many homotopy groups,
J.Pure Appl.  Alg., 24 (1982), 179--202.

* R. Brown and J.-L. Loday,  Van Kampen theorems for diagrams of spaces,   Topology, 26 (1987), 311 -- 337.

