
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A class of measures of [[entropy]] that are essentially logarithms of diversity indices. Let $p$ be a [[probability distribution]] over $n$ elements, and let $\alpha$ be a nonnegative [[real number]] not equal to 1. The Rényi entropy of order $\alpha$ of $p$ is

$$ H_\alpha(p) := \frac{1}{1-\alpha}\log\left(\sum_{i=1}^n p_i^\alpha\right) \, . $$

The $\alpha \to 1$ [[limit of a sequence|limit]] recovers the [[Shannon entropy]], and the $\alpha \to \infty$ [[limit of a sequence|limit]] yields the [[min-entropy]]. 

The Rényi entropy of order 2,

$$ H_2(p) = -\log \left(\sum_{i=1}^n p_i^2\right) \, , $$

is the negative logarithm of the "collision probability", i.e., the probability that two independent random variables both described by $p$ will take the same value.

## Related concepts

* [[min-entropy]]

* [[holographic Renyi entropy]]

## References

Due to:

* [[Alfréd Rényi]], *On Measures of Entropy and Information*, Berkeley Symposium on Mathematical Statistics and Probability, 1961: 547-561 (1961) ([euclid](https://projecteuclid.org/ebooks/berkeley-symposium-on-mathematical-statistics-and-probability/Proceedings%20of%20the%20Fourth%20Berkeley%20Symposium%20on%20Mathematical%20Statistics%20and%20Probability,%20Volume%201:%20Contributions%20to%20the%20Theory%20of%20Statistics/chapter/On%20Measures%20of%20Entropy%20and%20Information/bsmsp/1200512181))

See also

* Wikipedia, *[Rényi entropy](https://en.wikipedia.org/wiki/R%C3%A9nyi_entropy)*

On [[holographic Renyi entropy]] in relation to [[holographic entanglement entropy]] and [[quantum error correcting codes]]:

* [[Xi Dong]], *The Gravity Dual of Renyi Entropy*, Nature Communications 7, 12472 (2016) ([arXiv:1601.06788](https://arxiv.org/abs/1601.06788), [doi:10.1038/ncomms12472]( https://doi.org/10.1038/ncomms12472))

* [[Chris Akers]], [[Pratik Rath]], *Holographic Renyi entropy from quantum error correction*,  J. High Energ. Phys. 2019, 52 (2019) ([arXiv:1811.05171](https://arxiv.org/abs/1811.05171))

[[!redirects Rényi entropies]]

[[!redirects Renyi entropy]]
[[!redirects Renyi entropies]]

