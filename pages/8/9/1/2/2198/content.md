In addition to [[topological spaces]], some other structures can be used to found topological reasoning on sets, including [[uniform spaces]] and _proximity spaces_.  Proximity spaces are often (perhaps usually) called _nearness spaces_, but this term has other meanings in the literature; one can clarify with the term _set--set nearness space_.


## Definition

A __proximity structure__ (or set--set __nearness structure__) on a [[set]] $X$, or a __proximity relation__ (or __nearness relation__) on the [[power set]] $P(X)$ of subsets of $X$, is a binary [[relation]] $\delta$ on $P(X)$ such that 

1. _symmetry_:  $A\;\delta\;B$ iff $B\;\delta\;A$;

2. _binary additivity_:  $A\;\delta\;B\cup C$ iff either $A\;\delta\;B$ or $A\;\delta\;C$;

3. _nullary additivity_:  it is never true that $A\;\delta\;\emptyset$;

4. $\{x\}\;\delta\;\{y\}$ if $x=y$

5. if for every $C,D\subset X$ such that $C\cup D=X$, either $A\;\delta\;C$ or $B\;\delta\;D$, then $A\;\delta\;B$.

Often one requires the converse of (4):

*  _separation_:  $x=y$ if $\{x\}\;\delta\;\{y\}$

We say that $A$ and $B$ are __proximate__ (or __near__) if $A\;\delta\;B$, and __apart__ otherwise.  We also write $A \ll B$ if $(X \setminus A)\;\delta\;B$.

A __proximity space__ (or set--set __nearness space__) is a set $X$ equipped with a proximity structure $\delta$.  The proximity structure or proximity space is __separated__ if it satisfies the separation axiom (the converse of 4); note that many authors require this by default.

There are many variations possible in the list of axioms; one important consequence of the above (sometimes listed separately, allowing additivity to be weakened) is this:

*  _isotony_:  if $A\subset C$ and $B\subset D$, then $C\;\delta\;D$ if $A\;\delta\;B$.

It is also possible to write the definition in terms of the apartness relation or the relation $\ll$.  In particular, a (set--set) __apartness space__ is a set $X$ equipped with a binary relation $\bowtie$ on $P(X)$ such that the [[negation]] of $\bowtie$ is a proximity relation.  This is the preferred formulation in [[constructive mathematics]] (although you\'ll want to rephrase the definition axiom by axiom to remove spurious double negations).


## Relation to other topological structures

Every proximity space is a [[topological space]]; let $x$ belong to the closure of $A\subset X$ iff $\{x\}\;\delta\;A$.  This topology is always completely regular, and Hausdorff (hence Tychonoff) iff the proximity space is separated; see [[separation axiom]].

Conversely, if $(X,\tau)$ is a completely regular topological space, then for any $A,B\subset X$ let $A\;\delta\;B$ iff $A\neq \emptyset\neq B$ and there is no continuous function $f:X\to I=[0,1]$ such that $f(x)=0$ on $A$ and $f(x)=1$ on $B$. This defines a proximity structure on $X$, which induces the topology $\tau$ on $X$, and which is separated iff $\tau$ is a Hausdroff (hence Tychonoff) topology.

If $U$ is a uniformity on $Y$ (making it into a [[uniform space]]), then for all $A,B\subset Y$ let $A\delta B$ iff $V\cap (A\times B)\neq \emptyset$ for every [[entourage]] (aka vicinity) $V\in U$. This also defines a proximity structure on $Y$. The topology induced by the uniformity and the topology induced by the proximity structure are the same.


## References

*  R. Engelking, _General topology_, chapter 8.
*  [[Douglas Bridges]] et al, _Apartness, topology, and uniformity: a constructive view_, [pdf](http://www.math.canterbury.ac.nz/mathlsv/dagstuhl01.pdf)


[[!redirects proximity spaces]]
[[!redirects proximity structure]]
[[!redirects proximity relation]]
[[!redirects nearness space]]
[[!redirects nearness structure]]
[[!redirects nearness relation]]
[[!redirects set-set nearness space]]
[[!redirects set-set nearness structure]]
[[!redirects set-set nearness relation]]
[[!redirects set–set nearness space]]
[[!redirects set–set nearness structure]]
[[!redirects set–set nearness relation]]
[[!redirects set--set nearness space]]
[[!redirects set--set nearness structure]]
[[!redirects set--set nearness relation]]