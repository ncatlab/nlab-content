
# Apartness spaces
* table of contents
{: toc}

## Idea

An *apartness space* is a set equipped with an "apartness relation" that distinguishes between pairs of points or sets.  They are particularly interesting in [[constructive mathematics]]; in [[classical mathematics]] they tend to be equivalent to better-known definitions expressed in terms of "closeness" rather than "apartness".


## Definitions

There are actually three different notions of "apartness space" depending on whether the objects being compared on each side are points or sets.

* A _point--point apartness space_ is a set $X$ equipped with an _[[apartness relation]]_, usually written $x # y$ on elements $x,y\in X$.  Sometimes it is required to be [[tight relation|tight]], or to be only an [[inequality relation]].

* A _set--set apartness space_ is a set $X$ equipped with a relation $A\bowtie B$ between [[subsets]] $A,B\subseteq X$, satisfying appropriate axioms.  A set--set apartness space is one of the ways to describe the [[classical mathematics|classical]] notion of a _[[proximity space]]_.  In [[constructive mathematics]], the definition of a proximity space in terms of $\bowtie$ can be taken as a definition of a set--set apartness space.

* A __point--set apartness space__ is a set $X$ equipped with a relation $x \bowtie A$ between points $x\in X$ and subsets $A\subseteq X$, satisfying appropriate axioms.  In [[classical mathematics]], these axioms are obtained by [[contrapositive|contraposition]] from the definition of a [[topological space]] in terms of a [[exact functor|right exact]] [[Moore closure]] operator, so that point--set apartness spaces are equivalent to topological spaces.  In [[constructive mathematics]] ... well, keep reading.

Since point--point apartness spaces are described at [[apartness relation]], and set--set apartness spaces at [[proximity space]], the rest of this page will be about point--set apartness spaces.


### Point--set apartness spaces

+-- {: .un_defn}
###### Definition
An __apartness space__ is a set $X$ equipped with a relation $\bowtie$ between points $x\in X$ and subsets $A\subseteq X$ such that

1. if $x\bowtie A$, then $x\notin A$.
2. $x\bowtie (A\cup B)$ iff $x\bowtie A$ and $x\bowtie B$.
3. If $x \bowtie A$, and $\forall y, (y\bowtie A \to y\notin B)$, then $x\bowtie B$.
=--

The relation $x\bowtie A$ should be regarded as a "positive" way of saying that $x$ does not belong to the [[closure]] of $A$, i.e. $x\notin \overline{A}$.  Under this interpretation, the above axioms contrapose to become

1. If $x\in A$, then $x\in \overline{A}$, i.e. $A\subseteq \overline{A}$.
2. $\overline{A} \cup \overline{B} = \overline{A\cup B}$ (and in particular $(A\subseteq B) \to (\overline{A}\subseteq \overline{B})$).
3. If $B\subseteq \overline{A}$ and $x\in \overline{B}$, then $x\in\overline{A}$, i.e. $\overline{\overline{A}} = \overline{A}$.

which are precisely the axioms of a [[topology]] expressed in terms of a closure operator.  In constructive mathematics, of course, the law of contraposition does not hold.


## Separation properties

Any apartness space comes with an [[irreflexive relation]] $\lt$ defined by $x \lt y$ iff $y\bowtie \{x\}$.  This is a positive version of the negation of the [[specialization order]].  Just as a topological space is called $T_1$ (see [[separation axioms]]) if its specialization order is discrete, i.e. $(x\le y) \to (x=y)$, we may call a n apartness space **$T_1$** if the contrapositive of this holds, i.e. $(x\neq y) \to (x \bowtie \{y\})$.  In fact it is often more useful to replace $\neq$ here by a given [[apartness relation]] or [[inequality relation]] $#$ on $X$, and in this context we can also replace $y\notin B$ in the third axiom with $\forall z\in B, (y # z)$.

An apartness space may be called **comparable** (nonce definition on this page) if $x\bowtie A$ implies $(x\neq y) \vee (y\bowtie A)$ for any $y$, where $\neq$ might also be a given apartness on $X$.  This condition is classically trivial, and generalizes the [[comparison]] axiom on a point--point [[apartness relation]].  (In particular, if we take $\neq$ to be the relation $\lt$ defined above, then this property implies that $\lt$ is a [[comparison]] --- though in general it need not be symmetric, hence not an [[apartness relation]].)  It is also related topologically to Penon's definition of intrinsic [[open subset]] in [[synthetic topology]], and can also be viewed as a very weak version of [[regular space|regularity]].

[Bridges et al](#BSV) define apartness spaces to always be both $T_1$ and comparable, with respect to a given inequality on $X$.


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
