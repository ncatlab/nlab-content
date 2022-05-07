
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

A notion of [[entropy]]. (...)

For finite [[quantum systems]] with [[density matrix]] $\rho$, the min-entropy is the [[logarithm]] of the inverse of its [[maximum]] [[eigenvalue]]:

$$
  S_{min}(\rho)
  \;\coloneqq\;
  ln 
  \left(
    \frac{1}{
      max(\sigma(\rho))
    }
  \right)
  \,.
$$

(see e.g. [Chen 19, Def. 5.2.2](#Chen19)).  Here, $\sigma(\rho)$ is the [[operator spectrum]] of $\rho$, which (in the finite-dimensional case) is the set of eigenvalues.


## References

Review:

* {#Chen19} Yi-Hsiu Chen, *Computational Notions of Entropy:Classical, Quantum, and Applications*, 2019 ([pdf](https://dash.harvard.edu/bitstream/handle/1/42029772/CHEN-DISSERTATION-2019.pdf?sequence=1&isAllowed=y))

In the context of [[holographic entanglement entropy]]:

* [[Ning Bao]], [[Geoffrey Penington]], [[Jonathan Sorce]], [[Aron C. Wall]], Section 2.3 of: _Beyond Toy Models: Distilling Tensor Networks in Full AdS/CFT_,  JHEP 2019:69 ([arXiv:1812.01171](https://arxiv.org/abs/1812.01171))


[[!redirects min-entropy]]
[[!redirects min-entropies]]

[[!redirects min entropy]]
[[!redirects min entropies]]
