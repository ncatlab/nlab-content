
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Directed limits
* table of contents
{: toc}

## Abstract definition 

A __directed limit__ (or __codirected limit__) is a [[limit]] $\underset{\leftarrow}\lim F$ of a functor $F\colon J \to C$ whose [[source]] [[category]] $J$ is a downward-[[direction|directed set]].

More generally, for $\kappa$ a [[cardinal number|regular cardinal]] say that a **$\kappa$-directed set** $J$ is a [[poset]] in which every subset of cardinality $\lt \kappa$ has an upper bound. Then a limit over a functor $J \to C$ is called **$\kappa$-directed limit**.

If the directed set is an [[ordinal]], one speaks of a [[sequential limit]].

The [[duality|dual]] notion is that of [[directed colimit]], a [[colimit]] of a functor whose source is a upward-directed set.


## Terminology

Note that the terminology varies.  Especially in algebra, a directed limit may be called a '[[projective limit]]' or '[[inverse limit]]'; it\'s also possible to distinguish these so that an inverse limit may have an arbitrary (possibly undirected) [[partial order|poset]] as its source.  On the other hand, both terms are often used for arbitrary [[limits]] as an alternative to the 'co-' method of distinction.  (The corresponding dual terms are '[[inductive limit]]' and '[[direct limit]]', with no 'co-' even though these are [[colimits]].)

Directed (co)limits were studied in algebra (as projective and inductive limits) before the general notion of limit in category theory.  The elementary definition still seen there follows.


## Explicit definition

Let $C$ be a [[category]].

A __projective system__ in $C$ consists of a [[direction|directed set]] $I$ (which we will write directed-upward as usual), a family $(A_i)_{i: I}$ of objects of $C$, and a family $(f_{ij}: A_j \to A_i)_{i \leq j: I}$ of morphisms, such that:
* $f_{ii}: A_i \to A_i$ is the [[identity morphism]] on $A_i$;
* $f_{ik}: A_k \to A_i$ is the [[composition|composite]] $f_{ij} \circ f_{jk}$.

Then a __projective cone__ of this projective system is an object $X$ and a family of __projections__ $\pi_i: X \to A_i$ such that
$$ \pi_i = f_{ij} \circ \pi_j .$$

Finally, a __projective limit__ of the projective system is a projective cone $\underset{\leftarrow}\lim_i A_i$ (where both $f$ and $\pi$ are suppressed in the notation, each in its own way) which is [[universal property|universal]] in that, given any projective cone $X$, there exists a unique morphism $u\colon X \to \underset{\leftarrow}\lim_i A_i$ such that
$$ \pi_i = \pi_i \circ u $$
(where the left-hand $\pi$ is from the cone $X$ and the right-hand $\pi$ is from the limit).

Notice that a projective system in $C$ consists precisely of a directed set $I$ and a [[contravariant functor]] from $I$ (thought of as a category) to $C$, while a projective cone or limit of such a projective system is precisely a cone or limit of the corresponding functor.  So this is a special case of [[limit]].

As with other limits, a projective limit, if any exists at all, is unique up to a given isomorphism, so we speak of [[generalized the|the]] projective limit of a given projective system.


## In algebra

A projective limit in algebra is usually defined as a [[subobject|subalgebra]] of a [[cartesian product]].  To be precise, $\underset{\leftarrow}\lim_i A_i$ consists of those elements $(x_i)_{i: I}$ of $\prod_{i: I} A_i$ such that:
$$ x_i = f_ij(x_j) .$$
This can be seen as a special case of the construction of an arbitrary limit out of [[product]]s and [[equalizer]]s.


## Examples

Directed limits over the codirected set $(\mathbb{N},\geq)$ of [[natural numbers]], the [[tower]]-diagram,
$$
  \array{
     && && \lim_{\leftarrow_n} X(n) &&
     \\
     && &\swarrow& \downarrow & \searrow&
     \\
     \cdots & \to & X(2) & \to  & X(1) & \to & X(0)
  }
$$
are extremely common. Classical examples occur in the theory of [[Postnikov towers]] and also in the definition of the [[solenoids]].

A [[ring]] $ K [ [ x ] ] $ of formal [[power series]] (for $K$ a [[field]]) is a projective limit of the rings $K[x]/x^n$ (for $n$ a [[natural number]]).  Here, $C$ is the category of rings, $I$ is the directed set of natural numbers, $A_i = K[x]/x^i$, and $f_{ij}: A_j \to A_i$ is induced by the quotient map $K[x] \to K[x]/x^i$ (which must be proved well defined on $K[x]/x^j$ for $i \leq j$).

Similarly, a ring $\mathbf{Z}_p$ of $p$-[[adic integer]]s (for $p$ a [[prime number]]) is a projective limit of the rings $\mathbf{Z}/p^n$.

A set of infinite [[sequences]] is a projective limit of sets of [[list|finite sequences]] (which, at the level of [[sets]], includes the above examples).


[[!redirects directed limit]]
[[!redirects directed limits]]
[[!redirects codirected limit]]
[[!redirects codirected limits]]
