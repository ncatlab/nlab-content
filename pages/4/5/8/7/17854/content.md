
# Apartness spaces
* table of contents
{: toc}

## Idea

An *apartness space* is a set equipped with an "apartness relation" that distinguishes between pairs of points or sets.  They are particularly interesting in [[constructive mathematics]]; in [[classical mathematics]] they tend to be equivalent to better-known definitions expressed in terms of "closeness" rather than "apartness".


## Definitions

There are actually several different notions of "apartness space" depending on whether the objects being compared on each side are points or sets.

* A _point--point apartness space_ is a set $X$ equipped with an _[[apartness relation]]_, usually written $x # y$ on elements $x,y\in X$.  Sometimes it is required to be [[tight relation|tight]], or to be only an [[inequality relation]].

* A _set--set apartness space_ is a set $X$ equipped with a relation $A\bowtie B$ between [[subsets]] $A,B\subseteq X$, satisfying appropriate axioms.  A set--set apartness space is one of the ways to describe the [[classical mathematics|classical]] notion of a _[[proximity space]]_.  In [[constructive mathematics]], the definition of a proximity space in terms of $\bowtie$ can be taken as a definition of a set--set apartness space.

* A __point--set apartness space__ is a set $X$ equipped with a relation $x \bowtie A$ between points $x\in X$ and subsets $A\subseteq X$, satisfying appropriate axioms.  In [[classical mathematics]], these axioms are obtained by [[contrapositive|contraposition]] from the definition of a [[topological space]] in terms of a [[exact functor|right exact]] [[Moore closure]] operator, so that point--set apartness spaces are equivalent to topological spaces.  In [[constructive mathematics]] ... well, keep reading.

* A __uniform apartness space__ is a set $X$ equipped with a collection of "co-[[entourages]]", each giving a different notion of when two points are apart, satisfying appropriate axioms.  In [[classical mathematics]], the co-entourages are exactly the [[complements]] of the entourages of a [[uniform space]], and the same is true constructively if the space is [[uniformly regular]].

Since point--point apartness spaces are described at [[apartness relation]], and set--set apartness spaces at [[proximity space]], and uniform apartness spaces at [[uniformly regular space]], the rest of this page will be about point--set apartness spaces.


### Point--set apartness spaces

+-- {: .un_defn}
###### Definition
An __apartness space__ is a set $X$ equipped with a relation $\bowtie$ between points $x\in X$ and subsets $A\subseteq X$ such that

1. if $x\bowtie A$, then $x\notin A$.
2. $x\bowtie (A\cup B)$ iff $x\bowtie A$ and $x\bowtie B$.
3. $x\bowtie \emptyset$ for any $x$.
4. If $x \bowtie A$, and $\forall y, (y\bowtie A \to y\notin B)$, then $x\bowtie B$.  Equivalently, if $x\bowtie A$, then $x \bowtie \{ y \mid \neg (y\bowtie A) \}$.
=--

The relation $x\bowtie A$ should be regarded as a "positive" way of saying that $x$ does not belong to the [[closure]] of $A$, i.e. $x\notin \overline{A}$.  Under this interpretation, the above axioms contrapose to become

1. If $x\in A$, then $x\in \overline{A}$, i.e. $A\subseteq \overline{A}$.
2. $\overline{A} \cup \overline{B} = \overline{A\cup B}$ (and in particular $(A\subseteq B) \to (\overline{A}\subseteq \overline{B})$).
3. $\overline{\emptyset} = \emptyset$.
4. If $B\subseteq \overline{A}$ and $x\in \overline{B}$, then $x\in\overline{A}$, i.e. $\overline{\overline{A}} = \overline{A}$.

which are precisely the axioms of a [[topology]] expressed in terms of a closure operator.  In constructive mathematics, of course, the law of contraposition does not hold.

The axiom $x\bowtie \emptyset$ is almost unnecessary, since the last axiom ensures that if $x\bowtie A$ for any set $A$ then $x\bowtie\emptyset$.  In particular, this is the case if $X$ is $T_1$ (see below) and for any $x\in X$ there is a $y\in X$ with $x\neq y$.  [Bridges et al](#BSV) omit this axiom.

## Separation properties

Any apartness space comes with an [[irreflexive relation]] $\lt$ defined by $x \lt y$ iff $y\bowtie \{x\}$.  This is a positive version of the negation of the [[specialization order]].  Just as a topological space is called $T_1$ (see [[separation axioms]]) if its specialization order is discrete, i.e. $(x\le y) \to (x=y)$, we may call an apartness space **$T_1$** if the contrapositive of this holds, i.e. $(x\neq y) \to (x \bowtie \{y\})$.  In fact it is often more useful to replace $\neq$ here by a given [[apartness relation]] or [[inequality relation]] $#$ on $X$, and in this context we can also replace $y\notin B$ in the third axiom with $\forall z\in B, (y # z)$.

An apartness space may be called **comparable** (nonce definition on this page) if $x\bowtie A$ implies $(x\neq y) \vee (y\bowtie A)$ for any $y$, where $\neq$ might also be a given apartness on $X$.  This condition is classically trivial, and generalizes the [[comparison]] axiom on a point--point [[apartness relation]].  (In particular, if we take $\neq$ to be the relation $\lt$ defined above, then this property implies that $\lt$ is a [[comparison]] --- though in general it need not be symmetric, hence not an [[apartness relation]].)  It is also related topologically to Penon's definition of intrinsic [[open subset]] in [[synthetic topology]], and can also be viewed as a very weak version of [[regular space|regularity]].

[Bridges et al](#BSV) define apartness spaces to always be both $T_1$ and comparable, with respect to a given inequality on $X$.

An apartness space is **[[locally decomposable space|locally decomposable]]** if whenever $x\bowtie A$, there exists a set $B$ such that $x\bowtie B$ and every $y$ satisfies either $y\bowtie A$ or $y\in B$.  This condition is also classically trivial: take $B = \{ y \mid \neg(y\bowtie A) \}$.  It implies comparability (for $\neq$ the [[denial inequality]]).

## Relation to topological spaces

If $X$ is a topological space, we define $x\bowtie A$ if there is a neighborhood of $x$ disjoint from $A$.  This makes $X$ an apartness space.  Only the last axiom is somewhat nontrivial: if $x\in U$ with $U$ open and $U\cap A = \emptyset$, and $\forall y, (y\bowtie A \to y\notin B)$, then since $(y\in U) \Rightarrow (y\bowtie A)$ we have $U\cap B = \emptyset$ too, so $x\bowtie B$.

Conversely, if $X$ is an apartness space, define $U\subseteq X$ to be open if for all $x\in U$ there is a set $A$ such that $x\bowtie A$ and $\forall y, (y\bowtie A \Rightarrow y\in U)$.  This makes $X$ a topological space; the last axiom is not even needed.

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

* [[Douglas Bridges]], Peter Schuster, and Luminita Vita, *Apartness, Topology, and Uniformity: a Constructive View*, [doi](http://dx.doi.org/10.1002/1521-3870%28200210%2948:1%2B%3C16::AID-MALQ16%3E3.0.CO;2-7)
 {#BSV}

* [[Douglas Bridges]] and Luminita Vita, *Apartness and Uniformity: A Constructive Development*. [link](http://link.springer.com/book/10.1007%2F978-3-642-22415-7)


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
