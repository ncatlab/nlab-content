
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A notion of [[entropy]]. 

In the context of [[probability theory]], the **min-entropy** of a discrete probability distribution is the negative [[logarithm]] of the probability of the most likely outcome. It is never greater than the ordinary [entropy](entropy#entropy_of_a_partition_of_a_discrete_probability_space) of that distribution.

For a [[quantum system]] with [[density matrix]] $\rho$, the min-entropy is minus the [[logarithm]] of the [[maximum]] of its [[operator spectrum]], hence (since density matrices are [[self-adjoint operators]]) of its [[operator norm]] (which in the case of a [[finite-dimensional vector space|finite-dimensional]] [[space of states]] this is the maximum [[eigenvalue]]):

$$
  S_{min}(\rho)
  \;\coloneqq\;
  -
  ln 
  \Big(
    max
    \big(
       Spectrum(\rho)
    \big)
  \Big)
  \;=\;
  -
  ln
  \big(
    \left\Vert
      A
    \right\Vert
  \big)
  \,.
$$

(e.g. [Chen 19, Def. 5.2.2](#Chen19))


## Related entries

* [[max-entropy]]

## References

Review:

* {#Chen19} Yi-Hsiu Chen, *Computational Notions of Entropy: Classical, Quantum, and Applications*, 2019 ([pdf](https://dash.harvard.edu/bitstream/handle/1/42029772/CHEN-DISSERTATION-2019.pdf?sequence=1&isAllowed=y))

* Robert Koenig, Renato Renner, Christian Schaffner, *The operational meaning of min- and max-entropy*, IEEE Trans. Inf. Th., vol. 55, no. 9 (2009) ([arXiv:0807.1338](https://arxiv.org/abs/0807.1338))

See also:

* Wikipedia, *[Min-entropy](https://en.wikipedia.org/wiki/Min-entropy)*

* Scholarpedia, *[Quantum entropies -- Min entropy](http://www.scholarpedia.org/article/Quantum_entropies#Min_entropy)*

Generalization to condition entropies:

* Fabian Furrer, Johan Åberg, Renato Renner, *Min- and Max-Entropy in Infinite Dimensions*, Communications in Mathematical Physics volume 306, pages 165–186 (2011) ([doi:10.1007/s00220-011-1282-1](https://doi.org/10.1007/s00220-011-1282-1))


In the context of [[holographic entanglement entropy]]:

* [[Ning Bao]], [[Geoffrey Penington]], [[Jonathan Sorce]], [[Aron C. Wall]], Section 2.3 of: _Beyond Toy Models: Distilling Tensor Networks in Full AdS/CFT_,  JHEP 2019:69 ([arXiv:1812.01171](https://arxiv.org/abs/1812.01171))


[[!redirects min-entropy]]
[[!redirects min-entropies]]

[[!redirects min entropy]]
[[!redirects min entropies]]
