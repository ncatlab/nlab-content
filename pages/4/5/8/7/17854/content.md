
# Apartness spaces
* table of contents
{: toc}

## Idea

An *apartness space* is a set equipped with an "apartness relation" that distinguishes between pairs of points or sets.  They are particularly interesting in [[constructive mathematics]]; in [[classical mathematics]] they tend to be equivalent to better-known definitions expressed in terms of "closeness" rather than "apartness".


## Definitions

There are actually several different notions of "apartness space" depending on whether the objects being compared on each side are points or sets.

* A _point--point apartness space_ is a set $X$ equipped with an _[[apartness relation]]_, usually written $x # y$ on elements $x,y\in X$.  Sometimes it is required to be [[tight relation|tight]], or to be only an [[inequality relation]].

* A __point--set apartness space__ is a set $X$ equipped with a relation $x \bowtie A$ between points $x\in X$ and subsets $A\subseteq X$, satisfying appropriate axioms.  In [[classical mathematics]], these axioms are obtained by [[contrapositive|contraposition]] from the definition of a [[topological space]] in terms of a [[exact functor|right exact]] [[Moore closure]] operator, so that point--set apartness spaces are equivalent to topological spaces.  In [[constructive mathematics]] ... well, keep reading.

* A _set--set apartness space_ is a set $X$ equipped with a relation $A\bowtie B$ between [[subsets]] $A,B\subseteq X$, satisfying appropriate axioms.  A set--set apartness space is one of the ways to describe the [[classical mathematics|classical]] notion of a _[[proximity space]]_.  In [[constructive mathematics]], the definition of a proximity space in terms of $\bowtie$ can be taken as a definition of a set--set apartness space.

* A _uniform apartness space_ is a set $X$ equipped with a collection of "co-[[entourages]]", each giving a different notion of when two points are apart, satisfying appropriate axioms.  In [[classical mathematics]], the co-entourages are exactly the [[complements]] of the entourages of a [[uniform space]], and the same is true constructively if the space is [[uniformly regular]].

Since point--point apartness spaces are described at [[apartness relation]], set--set apartness spaces at [[proximity space]], and uniform apartness spaces at [[uniformly regular space]], the rest of this page will be about point--set apartness spaces.


## Point--set apartness spaces

+-- {: .un_defn}
###### Definition
An __apartness space__ is a set $X$ equipped with a relation $\bowtie$ between points $x\in X$ and subsets $A\subseteq X$ such that

1. $x\bowtie \emptyset$ for any $x$.
2. if $x\bowtie A$, then $x\neq y$ for all $y\in A$.
3. $x\bowtie (A\cup B)$ iff $x\bowtie A$ and $x\bowtie B$.
4. If $x\bowtie A$, then $x \bowtie \{ y \mid \forall z, (z\bowtie A \to z\neq y) \}$.
=--

The relation $x\bowtie A$ should be regarded as a "positive" way of saying that $x$ does not belong to the [[closure]] of $A$, i.e. $x\notin \overline{A}$.  Under this interpretation, the above axioms contrapose to become

1. $\overline{\emptyset} = \emptyset$.
2. If $x\in A$, then $x\in \overline{A}$, i.e. $A\subseteq \overline{A}$.
3. $\overline{A} \cup \overline{B} = \overline{A\cup B}$ (and in particular $(A\subseteq B) \to (\overline{A}\subseteq \overline{B})$).
4. If $B\subseteq \overline{A}$ and $x\in \overline{B}$, then $x\in\overline{A}$, i.e. $\overline{\overline{A}} = \overline{A}$.

which are precisely the axioms of a [[topology]] expressed in terms of a closure operator.  In constructive mathematics, of course, the law of contraposition does not hold.

The axiom $x\bowtie \emptyset$ is almost unnecessary, since the last axiom ensures that if $x\bowtie A$ for any set $A$ then $x\bowtie\emptyset$.  In particular, this is the case if $X$ is $T_1$ (see below) and for any $x\in X$ there is a $y\in X$ with $x\neq y$.

