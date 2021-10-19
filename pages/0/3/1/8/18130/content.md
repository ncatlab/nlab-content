
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[topological space]] $(X,\tau)$ is called a _Kolmogorov space_ if it satisfies the $T_0$-[[separation axiom]], hence if for $x_1 \neq x_2 \in X$ any two distinct points, then at least one of them has an [[open neighbourhood]] $U_{x_i} \in \tau$ which does not contain the other point.

[[!include main separation axioms -- table]]

## Properties
 {#Properties}


[[!include main separation axioms -- as lifting properties]]


### Reflection

+-- {: .num_prop #KolmogorovQuotient}
###### Proposition
**(Kolmogorov quotient)**

Let $(X,\tau)$ be a [[topological space]]. Consider the [[relation]] on the underlying set
by which $x_1 \sim x_1$ precisely if neighther $x_i$ has an [[open neighbourhood]] not containing the other.
This is an [[equivalence relation]]. The [[quotient topological space]] $X \to X/\sim$ by this
equivalence relation is a $T_0$-space. 

This construction is the reflector exhibiting Kolmogorov spaces as a [[reflective subcategory]] of the [[category]] [[Top]] of all topological spaces.

=--

## Related concepts

* [[Hausdorff topological space]]

* [[nice topological space]]

## References

* Wikipedia, _[Kolmogorov space](https://en.wikipedia.org/wiki/Kolmogorov_space)_


[[!redirects T0]]
[[!redirects T_0]]

[[!redirects Kolmogorov space]]
[[!redirects Kolmogorov spaces]]
[[!redirects T0 space]]
[[!redirects T0 spaces]]
[[!redirects T0-space]]
[[!redirects T0-spaces]]
[[!redirects T_0 space]]
[[!redirects T_0 spaces]]
[[!redirects T_0-space]]
[[!redirects T_0-spaces]]

[[!redirects Kolmogorov topological space]]
[[!redirects Kolmogorov topological spaces]]
[[!redirects T0 topological space]]
[[!redirects T0 topological spaces]]
[[!redirects T_0 topological space]]
[[!redirects T_0 topological spaces]]
[[!redirects T0-topological space]]
[[!redirects T0-topological spaces]]
[[!redirects T_0-topological space]]
[[!redirects T_0-topological spaces]]

[[!redirects Kolmogorov quotient]]
[[!redirects Kolmogorov quotients]]
[[!redirects T0 quotient]]
[[!redirects T0 quotients]]
[[!redirects T0-quotient]]
[[!redirects T0-quotients]]
[[!redirects T_0 quotient]]
[[!redirects T_0 quotients]]
[[!redirects T_0-quotient]]
[[!redirects T_0-quotients]]
