
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

A [[binary relation]] $\sim$ on a set $A$ is __total__ if any two elements are related in one order or the other:
$$ \forall (x, y: A),\; x \sim y \;\vee\; y \sim x .$$
In the language of the $2$-[[2-poset|poset]]-[[2-poset with duals|with-duals]] [[Rel]] of sets and relations, a relation $R: A \to A$ is __total__ if its union with its [[reverse relation|reverse]] is the [[universal relation]]:
$$ A \times A \subseteq R \cup R^{op} .$$
(Of course, this containment is in fact an equality.)

In [[constructive mathematics]], we can distinguish between a __strongly total__ relation, defined as above, and a __weakly total__ relation:
$$ \forall (x, y: A),\; \neg(x \sim y) \;\Rightarrow\; y \sim x .$$
(In theory, this should be conjoined with $\neg(y \sim x) \Rightarrow x \sim y$, but this follows because the original definition is symmetric in $x$ and $y$.)
This can also be expressed in the $2$-poset $Rel$ using the weak disjunction $\parr$ instead of $\cup$.
We can define an even weaker notion:
$$ \forall (x, y: A),\; \neg(x \sim y) \;\Rightarrow\; \neg\neg(y \sim x) ,$$
which is based on using the [[double negation]] of union in $Rel$, but it\'s not clear whether anyone uses this for anything.

We can also consider a [[disjoint pair]] of relations $\sim$ and $\nsim$ related according to the [[antithesis interpretation]] of [[linear logic]] within constructive mathematics, which requires that
$$ \forall (x, y: A),\; x \nsim y \;\Rightarrow\; \neg(x \sim y) $$
(but not the converse).  Then this pair is __weakly total__ if additionally
$$ \forall (x, y: A),\; (x \nsim y \;\Rightarrow\; y \sim x) .$$
It\'s __strongly total__ if, in addition to all of the above,
$$ \forall (x, y: A),\; x \sim y \;\vee\; y \sim x .$$
This can all be expressed in a $2$-poset of disjoint pairs of relations with strong ($\cup$) and weak ($\parr$) notions of union.


## Properties

A [[total order]] is precisely a [[partial order]] that is total in the sense of this article.

In classical logic, $\sim$ is total if and only if $(\sim) = (\underset{\neq}\sim) \cup \Delta$ for some [[connected relation]] $\underset{\neq}\sim$, and then $\underset{\neq}\sim$ must be $(\sim) \setminus \Delta$.  (Here, $\Delta$ is the [[equality relation]] on the set $A$.)

Totality is antithetical to [[asymmetric relation|asymmetry]].  In [[classical logic]], this means that $\sim$ is total if and only if its [[negation]] is asymmetric.  More generally, in terms of the [[antithesis interpretation]], the disjoint pair $(\sim,\nsim)$ is strongly/weakly total if and only if $(\nsim,\sim)$ is strongly/weakly asymmetric.

In particular, $\nsim$ is asymmetric in its own right whenever the disjoint pair $(\sim,\nsim)$ is weakly total.  Conversely, a disjoint pair $(\sim,\nsim)$ is strongly total if (and only if) $\sim$ is strongly total in its own right and $\nsim$ is asymmetric in its own right.


[[!redirects total relation]]
[[!redirects total relations]]
