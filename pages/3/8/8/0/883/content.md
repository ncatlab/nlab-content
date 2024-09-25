
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **comparison** or **cotransitive relation** or **weakly linear relation** on a set $A$ is a (binary) [[relation]] $\sim$ on $A$ such that in every pair of related elements, any other element is related to one of the original elements in the same order as the original pair:
$$\forall (x, y, z: A),\; x \sim z \;\Rightarrow\; x \sim y \;\vee\; y \sim z$$
which generalises from $3$ to any (finite, positive) number of elements.  To include the case where $n = 1$, we must explicitly state that the relation is [[irreflexive relation|irreflexive]].

Alternatively, this is the same condition as 
$$\forall (x, z: A),\; x \sim z \;\Rightarrow\; \forall (y: A),\; x \sim y \;\vee\; y \sim z$$

Comparisons are most often studied in [[constructive mathematics]].  In particular, the relation $\lt$ on the (located Dedekind) [[real numbers]] is an [[irreflexive comparison]], even though its [[negation]] $\geq$ is not constructively [[total relation|total]].  (Indeed, $\lt$ is a [[pseudo-order]], even though $\geq$ is not constructively a [[total order]].)

A comparison is a [[cartesian monoidal category|cartesian monoidal]] [[semicategory]] [[enriched category|enriched]] on the [[co-Heyting algebra]] $TV^\op$, where $TV$ is the [[Heyting algebra]] of [[truth values]].

## Mere and pure comparisons

In [[dependent type theory]], there are two different notions of a cotransitive or weakly linear relation

* There is the traditional interpretation of a cotransitive or weakly linear relation which uses the [[disjunction]], and is called a **merely cotransitive relation** or **merely weakly linear relation** or a **mere comparison**

$$\prod_{x, y, z: A}  x \sim z \to (x \sim y \vee y \sim z)$$

* There is the traditional interpretation of a cotransitive or weakly linear relation which uses the [[sum type]] to represent inclusive or, and is called a **purely cotransitive relation** or **purely weakly linear relation** or a **pure comparison** or a **constructively cotransitive relation** or **constructively weakly linear relaiton** or a **constructive comparison**

$$\prod_{x, y, z: A}  x \sim z \to (x \sim y + y \sim z)$$

This distinction could also be made in [[set theory]]: Given a proposition $P$, $P$ can be made into a [[subsingleton]] [[set]] by considering the subset $\{\top \vert P\} \coloneqq \{p \in \{\top\} \vert (p = \top) \wedge P\}$ of the [[singleton]] $\{\top\}$. Let $[A]$ denote the [[support of a set|support of the set]] $A$, and let $A \uplus B$ denote the [[disjoint union]] of sets $A$ and $B$. Then 

* a **merely cotransitive relation** or **merely weakly linear relation** on a set $A$ is a relation $\sim$ which for all $x$, $y$, and $z$ one can construct an element 

$$\mathrm{cotransitive}(x, y, z) \in \left[\{\top \vert x \sim y\} \uplus \{\top \vert y \sim z\}\right]^{\{\top \vert x \sim z\}}$$

* a **purely cotransitive relation** or **purely weakly linear relation** or **constructively cotransitive relation** or **constructively weakly linear relation** on a set $A$ is a relation $\sim$ which for all $x$, $y$, and $z$ one can construct an element 

$$\mathrm{cotransitive}(x, y, z) \in \left(\{\top \vert x \sim y\} \uplus \{\top \vert y \sim z\}\right)^{\{\top \vert x \sim z\}}$$

## Related concepts

* [[pseudo-order]]

* [[total relation]]

## References

* Wikipedia, [Apartness relation](https://en.wikipedia.org/wiki/Apartness_relation)

* Wikipedia, [Pseudo-order](https://en.wikipedia.org/wiki/Pseudo-order)

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

[[!redirects comparison]]
[[!redirects comparisons]]
[[!redirects comparison relation]]
[[!redirects comparison relations]]

[[!redirects mere comparison]]
[[!redirects mere comparisons]]
[[!redirects mere comparison relation]]
[[!redirects mere comparison relations]]

[[!redirects pure comparison]]
[[!redirects pure comparisons]]
[[!redirects pure comparison relation]]
[[!redirects pure comparison relations]]

[[!redirects constructive comparison]]
[[!redirects constructive comparisons]]
[[!redirects constructive comparison relation]]
[[!redirects constructive comparison relations]]

[[!redirects cotransitive]]
[[!redirects cotransitive relation]]
[[!redirects cotransitive relations]]
[[!redirects cotransitivity]]

[[!redirects merely cotransitive]]
[[!redirects merely cotransitive relation]]
[[!redirects merely cotransitive relations]]
[[!redirects mere cotransitivity]]

[[!redirects purely cotransitive]]
[[!redirects purely cotransitive relation]]
[[!redirects purely cotransitive relations]]
[[!redirects pure cotransitivity]]

[[!redirects constructively cotransitive]]
[[!redirects constructively cotransitive relation]]
[[!redirects constructively cotransitive relations]]
[[!redirects constructive cotransitivity]]

[[!redirects weakly linear]]
[[!redirects weakly linear relation]]
[[!redirects weakly linear relations]]
[[!redirects weak linearity]]

[[!redirects merely weakly linear]]
[[!redirects merely weakly linear relation]]
[[!redirects merely weakly linear relations]]
[[!redirects mere weak linearity]]

[[!redirects purely weakly linear]]
[[!redirects purely weakly linear relation]]
[[!redirects purely weakly linear relations]]
[[!redirects pure weak linearity]]

[[!redirects constructively weakly linear]]
[[!redirects constructively weakly linear relation]]
[[!redirects constructively weakly linear relations]]
[[!redirects constructive weak linearity]]
