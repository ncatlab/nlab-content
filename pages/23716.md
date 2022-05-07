[[!redirects function limit spaces]]
[[!redirects Hausdorff function limit space]]
[[!redirects Hausdorff function limit spaces]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A very general structure where the concept of [[limit of a function]] makes sense. 

## Definition ##

A __function limit space__ is a set $T$ such that for all [[subsets]] $S \subseteq T$, there is a ternery relation on the Cartesian product $(S \to T) \times S \times T$
$$ f(x) \underset{x \to c}{\to} L $$
for $f:S \to T$, $c \in S$, and $L \in T$. 

### Hausdorff function limit spaces ###

A __Hausdorff function limit space__ is a set $T$ such that for all [[subsets]] $S \subseteq T$, there is a [[partial function]] 
$$\lim_{x \to (-)} (-)(x): S \times (S \to T) \to T$$ 

## See also ##

* [[limit of a function]]

* [[pointwise continuous function]]

* [[algebraic limit field]]