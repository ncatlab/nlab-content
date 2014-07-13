
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Proximity spaces
* table of contents
{: toc}

## Idea

In addition to the well-known [[topological spaces]], many other structures can be used to found topological reasoning on sets, including [[uniform spaces]] and _proximity spaces_.  Proximity spaces provide a level of structure in between topologies and uniformities; in fact a proximity is equivalent to an equivalence class of uniformities with the same [[totally bounded space|totally bounded]] [[reflection]].

Proximity spaces are often called _nearness spaces_, but this term has other meanings in the literature. (See for example [this article](http://ijmsa.yolasite.com/resources/43--newnew.pdf).) One can clarify with the term _set--set nearness space_.


## Notation and terminology

A __proximity space__ is a kind of [[structured set]]: it consists of a [[set]] $X$ (the set of __[[points]]__ of the space) and a __proximity structure__ on $X$.  This proximity structure is given by any of various [[binary relations]] between the [[subsets]] of $X$:

*  The __proximity relation__ or __nearness relation__ $\delta$; subsets $A$ and $B$ are __proximal__  or __near__ if $A \;\delta\; B$;
*  The __apartness relation__ $\bowtie$; $A$ and $B$ are __apart__ if $A \bowtie B$.
*  The __neighbourhood relation__ $\ll$; $A$ is a __proximal neighbourhood__ of $B$ if $B \ll A$.

The conditions required of these relations are given below in the Definitions.  (We say 'proximal neighbourhood' instead of simply 'neighbourhood' to avoid misapplying intuition from general topology.  That $A \ll B$ doesn\'t necessarily mean that $A \subseteq Int(B)$; sometimes it means that $Cl(A) \subseteq Int(B)$, which is stronger, or something else.)


In [[classical mathematics]], these relations are all interdefinable:

*  $A \;\delta\; B \;\iff\; \neg(A \bowtie B) \;\iff\; \neg(A \ll B')$;
*  $A \bowtie B \;\iff\; \neg(A \;\delta\; B) \;\iff\; A \ll B'$;
*  $A \ll B \;\iff\; \neg(A \;\delta\; B') \;\iff\; A \bowtie B'$.

(Here, $\neg$ indicates [[negation]] of truth values, while $B'$ is the [[complement]] of $B$ in $X$.)

In [[constructive mathematics]], any one of these relations may be taken as primary and the others defined using it; thus we distinguish, constructively, between a __set--set nearness space__, a __set--set apartness space__, and a __set--set neighbourhood space__.


## Definitions

From the previous section, we have a [[set]] $X$ and we are discussing [[binary relations]] $\delta, \bowtie, \ll$ on $X$.  These are required to satisfy the following conditions; in each row, the conditions for the various relations are all equivalent (classically).  In these conditions, $x, y$ are points, while $A, B, C$ are subsets, and we require them for all points or subsets.

| Name | Condition for nearness | Condition for apartness | Condition for proximal neighbourhoods |
| - | - | - | - |
| Symmetry | $A \;\delta\; B$ iff $B \;\delta\; A$ | $A \bowtie B$ iff $B \bowtie A$ | $A \ll B$ iff $B' \ll A'$ |
| Additivity (left, binary) | $A \cup B \;\delta\; C$ iff $A \;\delta\; C$ or $B \;\delta\; C$ | $A \cup B \bowtie C$ iff $A \bowtie C$ and $B \bowtie C$ | $A \cup B \ll C$ iff $A \ll C$ and $B \ll C$ |
| Additivity (right, binary) | $A \;\delta\; B \cup C$ iff $A \;\delta\; B$ or $A \;\delta\; C$ | $A \bowtie B \cup C$ iff $A \bowtie B$ and $A \bowtie C$ | $A \ll B \cap C$ iff $A \ll B$ and $A \ll C$ |
| Additivity (left, nullary) | It is false that $\emptyset \;\delta\; A$ | $\emptyset \bowtie A$ | $\emptyset \ll A$ |
| Additivity (right, nullary) | It is false that $A \;\delta\; \emptyset$ | $A \bowtie \emptyset$ | $A \ll X$ |
| Isotony | If $A \subseteq C$ and $B \subseteq D$, then $C \;\delta\; D$ if $A \;\delta\; B$ | If $A \subseteq C$ and $B \subseteq D$, then $A \bowtie B$ if $C \bowtie D$ | If $A \subseteq C$ and $B \subseteq D$, then $A \ll D$ if $C \ll B$ |
| Reflexivity (general) | If $A$ meets $B$ (their [[intersection]] is [[inhabited subset|inhabited]]), then $A \;\delta\; B$ | If $A \bowtie B$, then $A$ and $B$ are [[disjoint set|disjoint]] | If $A \ll B$, then $A \subseteq B$ |
| Reflexivity (for singletons) | $\{x\} \;\delta\; \{y\}$ | It is false that $\{x\} \bowtie \{y\}$ | If $\{x\} \ll A$, then $x \in A$ |
| Regularity (constructive) | If for every $D, E \subseteq X$ such that $D \cup E = X$, either $A \;\delta\; D$ or $E \;\delta\; B$, then $A \;\delta\; B$ | If $A \bowtie B$, then for some $D, E \subseteq X$ such that $D \cup E = X$, both $A \bowtie D$ and $E \bowtie B$ | If $A \ll B$, then for some $D, E \subseteq X$ such that $D \subseteq E$, both $A \ll D$ and $E \ll B$ |
| Regularity (simplified) | If for every $D \subseteq X$, either $A \;\delta\; D$ or $D' \;\delta\; B$, then $A \;\delta\; B$ | If $A \bowtie B$, then for some $D \subseteq X$, both $A \bowtie D$ and $D' \bowtie B$ | If $A \ll B$, then for some $D \subseteq X$, both $A \ll D$ and $D \ll B$ |

In this list, Isotony is redundant; it is equivalent to one direction of (left and right) binary additivity, so some lists include only the other direction.  In the light of Isotony, we need Reflexivity only for singletons, although this is often not done (to avoid mentioning points).  Similarly, Isotony allows us to simplify Regularity as shown (which is usually done), although this simplification is appropriate for constructive mathematics only when defining neighbourhood spaces.  Finally, left and right Additivity are equivalent in the light of Symmetry, so usually only one direction is given.

On the other hand, we have a __quasiproximity__ (etc) if Symmetry is allowed to fail; then both left and right Additivity must be stated.  (Symmetry for neighbourhood spaces is particularly tricky in constructive mathematics.)

If $X$ and $Y$ are (quasi)-proximity spaces, then a [[function]] $f: X \to Y$ is said to be **proximally continuous** if $A \;\delta\; B$ implies $f_*(A) \;\delta\; f_*(B)$, equivalently if $A \bowtie B$ whenever $f_*(A) \bowtie f_*(B)$, equivalently if $f^*(C) \ll f^*(D)$ whenever $C \ll D$.  In this way we obtain a [[category]] $Prox$; the [[forgetful functor]] $Prox \to Set$ (taking a space to its set of points) makes it into a [[topological concrete category]].  The same goes for the category $QProx$ of quasiproximity spaces.


## Relation to other topological structures

### Preorders

Given points $x, y$ of a (quasi)-proximity space, let $x \leq y$ mean that $x$ belongs to every proximal neighbourhood of $\{y\}$, or equivalently (via Isotony) that $\{y\} \;\delta\; \{x\}$.  By Reflexivity, $\leq$ is [[reflexive relation|reflexive]]; by Regularity, $\leq$ is [[transitive relation|transitive]].  (In fact, we can use these to deduce that $x \leq y$ iff every proximal neighbourhood of $\{y\}$ is a proximal neighbourhood of $\{x\}$, which is manifestly reflexive and transitive.)  Therefore, $\leq$ is a [[preorder]].

If the quasiproximity satisfies Symmetry, then this preorder is [[symmetric relation|symmetric]] and hence an [[equivalence relation]].

Regardless of Symmetry, we say that a (quasi)-proximity space is __separated__ if this preorder is the [[equality relation]].  That is, $x = y$ if $x$ belongs to every proximal neighbourhood of $\{y\}$, or equivalently if every proximal neighbourhood of $\{y\}$ is a proximal neighbourhood of $\{x\}$, or equivalently if $\{x\}$ is near $\{y\}$, or equivalently if $\{x\}$ is not apart from $\{y\}$.  This may be viewed as a converse of simplified Reflexivity, which states that $\{x\} \;\delta\; \{y\}$ whenever $x = y$.

Conversely, given a set equipped with a preorder $\leq$, let $A \;\delta\; B$ if $x \leq y$ for some $x \in A$ and some $y \in B$, or equivalently let $A \bowtie B$ if $x \leq y$ for no $x \in A$ and no $y \in B$, or equivalently let $A \ll B$ if $x \leq y$ for $x \in A$ implies $y \in B$.  The we have a quasiproximity space which is symmetric iff $\leq$ is.

In this way, we get the category $Proset$ of preordered sets as a [[reflexive subcategory]] of $QProx$, with the category $Setoid$ of [[setoids]] (sets equipped with equivalence relations) as a reflexive subcatgory of $Prox$.


### Topological spaces

Every proximity space is a [[topological space]]; let $x$ belong to the closure of $A \subseteq X$ iff $\{x\} \;\delta\; A$, or equivalently let $x$ belong to the interior of $A$ iff $\{x\} \ll A$.  This topology is always [[completely regular space|completely regular]], and [[Hausdorff space|Hausdorff]] (hence [[Tychonoff space|Tychonoff]]) iff the proximity space is separated; see [[separation axiom]].  Proximally continuous functions are [[continuous map|continuous]] for the induced topologies, so we have a functor $Prox \to Top$ over $Set$.

Conversely, if $(X,\tau)$ is a completely regular topological space, then for any $A, B \subseteq X$ let $A \bowtie B$ iff there is a continuous function $f: X\to [0,1]$ such that $f(x) = 0$ for $x \in A$ and $f(x) = 1$ for $x \in B$.  This defines a proximity structure on $X$, which induces the topology $\tau$ on $X$, and which is separated iff $\tau$ is a Hausdorff (hence Tychonoff) topology.

In general, a completely regular topology may be induced by more than one proximity.  However, if it is moreover [[compact topological space|compact]], then it has a unique compatible proximity, given above.  In the case of a [[compact Hausdorff space]] (or more generally any [[normal regular space]]), we then have $A \ll B$ iff $Cl(A) \subseteq Int(B)$.


### Uniform spaces

If $U$ is a [[uniformity]] on $Y$ (making it into a [[uniform space]]), then for all $A, B \subseteq Y$ let $A \;\delta\; B$ iff $V \cap (A \times B)$ is [[inhabited set|inhabited]] for every [[entourage]] (aka vicinity) $V$. This also defines a proximity structure on $Y$.

[[uniformly continuous map|Uniformly continuous functions]] are proximally continuous for the induced proximities, so we have a functor $Unif \to Prox$ over $Set$.  Moreover, the composite $Unif \to Prox \to Top$ is the usual "underlying topology" functor of a uniform space, i.e. the topology induced by the uniformity and the topology induced by the proximity structure are the same.

Conversely, if $X$ is a proximity space, consider the family of sets of the form
$$ \bigcup_{k=1}^n (A_k \times A_k) $$
where $(A_k)_k$ is a [[list]] (a finite family) of sets such that there exists a same-length list of sets $(B_k)_k$ with $B_k \ll A_k$ and $X = \bigcup_{k=1}^n B_k$.  These sets form a base for a [[totally bounded uniformity]] on $X$, which induces the given proximity.

In fact, this is the *unique* totally bounded uniformity which induces the given proximity: every proximity-class of uniformities contains a unique totally bounded member.  Moreover, a proximally continuous function between uniform spaces with totally bounded [[codomain]] is automatically uniformly continuous.  Therefore, the forgetful functor $Unif \to Prox$ is a left adjoint, whose right adjoint also lives over $Set$, is [[fully faithful functor|fully faithful]], and has its [[essential image]] given by the totally bounded uniform spaces.

In general, proximally continuous functions need not be uniformly continuous, but in addition to total boundedness of the codomain, a different sufficient condition is that the domain be a [[metric space]].


### Syntopogenous spaces

A proximity space can be identified with a [[syntopogenous space]] which is both *simple* and *symmetric*; see [[syntopogenous space]].


### Compactifications

The (separated) proximities inducing a given (Hausdorff) completely regular topology can be identified with (Hausdorff) [[compactifications]] of that topology.  The compactification corresponding to a proximity on $X$ is called its __Smirnov compactification__.  The points of this compactification can be taken to be __clusters__ in $X$, which are defined to be collections $\sigma$ of subsets of $X$ such that

1. If $A \in \sigma$ and $B \in \sigma$, then $A \;\delta\; B$.
2. If $A \;\delta\; C$ for all $C \in \sigma$, then $A \in \sigma$.
3. If $(A \cup B) \in \sigma$, then $A \in \sigma$ or $B \in \sigma$.


## Related concepts

* [[uniform space]], [[syntopogenous space]], [[apartness relation]], [[pretopological space]]


## References

*  R. Engelking, _General topology_, chapter 8.

*  [[Douglas Bridges]] et al, _Apartness, topology, and uniformity: a constructive view_, [pdf](http://www.math.canterbury.ac.nz/mathlsv/dagstuhl01.pdf)

*  S. A. Naimpally and B. D. Warrack, _Proximity spaces_, Cambridge University Press 1970


[[!redirects proximity]]
[[!redirects proximities]]
[[!redirects proximity space]]
[[!redirects proximity spaces]]
[[!redirects proximity structure]]
[[!redirects proximity structures]]
[[!redirects proximity relation]]
[[!redirects proximity relations]]

[[!redirects nearness space]]
[[!redirects nearness spaces]]
[[!redirects nearness structure]]
[[!redirects nearness structures]]
[[!redirects nearness relation]]
[[!redirects nearness relations]]

[[!redirects set-set nearness space]]
[[!redirects set-set nearness spaces]]
[[!redirects set–set nearness space]]
[[!redirects set–set nearness spaces]]
[[!redirects set--set nearness space]]
[[!redirects set--set nearness spaces]]
[[!redirects set-set nearness structure]]
[[!redirects set-set nearness structures]]
[[!redirects set–set nearness structure]]
[[!redirects set–set nearness structures]]
[[!redirects set--set nearness structure]]
[[!redirects set--set nearness structures]]
[[!redirects set-set nearness relation]]
[[!redirects set-set nearness relations]]
[[!redirects set–set nearness relation]]
[[!redirects set–set nearness relations]]
[[!redirects set--set nearness relation]]
[[!redirects set--set nearness relations]]

[[!redirects quasiproximity]]
[[!redirects quasiproximities]]
[[!redirects quasi-proximity]]
[[!redirects quasi-proximities]]
[[!redirects quasiproximity space]]
[[!redirects quasiproximity spaces]]
[[!redirects quasi-proximity space]]
[[!redirects quasi-proximity spaces]]
[[!redirects quasiproximity structure]]
[[!redirects quasiproximity structures]]
[[!redirects quasi-proximity structure]]
[[!redirects quasi-proximity structures]]
[[!redirects quasiproximity relation]]
[[!redirects quasiproximity relations]]
[[!redirects quasi-proximity relation]]
[[!redirects quasi-proximity relations]]

[[!redirects proximally continuous function]]
[[!redirects proximally continuous functions]]

[[!redirects Smirnov compactification]]
[[!redirects Smirnov compactifications]]
