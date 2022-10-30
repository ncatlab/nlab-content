
# Eventuality filters
* table of contents
{: toc}

## Idea

Eventuality filters are the key translation between [[filters]] and [[nets]] (particularly in [[topology]]).  Specifically:
*  Given a net $n$ (or in particular a [[sequence]]) in a [[set]] $X$, the eventuality filter of $n$ is a [[proper filter]] on $X$;
*  Every proper filter on $X$ is the eventuality filter of some net in $X$;
*  Two nets are equivalent for purposes of [[convergence]] (meaning precisely that they are [[subnets]] of each other in the sense of &#197;rnes & Anden&#230;s) if and only if their eventuality filters are equal.

This last point is not so much a result as the *definition* of the subnet relation (or at least of its [[symmetric relation|symmetrisation]], the relation of equivalence of nets).  One still needs to check that every use of nets in topology (or other fields) actually respects this notion of equivalence of nets, if one wishes to convert nets to filters.


## Definition

Let $X$ be a [[set]], let $D$ be a [[directed set]], and let $n$ be a [[function]] from $D$ to $X$, so that $n$ is a [[net]] in $X$.  Given a [[subset]] $A$ of $X$, $n$ is __eventually__ in $A$ if, for some $i$ in $D$, for each $j \geq i$ in $D$, $n_j \in A$.  The collection $F_n$ of all those subsets $A$ such that $x$ is eventually in $A$ is a [[proper filter]] on $X$, called the __eventuality filter__ of $n$.

In symbols,
$$ F_n \coloneqq \{ A \subseteq X \;|\; \ess \forall\, j,\; n_j \in A \} ,$$
where $\ess \forall\, j$ is read 'for essentially each $j$' or 'eventually for each $j$' and means $\exists\, i,\; \forall j \geq i$.  In the case where $D$ is the set of [[natural numbers]] directed by $\leq$, so that $n$ is an [[infinite sequence]] ($\omega$-sequence) in $X$, then $\ess \forall\, j$ may be read as 'for all but finitely many $j$'.


## Converse

Given a [[filter]] $F$ on $X$, let $D$ be the [[binary relation]] $\in_X$ restricted to $F$, viewed as a subset of the [[cartesian product]] $X \times F$, [[preorder|ordered]] so that $(y, A) \leq (z, B)$ means simply that $B \subseteq A$.  Let $n\colon D \to X$ map $(y, A)$ simply to $y$.  Then $D$ is [[direction|directed]] (so that $n$ is a net in $X$) iff $F$ is [[proper filter|proper]]; and in that case, the eventuality filter of the net $n$ is $F$.

It is possible to define $D$ as ${{\in_X}|_F} \times \mathbb{N}$ (instead of as ${\in_X}|_F$ as done above) so that the direction on $D$ is a [[partial order]], if one really wants to.  (Then $(y, A, i) \leq (z, B, j)$ means that $B \subseteq A$, $i \leq j$, and $y = z$ if $i = j$.)


[[!redirects eventuality filter]]
[[!redirects eventuality filters]]

[[!redirects eventuality]]
[[!redirects eventualities]]
[[!redirects eventual]]
[[!redirects eventually]]
