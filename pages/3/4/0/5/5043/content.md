
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Cofinal diagrams
* table of contents
{: toc}

## Definition

A [[pair]] of [[diagrams]] $D,D'$ in a [[category]] $C$ (e.g.: directed systems, sub-posets, ... ) are **cofinal** if they have *equivalent [[colimits]]*. 

In most cases where the word "cofinal" is used, it seems to be the case $D'$ is a subdiagram of $D$ in whatever sense of subdiagram appears suitable.  In that case the cofinality is equivalent to the inclusion [[functor]] being a **[[cofinal functor]]**.


As defined above, no relation is posited between $D$ and $D'$, and so it seems not too much in violation of the [[principle of equivalence]] to define cofinalness[^1] as "a single object is a colimit for both diagrams".


It is *not* said that they are final if they have equivalent *[[limits]]* --- the "co"s are not freely mutable, although the dual situation is doubtless just as interesting.


## Examples

* Let $D' = D F$, and let $L\colon D \times (0 \to 1) \to C$ be an initial cocone over $D$; it seems natural to ask that $L \circ (F \times (0 \to 1))$ be an initial cocone over $D'$.

* Nonempty subsets of a finite [[total order]] are cofinal iff they have the same maximum.

* Every infinite subset of $\omega$ is cofinal with $\omega$, as diagrams in $\omega + 1$.



## Related concepts

* [[cofinal functor]]

* [[homotopy final functor]]

* [[final (∞,1)-functor]]


[^1]: [[cofinality|Cofinality]] is an ordinal invariant of [[ordinals]], which doesn't make sense in the present generality, so we need another name for the adjective.


[[!redirects cofinal diagram]]

