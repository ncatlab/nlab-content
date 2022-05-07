


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[probability distribution]] on [[Young diagrams]].

## Definition

For $\lambda$ a [[partition]]/[[Young diagram]], its Plancherel probability is (compare the [[hook length formula]]):

$$
  p_\lambda
  \;\coloneqq\;
  n!
  \underset{
    { 1 \leq i \leq rows(\lambda) }
    \atop
    { 1 \leq j \leq \lambda_i }
  }{\prod}
  \frac{1}{ \big(\ell hook_\lambda(i,j)\big)^2 }
  \,.
$$

## Related concepts

* [[Schur-Weyl measure]]

* [[hook length formula]]


## References

* Maciej Dołęga, *Central limit theorem for random Young diagramswith respect to Jack measure* 2014 ([pdf](https://www.impan.pl/~mdolega/papers/CLT.pdf))

[[!redirects Plancherel measures]]
