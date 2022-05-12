
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition ##

A [[protoring]] $M$ is an **archimedean protoring** if for all terms $a, b, c, d \in M$, $c \lt d$ implies that there exists a positive [[natural number]] $n \in \mathbb{N}_+$ such that 

$$b + \sum_{i=1}^n c \lt a + \sum_{i=1}^n d$$

where 

$$\sum_{i=1}^{(-)} (-):\mathbb{N}_+ \times M \to M$$ 

is the canonical left non-unital $\mathbb{N}_+$-[[action]] for [[commutative semigroups]] defined inductively by 

$$\sum_{i=1}^{1} c \coloneqq c$$

$$\sum_{i=1}^{n + 1} c \coloneqq c + \sum_{i=1}^{n}$$

## See also ##

* [[archimedean group]]

* [[archimedean integral domain]]

* [[archimedean difference protoring]]

* [[protoring]]

## Examples ##

* Every [[archimedean integral domain]] is a archimedean protoring. 

## References

* Davorin Lešnik, Synthetic Topology and Constructive Metric Spaces, ([arxiv:2104.10399](https://arxiv.org/abs/2104.10399))

[[!redirects archimedean protorings]]
[[!redirects Archimedean protoring]]
[[!redirects Archimedean protorings]]