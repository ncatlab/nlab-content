
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **(co)sequential limit** is a [[limit]]/[[colimit]] whose [[diagram]] category is the [[opposite poset|opposite]] of a nonzero [[ordinal]] regarded as a [[poset]], regarded as a [[category]]. For instance over a [[tower diagram]]. 

Sometimes the term is used even more specifically for a limit over the opposite of the ordinal $\omega$.

Thus, a sequential limit is a special case of a (co)[[directed limit]]. See there for more details.

## Examples

Sequential limits i.e. the [[tower]]-diagram
$$
  \array{
     && && \lim_{\leftarrow_n} X(n) &&
     \\
     && &\swarrow& \downarrow & \searrow&
     \\
     \cdots & \to & X(2) & \to  & X(1) & \to & X(0)
  }
$$
are extremely common. Classical examples occur in the theory of [[Postnikov towers]] and also in the definition of the [[solenoids]], as well as [[projective limits]]. 

A [[ring]] $ K [ [ x ] ] $ of formal [[power series]] (for $K$ a [[field]]) is a sequential limit of the rings $K[x]/x^n$ (for $n$ a [[natural number]]). 

Similarly, a ring $\mathbf{Z}_p$ of $p$-[[adic integer]]s (for $p$ a [[prime number]]) is a sequential limit of the rings $\mathbf{Z}/p^n$.

A set of infinite [[sequences]] is a sequential limit of sets of [[list|finite sequences]] (which, at the level of [[sets]], includes the above examples).

The [[axiom of dependent choice]] states that given a [[family of sets]] $X_n$ and a family of [[surjections]] $f_n:X_{n + 1} \to X_n$ indexed by natural numbers $n \in \mathbb{N}$: 
$$
  \array{
     && && \lim_{\leftarrow_n} X_n &&
     \\
     && &\swarrow& \downarrow & \searrow&
     \\
     \cdots & \underset{f_2}\to & X_2 & \underset{f_1}\to  & X_1 & \underset{f_0}\to & X_0
  }
$$
the projection function to $X_0$ from the sequential limit $\underset{\leftarrow}\lim X_n$ of the above diagram is a surjection. 

## Related concepts

* [[tower of fibrations]]

* [[lim^1 and Milnor sequences]]

* [[axiom of dependent choice]]

* [[sequential colimit]]

## References

The version of the [[axiom of dependent choice]] using sequential limits can be found in:

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203), [summary](https://felix-cherubini.de/condensed-summary.pdf))

[[!redirects sequential limit]]
[[!redirects sequential limits]]
[[!redirects cosequential limit]]
[[!redirects cosequential limits]]