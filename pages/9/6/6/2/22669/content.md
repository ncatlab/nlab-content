


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

For $\lambda$ a [[partition]]/[[Young diagram]], its Plancherel probability is (see at *[[hook length formula]]*):

$$
  p_\lambda
  \;\coloneqq\;
  \frac
    {
      \big(
        dim(S^{(\lambda)}) 
      \big)^2
    }
    {n!}
  \;=\;
  n!
  \underset{
    { 1 \leq i \leq rows(\lambda) }
    \atop
    { 1 \leq j \leq \lambda_i }
  }{\prod}
  \frac{1}{ \big(\ell hook_\lambda(i,j)\big)^2 }
  \,,
$$

where 

* $S^{(\lambda)}$ denotes the [[complex numbers|complex]] [[irrep]] of the [[symmetric group]] that is labelled by $\lambda$ via the [[representation theory of the symmetric group]] (the $\lambda$th [[Specht module]])
 
* $\ell hook_\lambda(i,j)$ denotes the *hook length* at the $(i,j)$-box in the Young diagram $\lambda$.

## Related concepts

* [[Schur-Weyl measure]]

* [[hook length formula]]


## References

* Maciej Dołęga, *Central limit theorem for random Young diagrams with respect to Jack measure* 2014 ([pdf](https://www.impan.pl/~mdolega/papers/CLT.pdf))

See also:

* Wikipedia, [Plancherel measure](https://en.wikipedia.org/wiki/Plancherel_measure)

In relation to [[matrix models]]:

* Suvankar Dutta, Debangshu Mukherjee, Neetu, Sanhita Parihar, *A Unitary Matrix Model for q-deformed Plancherel Growth* ([arXiv:2105.09342](https://arxiv.org/abs/2105.09342))

[[!redirects Plancherel measures]]
