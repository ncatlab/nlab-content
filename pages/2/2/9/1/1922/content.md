A regular space is a [[topological space]] (or variation) that has, in a certain sense, enough regular open subsets.  The condition of regularity is one the [[separation axioms]] satsified by every [[metric space]] (in this case, by every pseudometric space).


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
+-- {: .un_defn}
###### Definition (of $T_0$)
Given any two points, if each neighbourhood of either is a neighbourhood of the other, then they are equal.
=--
Other authors use the weaker definition above but call a regular $T_0$ space a __$T_3$ space__, but then that term is also used for a (merely) regular space.

We have
+-- {: .un_theorem}
###### Theorem
Every $T_3$ space is [[Hausdorff space|Hausdorff]].
=--
+-- {: .proof}
###### Proof
...
=--
In light of this, a less ambiguous term for a $T_3$ space is a __regular Hausdorff space__.


It is possible to describe the regularity condition fairly simply entirely in terms of the algebra of open sets.  First notice the relevance above of the condition that $Cl(A) \subset B$ (for open $A, B$); we write $A \subset\subset B$ in that case and say that $A$ is __well inside__ $B$.  We now rewrite this condition in terms of open sets and regularity in terms of this condition.
+-- {: .num_defn #locale}
###### Definition
Given open sets $A, B$, $A \subset\subset B$ iff there exists an open set $C$ such that $A \cap C = \empty$ but $B \cap C = X$.  Then $X$ is regular iff, given any open set $U$, $U$ is the union of all of the open sets that are well inside $U$.
=--
+-- {: .proof}
###### Proof of equivalence
...
=--
This definition is suitable for [[locales]].  As the definition of a Hausdroff locale is rather more complicated, one often speaks of compact regular locales where classically one would have spoken of [[compact Hausdorff space]]s.  (The theorem that compact regular $T_0$ spaces and compact Hausdorff spaces are the same works also for locales, and every locale is $T_0$, so compact regular locales and compact Hausdorff locales are the same.)


The condition that a space $X$ be regular is related to the __regular open sets__ in $X$, that is those open sets $G$ such that $G$ is the interior of its own closure.  (In the [[Heyting algebra]] of open subsets of $X$, this means precisely that $G$ is its own [[double negation]]; this immediately generalises the concept to locales.)  Basically, we start with a neighbourhood $U$ of $x$ and reduce that to a closed neighbourhood $Cl(V)$ of $x$; then $Int(Cl(V))$ is a regular open set.

This is enough to characterise regular spaces, as follows:
+-- {: .num_defn #basis}
###### Definition
Given a neighbourhood $U$ of $x$, there is a closed neighbourhood of $x$ that is contained in $U$.  Equivalently, $x$ has a regular open neighbourhood contained in $U$.  In other words, the closed neighbourhoods of $x$, or equivalently the regular open neighbourhoods of $x$, form a local base (a base of the [[neighbourhood filter]]) at $x$.
=--
+-- {: .proof}
###### Proof of equivalence
...
=--

This suggests a slightly weaker condition, that of a __semiregular space__:
+-- {: .un_defn}
###### Definition (of semiregular)
The regular open sets form a basis for the topology of $X$.
=--


In [[constructive mathematics]], Definition \ref{constructive} is good; then everything else follows without change, except for the equivalence with \ref{classical}.  Even then, the classical separation axioms hold for a regular space; they just are not sufficient.