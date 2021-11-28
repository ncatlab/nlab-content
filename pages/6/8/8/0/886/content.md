
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Total relations
* table of contents
{: toc}

## Idea

A _total relation_ is a [[binary relation]] on a set with the property that distinguishes the [[total orders]] among the [[partial orders]].


## Terminology

An [[entire relation]] is sometimes called 'total', but these are unrelated concepts.  The 'total' there is in the sense of a total (as opposed to [[partial function|partial]]) [[function]], while the 'total' here is in the sense of a total (as opposed to partial) [[order]].

A total relation is necessarily [[reflexive relation|reflexive]].  For an [[irreflexive relation|irreflexive]] version, see _[[connected relation]]_.  In [[classical mathematics]], total relations and connected relations are equivalent concepts, since either may be constructed from the other by changing every truth value of the form $x \sim x$, and so the distinction is not always maintained.


## Definitions

A [[binary relation]] $R$ on a set $A$ is __total__ if any two elements are related in one order or the other:
$$ \forall (x, y: A),\; x \sim_R y \;\vee\; y \sim_R x .$$
In other words, $R$ is __total__ if its [[union]] with its [[reverse relation|reverse]] is the [[universal relation]]:
$$ A \times A \subseteq R \cup R^{op} .$$
(Of course, this containment is in fact an equality.)  In this way, the concept can be generalized from [[Rel]] to any $2$-[[2-poset|poset]]-[[2-poset with duals|with-duals]]; part of the definition then becomes the requirement that the union $R \cup R^{op}$ exists.

In [[constructive mathematics]], we can distinguish between a __strongly total__ relation, defined as above, and a __weakly total__ relation:
$$ \forall (x, y: A),\; \neg(x \sim_R y) \;\Rightarrow\; y \sim_R x .$$
(In theory, this should be conjoined with $\neg(y \sim_R x) \Rightarrow x \sim_R y$, but this follows because the original definition is symmetric in $x$ and $y$.)
This can also be expressed in $Rel$ using the weak union $\parr$ instead of $\cup$ and generalized to other $2$-posets with the structure to support this operation.
We can define an even weaker notion:
$$ \forall (x, y: A),\; \neg(x \sim_R y) \;\Rightarrow\; \neg\neg(y \sim_R x) ,$$
which is based on using the [[double negation]] of union in $Rel$, but I\'m not sure that anyone uses this in practice.

We can also let $R$ be a [[disjoint pair]] of relations, denoted $R^+$ and $R^-$ or (more suggestively) $\sim_R$ and $\nsim_R$, related according to the [[antithesis interpretation]] of [[linear logic]] within constructive mathematics, which requires that
$$ \forall (x, y: A),\; x \nsim_R y \;\Rightarrow\; \neg(x \sim_R y) $$
(but not the converse).  Then $R$ is __weakly total__ if additionally
$$ \forall (x, y: A),\; (x \nsim_R y \;\Rightarrow\; y \sim_R x) .$$
It\'s __strongly total__ if, in addition to all of the above,
$$ \forall (x, y: A),\; x \sim_R y \;\vee\; y \sim_R x .$$
This can all be expressed in a $2$-poset of disjoint pairs of relations equipped with strong ($\uplus$) and weak ($\parr$) notions of union.


## Properties

A [[total order]] is precisely a [[partial order]] that is total in the sense of this article.

In classical logic, $R$ is total if and only if $R = \dot{R} \cup \Delta_A$ for some [[connected relation]] $\dot{R}$, and then $\dot{R}$ must be $R \setminus \Delta_A$.  (Here, $\Delta_A$ is the [[equality relation]] on the set $A$.)

Totality is antithetical to [[asymmetric relation|asymmetry]].  In [[classical logic]], this means that $R$ is total if and only if its [[negation]] is asymmetric.  More generally, in terms of the [[antithesis interpretation]], the disjoint pair $R = (R^+,R^-)$ is strongly/weakly total if and only if its formal negation $R^\bot = (R^-,R^+)$ is strongly/weakly asymmetric.

In particular, $R^-$ is asymmetric in its own right whenever a disjoint pair $(R^+,R^-)$ is weakly total.  Conversely, a disjoint pair $(R^+,R^-)$ is strongly total if (and only if) $R^+$ is strongly total in its own right and $R^-$ is asymmetric in its own right.


[[!redirects total relation]]
[[!redirects total relations]]
