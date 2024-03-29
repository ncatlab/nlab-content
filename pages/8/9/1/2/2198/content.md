
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

Proximity spaces are often called _nearness spaces_, but this term has other meanings in the literature. (See for example [this article](http://ijmsa.yolasite.com/resources/43--newnew.pdf).) One can clarify with the term _set--set nearness space_.  The same goes for the term _apartness space_, which is another way to look at the same basic idea.  (See [[apartness space]] for a point--set version and [[apartness relation]] for a point--point version.)


## Notation and terminology

A __proximity space__ is a kind of [[structured set]]: it consists of a [[set]] $X$ (the set of __[[points]]__ of the space) and a __proximity structure__ on $X$.  This proximity structure is given by any of various [[binary relations]] between the [[subsets]] of $X$:

*  The __proximity relation__ or __nearness relation__ $\delta$; subsets $A$ and $B$ are __proximal__  or __near__ if $A \;\delta\; B$;
*  The __apartness relation__ $\bowtie$; $A$ and $B$ are __apart__ if $A \bowtie B$.
*  The __neighbourhood relation__ $\ll$; $A$ is a __proximal neighbourhood__ of $B$ if $B \ll A$.

The conditions required of these relations are given below in the Definitions.  (We say 'proximal neighbourhood' instead of simply 'neighbourhood' to avoid misapplying intuition from general topology.  That $A \ll B$ doesn\'t necessarily mean that $A \subseteq Int(B)$; sometimes it means that $Cl(A) \subseteq Int(B)$, which is stronger, or something else.)


In [[classical mathematics]], these relations are all interdefinable:

*  $A \;\delta\; B \;\iff\; \neg(A \bowtie B) \;\iff\; \neg(A \ll B^{\mathsf{c}})$;
*  $A \bowtie B \;\iff\; \neg(A \;\delta\; B) \;\iff\; A \ll B^{\mathsf{c}}$;
*  $A \ll B \;\iff\; \neg(A \;\delta\; B^{\mathsf{c}}) \;\iff\; A \bowtie B^{\mathsf{c}}$.

(Here, $\neg$ indicates [[negation]] of truth values, while $B^{\mathsf{c}}$ is the [[complement]] of $B$ in $X$, i.e. $X\setminus B$.)

In [[constructive mathematics]], any one of these relations may be taken as primary and the others defined using it; thus we distinguish, constructively, between a __set--set nearness space__, a __set--set apartness space__, and a __set--set neighbourhood space__.


## Definitions

From the previous section, we have a [[set]] $X$ and we are discussing [[binary relations]] $\delta, \bowtie, \ll$ on $X$.  These are required to satisfy the following conditions; in each row, the conditions for the various relations are all equivalent (classically).  In these conditions, $x, y$ are points, while $A, B, C$ are subsets, and we require them for all points or subsets.  We list the conditions roughly in order of increasing optional-ness, then define terminology for relations satisfying them.

| Name | Condition for nearness | Condition for apartness | Condition for proximal neighbourhoods |
| - | - | - | - |
| Isotony (left) | If $A \supseteq B \;\delta\; C$, then $A \;\delta\; C$ | If $A \subseteq B \bowtie C$, then $A \bowtie C$ | If $A \subseteq B \ll C$, then $A \ll C$ |
| Isotony (right) | If $B \;\delta\; C \subseteq D$, then $B \;\delta\; D$ | If $B \bowtie C \supseteq D$, then $B \bowtie D$ | If $B \ll C \subseteq D$, then $B \ll D$ |
| Additivity (left, nullary) | It is false that $\emptyset \;\delta\; A$ | $\emptyset \bowtie A$ | $\emptyset \ll A$ |
| Additivity (right, nullary) | It is false that $A \;\delta\; \emptyset$ | $A \bowtie \emptyset$ | $A \ll X$ |
| Additivity (left, binary) | If $A \cup B \;\delta\; C$, then $A \;\delta\; C$ or $B \;\delta\; C$ | If $A \bowtie C$ and $B \bowtie C$, then $A \cup B \bowtie C$ | If $A \ll C$ and $B \ll C$, then $A \cup B \ll C$ |
| Additivity (right, binary) | If $A \;\delta\; B \cup C$, then $A \;\delta\; B$ or $A \;\delta\; C$ | If $A \bowtie B$ and $A \bowtie C$, then $A \bowtie B \cup C$ | If $A \ll B$ and $A \ll C$, then $A \ll B \cap C$ |
| Reflexivity (general) | If $A$ meets $B$ (their [[intersection]] is [[inhabited subset|inhabited]]), then $A \;\delta\; B$ | If $A \bowtie B$, then $A$ and $B$ are [[disjoint set|disjoint]] | If $A \ll B$, then $A \subseteq B$ |
| Reflexivity (for singletons) | $\{x\} \;\delta\; \{x\}$ | It is false that $\{x\} \bowtie \{x\}$ | If $\{x\} \ll A$, then $x \in A$ |
| Transitivity | If for every $D \subseteq X$, either $A \;\delta\; D^{\mathsf{c}}$ or $D \;\delta\; B$, then $A \;\delta\; B$ | If $A \bowtie B$, then for some $D \subseteq X$, both $A \bowtie D^{\mathsf{c}}$ and $D \bowtie B$ | If $A \ll B$, then for some $D \subseteq X$, both $A \ll D$ and $D \ll B$ |
| Symmetry (weak) | if $A \;\delta\; B$ then $B \;\delta\; A$ | if $A \bowtie B$ then $B \bowtie A$ | if $A \ll B$ then $B^{\mathsf{c}} \ll A^{\mathsf{c}}$ |
| Symmetry (strong) | $A \;\delta\; B$ iff $B \;\delta\; A$ | $A \bowtie B$ iff $B \bowtie A$ | $A \ll B$ iff $B^{\mathsf{c}} \ll A^{\mathsf{c}}$ |
| Local Decomposability | | If $\{x\}\bowtie B$, then for some $C$ and $D$, $\{x\}\bowtie D$, $C\bowtie B$, and $C\cup D = X$. | If $\{x\}\ll B$, then for some $C$ and $D$, $\{x\}\ll C$, $D\ll B$, and $C^{\mathsf{c}}\cup D = X$. |
| Decomposability | | If $A\bowtie B$, then for some $C$ and $D$, $A\bowtie D$, $C\bowtie B$, and $C\cup D = X$. | If $A\ll B$, then for some $C$ and $D$, $A\ll C$, $D\ll B$, and $C^{\mathsf{c}}\cup D = X$. |
| Separation | If $\{x\} \delta \{y\}$, then $x = y$ | Unless $\{x\} \bowtie \{y\}$, then $x = y$ | $x = y$ if, for all $A$, $y \in A$ whenever $\{x\} \ll A$ |
| Perfection (left) | If $A \;\delta\; B$, then $\{x\} \;\delta\; B$ for some $x \in A$ | $A \bowtie B$ if $\{x\} \bowtie B$ for all $x \in A$ | $A \ll B$ if $\{x\} \ll B$ for all $x \in A$ |
| Perfection (right) | If $A \;\delta\; B$, then $A \;\delta\; \{y\}$ for some $y \in B$ | If $A \bowtie \{y\}$ for all $y \in B$, then $A \bowtie B$ | If $A \ll C_i$ for all $i$, then $A \ll \bigcap_i C_i$ |

When both left and right rules are shown, we only need one of them if we have Symmetry, but we need both if we lack Symmetry (or if we are using proximal neighbourhoods in constructive mathematics; see below).  Even so, Isotony is usually given on both sides, since it is convenient to combine both directions into a single statement.  On the other hand, Isotony is equivalent to the converse of binary Additivity, so sometimes these are combined instead (so Isotony does not explicitly appear), usually on only one side when Symmetry is used.

Whether made explicit or not, Isotony is very fundamental.  In particular, it allows us to assert Reflexivity only for singletons, although this is often not done (to avoid mentioning points).

In [[classical mathematics]], the weak Symmetry axioms are equivalent to the strong versions, while Decomposability is equivalent to Transitivity (and Local Decomposability is of course a special case of Decomposability).  In [[constructive mathematics]], strong Symmetry for $\ll$ is unreasonably strong (as is binary Additivity for $\delta$), while Local Decomposability and Decomposability appear genuinely stronger than Transitivity (but not unreasonably so); see remarks below.  (We don't bother to state a version of (Local) Decomposability for $\delta$ because the other axioms for $\delta$ seem unreasonably strong constructively, while Decomposability is automatic in classical mathematics.)

A __topogeny__ is a relation that satisfies both forms of Isotony and all four forms of Additivity.  A __topogenous relation__ or __quasipreproximity__ is a topogeny that also satisfies Reflexivity; a __quasiproximity__ is a quasipreproximity that also satisfies Reflexivity and Transitivity.  A topogeny is __symmetric__ if it satisfies Symmetry; a __preproximity__ is a symmetric quasipreproximity, and a __proximity__ is a symmetric quasiproximity.  A topogeny is __separated__ if it satisfies Separation.  A topogeny is __perfect__ if it satisfies left Perfection, __coperfect__ if it satisfies right Perfection, and __biperfect__ if it satisfies both; a symmetric topogeny is usually called simply __perfect__ if it satisfies any form of Perfection, because then it must satisfy both (except in constructive mathematics using proximal neighbourhoods).  Constructively, a proximity space satisfying Regularity may be called __proximally regular__.

A __(quasi)-(pre)-proximity space__ is a set equipped with a (quasi)-(pre)-proximity.  All of these terms may be used with _nearness_, _apartness_, or _proximal neighbourhoods_, as explained in the previous section; nearness is usually the default.

+-- {: .un_remark}
###### Warnings

Some authors require a (quasi)-proximity to be separated; conversely, some authors do not require a (quasi)-proximity to satisfy Transitivity (so 'pre' is the default for them).  The term 'topogeny' is also not found in the literature (except [[toddtrimble:topogeny|here]], in a generalization of nearness spaces); it is derived from '[[topogenous relation]]', a term used in the theory of [[syntopogenous spaces]] for a quasipreproximity.  The terminology for Perfection also comes from syntopogenous spaces.

Transitivity is sometimes called _normality_, due to its superficial similarity with the notion of a [[normal space]].  However, the underlying topology of a proximity space need not be normal in the topological sense.  If regarded as a [[separation axiom]], the Transitivity axiom is more analogous to [[completely regular space|complete regularity]] than to normality, and at least in classical mathematics every proximity space is completely regular --- but this is not true in constructive mathematics, or for quasi-proximity spaces, so it is debatable whether it should be attributed to the Transitivity axiom.  When comparing proximities to topologies via [[syntopogenies]], Transitivity is instead analogous to the fact that the closure of a set is closed (or the interior of a set is open), which we require of all topologies; thus arguably we should require it of all (quasi-)proximities.  If this is removed from the definition of topological space, then we have a [[pretopological space]], which is the origin of the 'pre' terminology above.
=--

If $X$ and $Y$ are (quasi)-(pre)-proximity spaces, then a [[function]] $f: X \to Y$ is said to be **proximally continuous** if $A \;\delta\; B$ implies $f_*(A) \;\delta\; f_*(B)$, equivalently if $A \bowtie B$ whenever $f_*(A) \bowtie f_*(B)$, equivalently if $f^*(C) \ll f^*(D)$ whenever $C \ll D$.  In this way we obtain [[categories]] $QProx$ and $Prox$; the [[forgetful functors]] $QProx \to Set$ and $Prox \to Set$ (taking a space to its set of points) make them into [[topological concrete categories]].


### In constructive mathematics

As remarked above, the strong Symmetry axiom for $\ll$ is too strong in constructive mathematics.  In fact, if it is satisfied by a nontrivial space $X$, then [[excluded middle]] follows: for any [[truth value]] $P$ such that $\neg\neg P$ is true, let $A=X$ and $B = \{ x\in X \mid P \}$; then $B^{\mathsf{c}} = \emptyset \ll \emptyset = A^{\mathsf{c}}$, so strong Symmetry gives $A\ll B$, hence $A\subseteq B$ and so $P$ holds.

On the other hand, while the Symmetry axioms for $\bowtie$ and $\delta$ may seem stronger than the allowable weak symmetry axiom for $\ll$, this is arguably an illusion.  For given a proximal neighborhood space with $\ll$ (and weak Symmetry), if we define $A\bowtie B$ to mean $A\ll B^{\mathsf{c}}$, we obtain a proximal apartness space (with Symmetry).  In fact, the Transitivity axiom for $\bowtie$ implies that if $A\bowtie B$ then $A\bowtie (B^{\mathsf{c}})^{\mathsf{c}}$, so that (with Symmetry) $\bowtie$ is completely determined by its restriction to subsets that are complements.

In this sense, a proximal neighborhood space actually contains more information than a proximal apartness space; it is unclear whether the latter gives rise to the former constructively.  On the other side, we can of course define $A\;\delta \; B$ to mean $\neg(A\bowtie B)$, but with this definition we cannot even prove binary Additivity for $\delta$.  In fact, binary Additivity for $\delta$ seems too strong: it is apparently not satisfied even by a metric space.

We can, however, show the following constructively.

+--{: .un_theorem}
###### Theorem
(Quasi-)proximal apartness spaces satisfying Decomposability are equivalent to (quasi-)proximal neighborhood spaces satisfying Decomposability.
=--
+--{: .proof}
###### Proof
As above, in one direction we define $A\bowtie B$ to mean $A\ll B^{\mathsf{c}}$.  In the other, we define $A\ll B$ to mean that there exists a $C$ with $A\bowtie C$ and $B\cup C = X$.  Most of the axioms are easy.  To prove right binary Additivity for $\ll$, given $A\ll B$ and $A\ll C$, we have $A\bowtie D$ and $A\bowtie E$ with $D\cup B = X$ and $E\cup C = X$, whence $A\bowtie D\cup E$ with $(D\cup E) \cup (B\cap C) = X$ by distributing $\cup$ over $\cap$.

To prove Decomposability (and hence Transitivity) for $\ll$, given $A\ll B$, we have $A\bowtie C$ with $B\cup C = X$, whence by Decomposability for $\bowtie$ we have $D,E$ with $A\bowtie D$, $E\bowtie C$, and $D\cup E = X$.  By Decomposability again, we have $D_1,D_2,E_1,E_2$ with $A\bowtie D_1$, $D_2\bowtie D$, and $D_1\cup D_2 = X$, while $E\bowtie E_1$, $E_2\bowtie C$, and $E_1\cup E_2=X$.  Then $A\ll D_2$ (because of $D_1$) and $E_2 \ll B$ (because of $C$), while $D\subseteq D_2^{\mathsf{c}}$ (since $D_2\bowtie D$) and $E\subseteq E_2$ (because $E\bowtie E_1$ and so $E\subseteq E_1^{\mathsf{c}} \subseteq E_2$) and so $X = D\cup E = D_2^{\mathsf{c}} \cup E_2$.

Lastly, if $\bowtie$ satisfies Symmetry and $A\ll B$, we have $A\bowtie C$ with $B\cup C = X$, whence by Decomposability for $\bowtie$ we have $D,E$ with $A\bowtie D$, $E\bowtie C$, and $D\cup E = X$.  Then by Symmetry, we have $B^{\mathsf{c}} \subseteq C\bowtie E$ while $X = E\cup D \subseteq E\cup A^{\mathsf{c}}$, so $B^{\mathsf{c}} \ll A^{\mathsf{c}}$.

To show that these constructions are inverses, if we start with $\ll$ then by a round-trip we obtain $A\ll' B$ defined to mean that there exists $C$ with $A\ll C^{\mathsf{c}}$ and $B\cup C = X$.  Now on one hand, $B\cup C = X$ implies $C^{\mathsf{c}}\subseteq B$, so $A\ll C^{\mathsf{c}} \subseteq B$.  But on the other, if $A\ll B$ then Decomposability gives $C$ and $D$ with $A\ll C$, $D\ll B$, and $C^{\mathsf{c}}\cup D = X$, whence $A \ll (C^{\mathsf{c}})^{\mathsf{c}}$ and $X = D \cup C^{\mathsf{c}} \subseteq B \cup C^{\mathsf{c}}$.

On the other side, if we start with $\bowtie$ then by a round-trip we obtain $A\bowtie' B$ defined to mean that there exists $C$ with $A\bowtie C$ and $C \cup B^{\mathsf{c}}= X$.  Now on one hand, if $C \cup B^{\mathsf{c}}= X$ then $B \subseteq C$, so $A\bowtie C$ implies $A\bowtie B$.  But on the other, if $A\bowtie B$ then Decomposability gives $C$ and $D$ with $A\bowtie C$ and $D\bowtie B$ and $C\cup D = X$, whence $D\subseteq B^{\mathsf{c}}$ and so $X = C\cup D \subseteq C \cup B^{\mathsf{c}}$.
=--

In other words, the two constructively reasonable ways to define a (quasi-)proximity space give the same result in the Decomposable case.

On the other hand, the Decomposability axiom is very strong, constructively; as noted [below](#Uniform), the standard way to make a proximity space from a uniform space does not satisfy it.  Thus constructive treatments of proximity such as [Bridges-Vita](#BridgesVita) have usually not included Decomposability, instead using the weaker Transitivity axiom (called the *Efremovic property* in [Bridges-Vita](#BridgesVita)).


## Relations to other topological structures

### Preorders

Given points $x, y$ of a (quasi)-proximity space, let $x \leq y$ mean that $x$ belongs to every proximal neighbourhood of $\{y\}$, or equivalently (via Isotony) that $\{y\} \;\delta\; \{x\}$.  By Reflexivity, $\leq$ is [[reflexive relation|reflexive]]; by Transitivity, $\leq$ is [[transitive relation|transitive]].  (In fact, we can use these to deduce that $x \leq y$ iff every proximal neighbourhood of $\{y\}$ is a proximal neighbourhood of $\{x\}$, which is manifestly reflexive and transitive.)  Therefore, $\leq$ is a [[preorder]].

If the quasiproximity satisfies Symmetry, then this preorder is [[symmetric relation|symmetric]] and hence an [[equivalence relation]].

Regardless of Symmetry, a (quasi)-proximity space is separated iff this preorder is the [[equality relation]].  That is, $x = y$ if $x$ belongs to every proximal neighbourhood of $\{y\}$, or equivalently if every proximal neighbourhood of $\{y\}$ is a proximal neighbourhood of $\{x\}$, or equivalently if $\{x\}$ is near $\{y\}$, or equivalently if $\{x\}$ is not apart from $\{y\}$.  This may be viewed as a converse of simplified Reflexivity, which states that $\{x\} \;\delta\; \{y\}$ whenever $x = y$.

Conversely, given a set equipped with a preorder $\leq$, let $A \;\delta\; B$ if $x \leq y$ for some $x \in A$ and some $y \in B$, or equivalently let $A \bowtie B$ if $x \leq y$ for no $x \in A$ and no $y \in B$, or equivalently let $A \ll B$ if $x \leq y$ for $x \in A$ implies $y \in B$.  Then we have a quasiproximity space which is symmetric iff $\leq$ is.

In this way, we get the category $Proset$ of preordered sets as a [[reflexive subcategory]] of $QProx$, with the category $SymPreOrd$ of [[symmetric prosets]] (sets equipped with equivalence relations) as a reflexive subcatgory of $Prox$.

In [[constructive mathematics]], a quasi-proximal nearness space (despite its general unreasonableness) or neighborhood space gives rise to a preordered set as above, while a proximal apartness space yields an [[inequality relation]] that is an [[apartness relation]] if we have Local Decomposability.


### Topological spaces

Every proximity space is a [[topological space]]; let $x$ belong to the closure of $A \subseteq X$ iff $\{x\} \;\delta\; A$, or equivalently let $x$ belong to the interior of $A$ iff $\{x\} \ll A$.  This topology is always [[completely regular space|completely regular]], and is [[Hausdorff space|Hausdorff]] (hence [[Tychonoff space|Tychonoff]]) iff the proximity space is separated; see [[separation axiom]].  Proximally continuous functions are [[continuous map|continuous]] for the induced topologies, so we have a functor $Prox \to Top$ over $Set$.

Conversely, if $(X,\tau)$ is a completely regular topological space, then for any $A, B \subseteq X$ let $A \bowtie B$ iff there is a continuous function $f: X\to [0,1]$ such that $f(x) = 0$ for $x \in A$ and $f(x) = 1$ for $x \in B$.  This defines a proximity structure on $X$, which induces the topology $\tau$ on $X$, and which is separated iff $\tau$ is a Hausdorff (hence Tychonoff) topology.

In general, a completely regular topology may be induced by more than one proximity.  However, if it is moreover [[compact topological space|compact]], then it has a unique compatible proximity, given above.  In the case of a [[compact Hausdorff space]] (or more generally any [[normal regular space]]), we then have $A \ll B$ iff $Cl(A) \subseteq Int(B)$.

The construction of a topology works just as well for a quasi-proximity, but the result is no longer necessarily completely regular.  In fact, every topology can be induced by some quasi-proximity: define $A \ll B$ if $A \subseteq int(B)$.  Moreover, in this way topological spaces can be identified with (left) perfect quasi-proximity spaces.

In [[constructive mathematics]], the three now-inequivalent kinds of (quasi-)proximity space (nearness, apartness, and neighborhood) yield three inequivalent notions of topological space: [[closure operators]], [[point-set apartness spaces]], and [[topological spaces]] (equivalently [[neighborhood]] spaces).  Note in particular that the Transitivity axiom ensures that (in the three cases) the closure of a set is closed, that the final axiom of a point-set apartness space holds (if $x\bowtie A$ then $x\bowtie \{ y \mid \neg(y\bowtie A) \}$), and that the interior of a set is open.  Hence, we can identify left perfect quasi-proximal apartness or neighborhood spaces with point-set apartness spaces and topological spaces respectively, by defining $A \ll B$ if $A \subseteq int(B)$ as above in the second case, and $A\bowtie B$ if $x\in A \Rightarrow x\bowtie B$ in the first.

If a quasi-proximal apartness or neighborhood space satisfies Local Decomposability, then its underlying point-set apartness space or topological space is [[locally decomposable space|locally decomposable]] (hence the name for the former axiom).  Conversely, the canonical quasi-proximial apartness or neighborhood space obtained from a point-set apartness space or topological space satisfies Local Decomposability if the original space was locally decomposable.

Unlike in the classical case, the topology underlying a proximity space (which, recall, includes Symmetry) apparently need not be [[completely regular space|completely regular]] or even [[regular space|regular]].  However, we can say:

+--{: .un_theorem}
###### Theorem
Let $X$ be a proximal apartness or neighborhood space (with Symmetry).  Then:

* If $X$ satisfies Local Decomposability, its underlying topological space is regular.
* If $X$ satisfies Decomposability and [[countable choice]] holds, then its underlying topological space is completely regular.
=--
+--{: .proof}
###### Proof
Suppose first that $X$ is a Locally Decomposable proximal neighborhood space and $U$ is an open set containing $x$, which means $\{x\} \ll U$.  By Local Decomposability, we have sets $C$ and $D$ such that $\{x\} \ll C$ and $D\ll U$ and $X = D \cup C^{\mathsf{c}}$.  Transitivity then gives us a set $B$ with $\{x\} \ll B \ll C$, and Symmetry then tells us that $C^{\mathsf{c}} \ll B^{\mathsf{c}}$.  Let $V = int(B^{\mathsf{c}})$ and $W = \int(B)$; then $V\cap W = \emptyset$, $W$ is an open neighborhood of $x$, and $X = D \cup C^{\mathsf{c}} \subseteq U \cup V$.  Thus, $X$ is regular.

Now suppose $X$ is a Decomposable proximal neighborhood space and we have countable choice.  Then given any opens $A,B$ with $A\ll B$, essentially the same proof as above shows that $A$ is "well-inside" $B$.  Thus, applying Transitivity repeatedly (making countably many choices) we can obtain a "scale" of interpolating well-inside open subsets indexed by (dyadic) rational numbers, and thereby a function $f:X\to \mathbb{R}$ separating $A$ and $B$, as in the classical proof of Urysohn's lemma.  (With only Transitivity instead of Decomposability, we would obtain only a function valued in the [[lower real numbers|lower]] or upper real numbers, rather than the [[located real numbers]].)

The arguments for proximal apartness spaces are essentially the same.
=--

Conversely, if $X$ is a completely regular topological space, then the above definition that $A \bowtie B$ iff they are separated by a continuous function $f: X\to [0,1]$ is also constructively valid, and produces a proximity space satisfying Symmetry and Decomposability.


### Uniform spaces {#Uniform}

If $Y$ is a [[uniform space]], then for all $A, B \subseteq Y$ let $A \;\delta\; B$ iff $V \cap (A \times B)$ is [[inhabited set|inhabited]] for every [[entourage]] (aka vicinity) $V$. This defines a biperfect proximity structure on $Y$.  In terms of the other relations, this means $A\bowtie B$ iff $V \cap (A \times B) = \emptyset$ for some entourage $V$, and $A\ll B$ iff $V[A] \subseteq B$ for some entourage $V$, where $V[A] = \{ y \mid \exists x\in A, (x,y)\in V \}$.

[[uniformly continuous map|Uniformly continuous functions]] are proximally continuous for the induced proximities, so we have a functor $Unif \to Prox$ over $Set$.  Moreover, the composite $Unif \to Prox \to Top$ is the usual "underlying topology" functor of a uniform space, i.e. the topology induced by the uniformity and the topology induced by the proximity structure are the same.

Conversely, if $X$ is a proximity space, consider the family of sets of the form
$$ \bigcup_{k=1}^n (A_k \times A_k) $$
where $(A_k)_k$ is a [[list]] (a finite family) of sets such that there exists a same-length list of sets $(B_k)_k$ with $B_k \ll A_k$ and $X = \bigcup_{k=1}^n B_k$.  These sets form a base for a [[totally bounded uniformity]] on $X$, which induces the given proximity.

In fact, this is the *unique* totally bounded uniformity which induces the given proximity: every proximity-class of uniformities contains a unique totally bounded member.  Moreover, a proximally continuous function between uniform spaces with totally bounded [[codomain]] is automatically uniformly continuous.  Therefore, the forgetful functor $Unif \to Prox$ is a left adjoint, whose right adjoint also lives over $Set$, is [[fully faithful functor|fully faithful]], and has its [[essential image]] given by the totally bounded uniform spaces.

In general, proximally continuous functions between given uniform spaces need not be uniformly continuous.  But in addition to total boundedness of the codomain, a different sufficient condition is that the domain be a [[metric space]].

The relation between quasi-uniformities and quasi-proximities is similar.

In [[constructive mathematics]], all three of the relations $\delta,\bowtie,\ll$ may be defined as above from a uniformity.  All the axioms of all three kinds of proximity are then provable, except Binary Additivity for $\delta$, Strong Symmetry for $\ll$, and (Local) Decomposability.  Local Decomposability follows from [[uniform regularity]] for the uniform space, but Decomposability seems unobtainable in this way; it seems to assert [[located subspace|locatedness]] of all subsets.

Moreover, constructively not every $\bowtie$- or $\ll$-proximity is induced by a uniformity in this way.  Consider, on an inhabited set $X$, the relation $A\bowtie B$ defined to mean $A = \emptyset \vee B=\emptyset$.  This is a $\bowtie$-proximity, but if it is induced by a uniformity, then [[weak excluded middle]] holds.  To see this, given a proposition $P$, fix $\xi\in X$ and let $A = \{ x \mid x=\xi \wedge P\}$ and $B = \{x \mid x=\xi \wedge \neg P\}$.  Then $A\times B = \emptyset$, hence $A\bowtie B$ in any proximity defined from a uniformity; but to say $A = \emptyset \vee B=\emptyset$ is weak excluded middle for $P$.  (This example is from [Bridges and Vita](#BridgesVita).)

However, there is a different way to obtain a proximity underlying a uniformity: define $A\bowtie B$ if there is a uniformly continuous function $f: X\to [0,1]$ such that $f(x) = 0$ for $x \in A$ and $f(x) = 1$ for $x \in B$.  Classically, this is equivalent to the usual definition, by the usual proof that any uniform space is completely regular.  Constructively, it (and a similar definition for $\ll$) yields a proximity space satisfying Decomposability, which has the same underlying topology *if* our original uniform space was already [[completely regular space|completely regular]].  It seems possible that at least with [[countable choice]], we could show that every Decomposable proximity space arises from a uniform space in this way.

### Syntopogenous spaces

A proximity space can be identified with a [[syntopogenous space]] which is both *simple* and *symmetric*, and similarly a quasi-proximity space can be identified with one that is just simple.  The relations with topological spaces and uniform spaces can then be seen as coreflections inside the category of syntopogenous spaces; see [[syntopogenous space]].


### Compactifications

The (separated) proximities inducing a given (Hausdorff) completely regular topology can be identified with (Hausdorff) [[compactifications]] of that topology.  The compactification corresponding to a proximity on $X$ is called its __Smirnov compactification__.  The points of this compactification can be taken to be __clusters__ in $X$, which are defined to be collections $\sigma$ of subsets of $X$ such that

1. If $A \in \sigma$ and $B \in \sigma$, then $A \;\delta\; B$.
2. If $A \;\delta\; C$ for all $C \in \sigma$, then $A \in \sigma$.
3. If $(A \cup B) \in \sigma$, then $A \in \sigma$ or $B \in \sigma$.
4. $\sigma$ is nonempty.

Note that conditions (1) and (2), together with Isotony for $\delta$, imply that any cluster $\sigma$ is upwards-closed.  Together with nullary Additivity for $\delta$, they also imply the nullary version of (3): $\emptyset \notin\sigma$.  However, a cluster is not generally a [[filter]]: it is not closed under binary intersections.  This is most obvious when we consider how $X$ embeds in its compactification, taking each point $x$ to the "principal cluster" $\sigma_x = \{ A \mid \{x\}\;\delta\; A \}$, i.e. the collection of sets whose closure contains $x$, which is certainly not generally closed under intersections.  (If it were a filter, of course, condition (3) would say that it is prime.)


## Proximities as profunctors {#profunctors}

As a [[poset]], the [[power set]] $\mathcal{P}X$ of $X$ may be regarded as a [[category]] [[enriched category|enriched]] over [[truth values]].  There is a notion of a [[bimodule]] over a category, also called (more specifically) a distributor or [[profunctor]].

Then a profunctor from $\mathcal{P}X$ to itself is precisely a binary relation $\ll$ on subsets of $X$ that satisfies Isotony.  Adding Reflexivity makes it a co-[[pointed object|pointed]] profunctor, and Transitivity morally makes it a [[coassociative coalgebra]] with Reflexivity as counit.  (Actually, coassociativity is trivial when enriched over truth values, as is the claim that Reflexivity, once it exists, is a counit, but we say 'coassociative' to clarify which sense of 'coalgebra' we mean.)

The sense in which Transitivity makes this a coalgebra is actually a bit involved, and it only quite works because of Additivity.  A coalgebra with a given profunctor $\ll$ as its underlying bimodule has the *structure* of an operation that, given $x \ll z$, takes this to an equivalence class of $y$ such that $x \ll y \ll z$, where $y$ is equivalent to $y'$ if $y \subseteq y'$ (or by any equivalence that follows).  By Isotony and left binary Additivity, $x \ll y \cup y' \ll z$ (or use right Additivity and $y \cap y'$); since $y, y' \subseteq y \cup y'$, we have the desired equivalence.

This suggests that if we want a notion of proximity *without* Additivity, then Transitivity must become more complicated, being a [[extra structure|structure]] rather than just a property (and a structure that should be preserved by proximal maps).

As for Additivity itself, this presumably corresponds to something more general in the world of profunctors related to [[limits]] and [[colimits]], but I haven\'t figured it out yet.

Symmetry probably doesn\'t fit into this picture very well, but who knows?


## Related concepts

[[!include generalized uniform structures - table]]


## References

*  R. Engelking, _General topology_, chapter 8.

*  [[Douglas Bridges]], Peter Schuster, and Luminita Vita, _Apartness, topology, and uniformity: a constructive view_, [pdf](http://www.math.canterbury.ac.nz/mathlsv/dagstuhl01.pdf)

* {#BridgesVita} [[Douglas Bridges]] and Luminita Vita, *Apartness and Uniformity: a constructive development* 

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

[[!redirects set-set apartness space]]
[[!redirects set-set apartness spaces]]
[[!redirects set–set apartness space]]
[[!redirects set–set apartness spaces]]
[[!redirects set--set apartness space]]
[[!redirects set--set apartness spaces]]
[[!redirects set-set apartness structure]]
[[!redirects set-set apartness structures]]
[[!redirects set–set apartness structure]]
[[!redirects set–set apartness structures]]
[[!redirects set--set apartness structure]]
[[!redirects set--set apartness structures]]
[[!redirects set-set apartness relation]]
[[!redirects set-set apartness relations]]
[[!redirects set–set apartness relation]]
[[!redirects set–set apartness relations]]
[[!redirects set--set apartness relation]]
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

[[!redirects topogeny]]
[[!redirects topogenies]]
[[!redirects symmetric topogeny]]
[[!redirects symmetric topogenies]]

[[!redirects proximally continuous function]]
[[!redirects proximally continuous functions]]

[[!redirects Smirnov compactification]]
[[!redirects Smirnov compactifications]]

[[!redirects proximally regular space]]
[[!redirects proximally regular spaces]]
[[!redirects proximally regular proximity space]]
[[!redirects proximally regular proximity spaces]]
