A regular space is a [[topological space]] (or variation) that has, in a certain sense, enough closed subsets.  The condition of regularity is one the [[separation axioms]] satsified by every [[metric space]] (in this case, by every pseudometric space).


## Definitions

Fix a [[topological space]] $X$.


The classical definition is this: that if a point and a closed set are disjoint, then they are separated by neighbourhoods.  In detail, this means:
+-- {: .num_defn #classical}
###### Definition
Given any point $a$ and closed set $F$, if $a \notin F$, then there exist a neighbourhood $V$ of $a$ and a neighbourhood $G$ of $F$ such that $V \cap G$ is empty.
=--

In many contexts, it is more helpful to change perspective, from a closed set that $a$ does *not* belong to, to an open set that $a$ *does* belong to.  Then the definition reads:
+-- {: .num_defn #constructive}
###### Definition
Given any point $a$ and neighbourhood $U$ of $a$, there exist a neighbourhood $V$ of $a$ and an open set $G$ such that $V \cap G = \empty$ but $U \cup G = X$.
=--
You can think of $V$ as being half the size of $U$, with $G$ the exterior of $V$.  (In a [[metric space]], or even in a [[uniform space]], this can be made into a proof.)

If we apply the regularity condition twice, then we get what at first might appear to be a stronger result:
+-- {: .num_defn #closed}
###### Definition
Given any point $a$ and neighbourhood $U$ of $a$, there exist a neighbourhood $W$ of $a$ and an open set $G$ such that $Cl(W) \cap Cl(G) = \empty$ but $U \cup G = X$ (where $Cl$ indicates topological closure).
=--
+-- {: .proof}
###### Proof of equivalence
Find $V$ and $G$ as above.  Now apply the regularity axiom to $x$ and the interior $Int(V)$ of $V$ to get $W$ and $H$.  We have $W \cap H = \empty$, so $Cl(W) \cap H = \empty$ since $H$ is open.  Since $Int(V) \cup H = X$, we get $Cl(W) \subseteq Int(V)$.  Meanwhile, $V \cap G = \empty$, so $Int(V) \cap Cl(G) = \empty$.  Therefore, $Cl(W) \cap Cl(G) = \empty$.  (We already have that $U \cup G = X$.)
=--
In terms of the classical language of separation axioms, this says that $x$ and $F$ are separated by *closed* neighbourhoods.

Sometimes one includes in the definition that a regular space must be $T_0$:
+-- {: .num_defn #T0}
###### Definition
(In addition to any of the above.)
Given any two points, if each neighbourhood of either is a neighbourhood of the other, then they are equal.
=--
Other authors use the weaker definition above but call a regular $T_0$ space a __$T_3$ space__, but then that term is also used for a (merely) regular space.

We have
+-- {: .num_theorem #Hausdorff}
###### Theorem
Every $T_3$ space is [[Hausdorff space|Hausdorff]].
=--
+-- {: .proof}
###### Proof
...
=--
In light of this, a less ambiguous term for a $T_3$ space is a __regular Hausdorff space__.


... [[locales]] ...


In [[constructive mathematics]], Definition \ref{constructive} is good; then everything else follows without change, except for the equivalence with \ref{classical}.  Even then, the classical separation axioms hold for a regular space; they just are not sufficient.


## ...