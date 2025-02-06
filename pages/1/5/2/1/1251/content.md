
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



# Directed colimits
* table of contents
{:toc}

## Abstract definition 

A __directed colimit__ is a [[colimit]] $\underset{\to}\lim F$ of a functor $F\colon J \to C$ whose [[source]] [[category]] $J$ is an (upward)-[[direction|directed set]].

More generally, for $\kappa$ a [[cardinal number|regular cardinal]] say that a **$\kappa$-directed set** $J$ is a [[poset]] in which every subset of cardinality $\lt \kappa$ has an upper bound. Then a colimit over a functor $J \to C$ is called **$\kappa$-directed colimit**.

If the directed set is an [[ordinal]], one speaks of a [[sequential colimit]].

The [[duality|dual]] notion is that of [[codirected limit]], a [[limit]] of a functor whose source is a downward-directed set.


## Terminology

Note that the terminology varies.  Especially in algebra, a directed colimit may be called an '[[inductive limit]]' or '[[direct limit]]'; it\'s also possible to distinguish these so that a direct limit may have an arbitrary (possibly undirected) [[partial order|poset]] as its source.  On the other hand, both terms are often used for arbitrary [[colimits]] as an alternative terminology.  (The corresponding dual terms are '[[projective limit]]' and '[[inverse limit]]' for [[limits]].)

Directed (co)limits were studied in algebra (as inductive and projective limits) before the general notion of limit in category theory.  The elementary definition still seen there follows.


## Concrete definition 

Let $C$ be a [[category]].

An __inductive system__ in $C$ consists of a [[direction|directed set]] $I$, a family $(A_i)_{i: I}$ of objects of $C$, and a family $(f_{i j}: A_i \to A_j)_{i \leq j: I}$ of morphisms, such that:
* $f_{i i}: A_i \to A_i$ is the [[identity morphism]] on $A_i$;
* $f_{i k}: A_i \to A_k$ is the [[composition|composite]] $f_{i j} ; f_{j k}$.

Then an __inductive cone__ of this inductive system is an object $X$ and a family of __inductions__ $\iota_i: A_i \to X$ such that
$$ \iota_i = f_{i j} ; \iota_j .$$

Finally, an __inductive limit__ of the inductive system is an inductive cone $\underset{\to}\lim_i A_i$ (where both $f$ and $\iota$ are suppressed in the notation, each in its own way) which is [[universal property|universal]] in that, given any inductive cone $X$, there exists a unique morphism $u\colon \underset{\to}\lim_i A_i \to X$ such that
$$ \iota_i = \iota_i ; u $$
(where the left-hand $\iota$ is from the cone $X$ and the right-hand $\iota$ is from the limit).

Notice that an inductive system in $C$ consists precisely of a directed set $I$ and a (covariant) [[functor]] from $I$ (thought of as a category) to $C$, while an inductive cone or limit of such an inductive system is precisely a cocone or colimit of the corresponding functor.  So this is a special case of [[colimit]].

As with other colimits, an inductive limit, if any exists at all, is unique up to a given isomorphism, so we speak of [[generalized the|the]] inductive limit of a given inductive system.


## Properties {#properties}

According to 1.5 and 1.21 in the [[Locally Presentable and Accessible Categories|book]] by [[Jiří Adámek]] & [[Jiří Rosický]], a category has $\kappa$-directed colimits iff it has $\kappa$-[[filtered colimit|filtered]] ones, and a functor preserves $\kappa$-directed colimits iff it preserves $\kappa$-filtered ones.

The fact that directed colimits suffice to obtain all filtered ones may be regarded as a convenience similar to the fact that all [[colimits]] can be constructed from [[coproducts]] and [[coequalizers]].


## Applications 

### In algebra

An inductive limit in algebra is usually defined as a [[quotient object|quotient]] of a [[disjoint union]].  To be precise, $\underset{\to}\lim_i A_i$ is the disjoint union $\biguplus_{i: I} A_i$ with $x: A_i$ identified with $y: A_j$ if
$$ f_{i k}(x) = f_{j k}(y) $$
for some $k$.  Here it is important that $C$ is a [[concrete category]] and that $I$ is a directed set (rather than merely a [[partial order|poset]]); this construction doesn\'t generalise very well.


### In accessible category theory 

The objects of an [[accessible category]] and of a [[presentable category]] are $\kappa$-directed limits over a given set of generators. 


## Examples 

A [[Pruefer group]] $Z_{p^\infty}$ (for $p$ a [[prime number]]) is an inductive limit of the [[cyclic group]]s $Z_{p^n}$ (for $n$ a [[natural number]]).  Here, $C$ is the category of [[group]]s, $I$ is the directed set of natural numbers, $A_i = Z_{p^i}$, and $f_{i j}: A_i \to A_j$ is induced by multiplication by $p$ (which must be proved well defined on $Z_{p^i}$ for $i \leq j$).

A [[stalk]] $F_x$ (for $F$ a [[sheaf]] on a [[topological space]] $S$ and $x$ an element of $S$) is an inductive limit of $F(U)$ (for $U$ an open neighbourhood of $x$).


## Related concepts

* [[filtered colimit]]

[[!redirects directed colimit]]
[[!redirects directed colimits]]
[[!redirects Directed colimits]]