The above definition is almost exactly that of a "pre-apartness" from [BV11](#BV11).  The differences are (1) they require $X$ to be [[inhabited set|inhabited]] (which category-theoretically is wrong-headed, since it excludes the [[initial object]]), and (2) they assume that $X$ is given with an ambient [[inequality relation]] that is referred to by the symbol $\neq$ in axioms 2 and 4.  (If $\neq$ is the [[denial inequality]], then these axioms can be written more simply as "if $x\bowtie A$ then $x\notin A$" and "if $x\bowtie A$ then $x\bowtie \{ y \mid \neg(y\bowtie A) \}$".)  Note that if the space is $T_1$ (see below) then this ambient inequality is definable in terms of $\bowtie$ as $x\bowtie \{y\}$.  For an "apartness", [BV11](#BV11) also require comparability (see below).

Axiom 4 is phrased in [BV11](#BV11) as "if $\forall x, (x\bowtie A \Rightarrow (\forall y\in B, x\neq y))$, then $\forall x, (x\bowtie A \Rightarrow x\bowtie B)$.  This is equivalent to our version, since $B = \{ y \mid \forall z, (z\bowtie A \to z\neq y) \}$ is the largest set $B$ satisfying $\forall x, (x\bowtie A \Rightarrow (\forall y\in B, x\neq y))$.

The earlier paper [BSV02](#BSV02) omits the axiom $x\bowtie \emptyset$, and phrases axiom 2 with the denial inequality but axiom 4 with an ambient inequality --- although these are probably oversights --- and requires $T_1$ as part of the definition too (see below).  An earlier, more predicative presentation of "apartness spaces" can be found in [Waaldijk](#FW96).


## Separation properties

Any apartness space comes with an [[irreflexive relation]] $\nleq$ defined by $x \nleq y$ iff $x \bowtie \{y\}$.  This is a positive version of the negation of the [[specialization order]].  Just as a topological space is called $T_1$ (see [[separation axioms]]) if its specialization order is discrete, i.e. $(x\le y) \to (x=y)$, an apartness space is called **$T_1$** if the contrapositive of this holds, i.e. $(x\neq y) \to (x \bowtie \{y\})$.

If $X$ is given with a [[apartness relation]] or [[inequality relation]] other than the [[denial inequality]], then we can use it here as well as in axioms 2 and 4 of an apartness space.  Note that axiom 2 implies the converse $(x\bowtie \{y\}) \to (x\neq y)$, so that in a $T_1$ apartness space the ambient inequality can be defined in terms of $\bowtie$.  In this case, axiom 2 should be stated in terms of the denial inequality (thereby asserting that the relation $x\bowtie \{y\}$ is [[irreflexive]]).

If one wants the relation $x\bowtie \{y\}$ to be [[symmetric relation|symmetric]] and thus an "[[inequality relation]]" one needs to assert this separately.  An apartness space with this property is naturally called **$R_0$**, just as a topological space is called $R_0$ if its specialization order is symmetric (see [[separation axioms]]).

However, stating axiom 4 in terms of the $\bowtie$-derived inequality is weaker, even in [[classical mathematics]], than stating it in terms of the denial inequality.  For instance, if $X = \{x,y,z\}$ with the only nonempty apartness relations $x\bowtie \{z\}$ and $z\bowtie \{x\}$, then axiom 4 for the denial inequality fails for $A=\{z\}$, since $\{ y \mid \neg(y\bowtie A)\} = \{y,z\}$ which is not apart from $x$; but stated in terms of the $\bowtie$-derived inequality it holds, since $\{ v \mid \forall u, (u\bowtie A \Rightarrow u \bowtie \{v\})\} = \{z\}$.  This is a [[pretopological space]] that is not a topological space; thus only axiom 4 with the denial inequality (or at least a [[tight inequality]], which classically becomes equivalent to denial) gives a notion of point-set apartness space that reduces classically to ordinary toplogical spaces.  In [BV11](#BV11), axiom 4 for the denial inequality is called the **reverse Kolmogorov property**.

An apartness space may be called **comparable** (nonce definition on this page) if $x\bowtie A$ implies $(x\neq y) \vee (y\bowtie A)$ for any $y$, where $\neq$ might also be a given apartness on $X$.  This condition is classically trivial, and generalizes the [[comparison]] axiom on a point--point [[apartness relation]].  In particular, if $\neq$ denotes the relation $\nleq$ defined above, then this property implies that $\nleq$ is a [[comparison]], and hence (if the space is also $R_0$, so it is symmetric) an [[apartness relation]].  It is also related topologically to Penon's definition of intrinsic [[open subset]] in [[synthetic topology]] and to the natural topology on a [[point-point apartness space]], and can be viewed as a very weak version of [[regular space|regularity]].

An apartness space is **[[locally decomposable space|locally decomposable]]** if whenever $x\bowtie A$, there exists a set $B$ such that $x\bowtie B$ and every $y$ satisfies either $y\bowtie A$ or $y\in B$.  This condition is also classically trivial: take $B = \{ y \mid \neg(y\bowtie A) \}$.  It implies comparability (for $\neq$ the [[denial inequality]]).


## Relation to topological spaces

If $X$ is a topological space, we define $x\bowtie A$ if there is a neighborhood of $x$ disjoint from $A$, or equivalently if the complement of $A$ is a neighborhood of $x$.  This makes $X$ an apartness space.  Only the last axiom is somewhat nontrivial: if $x\in U$ with $U$ open and $U\cap A = \emptyset$, and $\forall y, (y\bowtie A \to y\notin B)$, then since $(y\in U) \Rightarrow (y\bowtie A)$ we have $U\cap B = \emptyset$ too, so $x\bowtie B$.

Conversely, if $X$ is an apartness space, define $U\subseteq X$ to be a neighborhood of $x\in U$ if there is a set $A$ such that $x\bowtie A$ and $\forall y, (y\bowtie A \Rightarrow y\in U)$.  This makes $X$ a topological space.  Again the nontrivial part is the "transitivity" of neighborhoods, i.e. that if $U$ is a neighborhood of $x$ then so is $\{ y \mid U$ is a neighborhood of $y \}$.  To see this, if $x\bowtie A$ and $\forall y, (y\bowtie A \Rightarrow y\in U)$, then $U$ is a neighborhood of any point $y$ with $y\bowtie A$, so it suffices to show that $\{ y \mid y\bowtie A\}$ is a neighborhood of $x$; but this is obvious.

If we order the topologies on $X$ by $\tau_1 \le \tau_2$ if $\tau_2 \subseteq \tau_1$ (i.e. $\tau_1$ is finer than $\tau_2$), and the apartnesses by $\bowtie_1 \le \bowtie_2$ if $(x\bowtie_2 A) \Rightarrow (x\bowtie_1 A)$, then these constructions define [[monotone functions]] $\tau \mapsto \bowtie_\tau$ and $\bowtie \mapsto \tau_\bowtie$ respectively.  Moreover, we have:

+-- {: .un_theorem}
###### Theorem
The above functions exhibit the poset of apartnesses on $X$ as a [[reflective subcategory|reflective]] sub-poset of the poset of topologies on $X$: we have $\tau \le \tau_{\bowtie_\tau}$ and $\bowtie_{\tau_\bowtie} = \bowtie$.
=--
+-- {: .proof}
###### Proof
For the former inequality, if $U$ is open in $\tau_{\bowtie_\tau}$, then for every $x\in U$ there is a set $A$ such that $x\bowtie_\tau A$ and $\forall y, (y\bowtie_\tau A \Rightarrow y\in U)$.  Since $x\bowtie_\tau A$, there is an open set $V$ with $x\in V$ and $V\cap A = \emptyset$.  But then every $y\in V$ satisfies $y\bowtie_\tau A$, hence $y\in U$; so $V\subseteq U$.  Thus $U$ is open.

For the latter equation, if $x\bowtie A$, then to show $x \bowtie_{\tau_\bowtie} A$ we must construct an open set $U\in \tau_\bowtie$ with $x\in U$ and $U\cap A = \emptyset$; but it suffices to take $U = \{ y \mid y\bowtie A \}$.  Conversely, if $x \bowtie_{\tau_\bowtie} A$, then there is an open set $U\in \tau_\bowtie$ with $x\in U$ and $U\cap A = \emptyset$.  By definition, $U\in \tau_\bowtie$ and $x\in U$ mean there is a set $B$ with $x\bowtie B$ and $\forall y, (y\bowtie B \Rightarrow y\in U)$.  And by the last axiom of an apartness space, to show $x\bowtie A$ it suffices to show $\forall y, (y\bowtie B \to y\notin A)$; but this follows since $y\bowtie B \Rightarrow y\in U$ and $U\cap A = \emptyset$.
=--

In other words, an apartness space can be regarded as a well-behaved kind of topological space: one in which for every open neighborhood $U$ of a point $x$ there is a set $A$ and an open neighborhood $V$ of $x$ such that $V\cap A = \emptyset$ and $U$ contains the interior of the complement of $A$.  Note that $V$ is then in the interior of the complement of $A$, and if $x$ is in the interior of the complement of $A$ then the latter is such a $V$.  Thus, the condition can equivalently be phrased as: for every open neighborhood $U$ of $x$, there is a set $A$ such that $x \in int(\neg A) \subseteq U$.  In other words, the interiors of complements form a base for the topology.  In [Bridges et. al.](#BSV) this condition is called being **topologically consistent**.

A sufficient condition for topological consistency is local decomposability.  This was defined above for apartness spaces; more generally, a topological space is said to be [[locally decomposable space|locally decomposable]] if for every open neighborhood $U$ of $x$ there is an open neighborhood $V$ of $x$ such that $U \cup \neg V = X$, i.e. every $y\in X$ satisfies $(y\in U)\vee (y\notin V)$.  This implies that $x\in int(\neg\neg V) \subseteq \neg\neg V \subseteq U$, giving topological consistency.  (Of course, in classical mathematics every space is locally decomposable.)

In contrast to the above theorem, it is not quite justified to say that the *category* of apartness spaces is a subcategory of the category of topological ones.  It is most natural to say that a function $f:X\to Y$ between apartness spaces is **continuous** if for all $x\in X$ and $A\subseteq X$, if $f(x) \bowtie f(A)$ then $x\bowtie A$.  It is true that if $X$ and $Y$ are topological spaces and $f$ is topologically continuous, then it is apartness-continuous in this sense for the induced apartnesses.  For if $f(x)\bowtie f(A)$, then $f(x) \in U$ for some open set $U$ disjoint from $f(A)$; topological continuity of $f$ then gives that $f^{-1}(U)$ is an open set containing $x$ and disjoint from $A$, so that $x\bowtie A$.  Thus we do have a functor $Top \to Apart$.  

However, a continuous map between apartness spaces in the above sense apparently need not be continuous for the induced topologies; but this is true if $Y$ is locally decomposable.  For if $U\subseteq Y$ is open and $x\in f^{-1}(U)$, we have a set $A\subseteq Y$ such that $f(x)\bowtie A$ and $y\bowtie A$ implies $y\in U$, and by local decomposability gives a $B\subseteq Y$ such that $f(x)\bowtie B$ and every $y$ satisfies either $y\bowtie A$ or $y\in B$.  Let $C = f^{-1}(B)$; if $x'\bowtie C$, we have $x'\notin C$ and hence $f(x')\notin B$, so $f(x')\bowtie A$ and thus $f(x')\in U$ and $x'\in f^{-1}(U)$.  Moreover, since $f(x)\bowtie B$ we have $x\bowtie C$ by apartness-continuity.  Thus, $f^{-1}(U)$ is open.

Thus, the category of locally decomposable apartness spaces is equivalent to the category of locally decomposable topological spaces.


## References

Notions of "apartness space" based on a presentation in terms of basic opens, somewhat akin to [[formal topology]], were developed in:

* [[Frank Waaldijk]], *Modern intuitionistic topology*, Ph.D. thesis, 1996, [link](http://www.fwaaldijk.nl/modern%20intuitionistic%20topology.pdf)
 {#FW96}

* [[Frank Waaldijk]], *Natural topology*, 2011, 2012, [arxiv](https://arxiv.org/abs/1210.6288)

The above definition in terms of an apartness relation between points and subsets is slightly adapted from the version given in:

* [[Douglas Bridges]], Peter Schuster, and Luminita Vita, *Apartness, Topology, and Uniformity: a Constructive View*, 2002,  [doi](http://dx.doi.org/10.1002/1521-3870%28200210%2948:1%2B%3C16::AID-MALQ16%3E3.0.CO;2-7)
 {#BSV02}

* [[Douglas Bridges]] and Luminita Vita, *Apartness and Uniformity: A Constructive Development*. 2011, [link](http://link.springer.com/book/10.1007%2F978-3-642-22415-7)
 {#BV11}


[[!redirects apartness space]]
[[!redirects apartness spaces]]

[[!redirects point-set apartness space]]
[[!redirects point-set apartness spaces]]
[[!redirects point–set apartness space]]
[[!redirects point–set apartness spaces]]
[[!redirects point--set apartness space]]
[[!redirects point--set apartness spaces]]
[[!redirects point-set apartness structure]]
[[!redirects point-set apartness structures]]
[[!redirects point–set apartness structure]]
[[!redirects point–set apartness structures]]
[[!redirects point--set apartness structure]]
[[!redirects point--set apartness structures]]
[[!redirects point-set apartness relation]]
[[!redirects point-set apartness relations]]
[[!redirects point–set apartness relation]]
[[!redirects point–set apartness relations]]
[[!redirects point--set apartness relation]]
[[!redirects point--set apartness relations]]
