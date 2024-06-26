

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $X \subset \mathbb{R}^n$ be an [[open subset]] of [[Euclidean space]]. One way to state the [[continuous function|continuity]] condition on a [[distribution]] $u$ on $X$ --- being a [[continuous linear functional]] on the space $C^\infty_c(X)$ of [[bump functions]] --- is to require that for all [[compact topological space|compact]] [[subspaces]] $K$ there exist constants $C$ and $k$ such that for any $b\in C^\infty_c(X)$ with [[support of a function|support]] in $K$ the [[absolute value]] of $u(b)$ is bounded by $C$ times the [[suprema]] of the [[sums]] of the [[absolute values]] of all [[derivatives]] of $b$ of order bounded by $k$:

$$
  \underset{ {K \subset X} \atop {\text{compact}}}{\forall}
  \left(
    \underset{ {C_K \in \mathbb{R}} \atop {k_K \in \mathbb{N}} }{\exists}
    \left(
      \underset{b \in C^\infty_c(K)}{\forall}
      \left(
        {\vert u(b) \vert} 
        \leq
        C_K 
        \underset{
          \vert \alpha\vert \leq k_K
        }
        {\sum}
        sup(\partial^\alpha b)
      \right)
    \right)
  \right)
  \,.
$$

+-- {: .num_defn #OrderOfADistribution}
###### Definition
**(order of a distribution)**

The distribution $u \in \mathcal{D}'(X)$ has _order_ $\leq k \in \mathbb{N}$ if $k$ serves as a global choice (valid for all compact $K \subset X$) in the above formula, hence if:

$$
  \underset{ {K \subset X} \atop {\text{compact}}}{\forall}
  \left(
    \underset{ {C_K \in \mathbb{R}}  }{\exists}
    \left(
      \underset{b \in C^\infty_c(K)}{\forall}
      \left(
        {\vert u(b) \vert} 
        \leq
        C_K \underset{\vert \alpha\vert \leq k}{\sum}sup(\partial^\alpha b)
      \right)
    \right)
  \right)
  \,.
$$

If $u$ is of order $\leq k$ for some $k \in \mathbb{N}$, it is said to have _finite order_.


=--

(e.g. [Hoermander 90, def. 2.1.1, below (2.1.2)](#Hoermander90))

## Examples

+-- {: .num_example #CompactLySupportedDistributionsHaveFiniteOrder}
###### Example

Every [[compactly supported distribution]] has finite order.

=--

As a special case of example \ref{CompactLySupportedDistributionsHaveFiniteOrder}:

+-- {: .num_example}
###### Example

A [[point-supported distribution]] is a sum of [[derivatives]] of the [[delta distribution]] at that point. This has order $k$ if the order of the derivatives is bounded by $k$.

=--

([H&#246;rmander 90, theorem 2.3.4](#Hoermander90))

## Related concepts

* [[support of a distribution]]

* [[scaling degree of a distribution]]


## References

* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer (1983, 1990)


[[!redirects order of distributions]]
[[!redirects orders of distributions]]

