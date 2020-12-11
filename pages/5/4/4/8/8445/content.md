
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $N$ a [[module]] (over some [[ring]] $R$) and $S \hookrightarrow N$ a submodule, then the corresponding _quotient module_ $N/S$ is the mdoule where all elements in $N$ that differ by n element in $S$ are identified.

If the ring $R$ is a [[field]] then $R$-modules are called _[[vector spaces]]_ and quotient modules are called _quotient vector spaces_.

## Definition

Thoughout let $R$ be some [[ring]]. Write $R$[[Mod]] for the [[category]] of [[module]]s over $R$. Write $U:R Mod \to$ [[Set]] for the [[forgetful functor]] that sends a module to its underlying [[set]].

+-- {: .num_defn}
###### Definition

For $i : K \hookrightarrow N$ a [[submodule]], the **quotient module** $\frac{N}{K}$ is the [[quotient group]] of the underlying groups, equipped with the $R$-[[action]] induced by that on $N$.

=--

## Properties

### Equivalent characterizations

+-- {: .num_prop}
###### Proposition

The quotient module is equivalently the [[cokernel]] of the inclusion in $R$[[Mod]]

$$
  \frac{N}{K} \simeq coker(i)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The quotient module is equivalently the [[quotient object]] of the [[congruence]] $N \oplus K \to N \oplus N$ given by projection on the first factor and by addition in $N$.

=--

## Related concepts

* [[quotient group]]

* [[quotient ring]]

[[!redirects  quotient modules]]

[[!redirects quotient vector space]]
[[!redirects quotient vector spaces]]
