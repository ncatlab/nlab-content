
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

In [[information theory]], *Rényi entropy* refers to a class of measures,  of [[entropy]] that are essentially [[logarithms]] of diversity indices.

For special values of its parameter, the notion of Rényy entropy reproduces all of: [[Shannon entropy]], [[Hartley entropy]]/[[max-entropy]] and [[min-entropy]].

## Definition

Let $p$ be a [[probability distribution]] over $n \in \mathbb{N}$ elements, and let $\alpha$ be a non-[[negative number|negative]] [[real number]] not equal to 1:

$$
  \alpha 
    \;\in\;
  \mathbb{R}_{\geq 0} \setminus \{1\}
  \,.
$$


The *Rényi entropy* of $p$ *at order $\alpha$* is:

$$ 
  H_\alpha(p) 
    \;\coloneqq\; 
  \frac{1}{1-\alpha}
  \log
  \left(
    \sum_{i=1}^n 
    (p_i)^\alpha
  \right) 
  \,. 
$$



## Properties

### Relation to other notions of entropy
 {#RelationToOtherNotionsOfEntropy}

For various (limiting) values of $\alpha$ the Rényi entropy reduces to notions of entropy that are known by their own names:

* for $\alpha = 0$, Rényi entropy equals the *[[Hartley entropy]]*/*[[max-entropy]]*,

* in the [[limit of a sequence|limit]] $\alpha \to 1$, Rényi entropy equals the [[Shannon entropy]], 

* for $\alpha = 2$, Rényi entropy equals the [[collision entropy]],


* in the [[limit of a sequence|limit]] $\alpha \to \infty$, Rényi entropy    equals the *[[min-entropy]]*.


[[!include Renyi entropies -- table ]]


### Monotonicity

The Rényi entropy is an anti-[[monotone function]] in the order-parameter $\alpha$:


$$
  \alpha_1 \;\leq\; \alpha_2
  \;\;\;\;\;\;\;
    \Rightarrow
  \;\;\;\;\;\;\;
  H_{\alpha_1}(p)
    \;\geq\;
  H_{\alpha_2}(p)
  \,.
$$

(e.g. [Ram & Sason 16, Fact 1](#RamSason16))

In particular, in terms of the [above](#RelationToOtherNotionsOfEntropy) special cases, this means that

$$
  HartlyEntropy 
  \;\geq\;
  ShannonEntropy
  \;\geq\;
  CollisionEntropy
  \;\geq\;
  MinEntropy
  \,.
$$


## Related concepts

* [[Hartley entropy]], [[Shannon entropy]], [[collision entropy]], [[min-entropy]]

* [[holographic Renyi entropy]]

## References

Due to:

* [[Alfréd Rényi]], *On Measures of Entropy and Information*, Berkeley Symposium on Mathematical Statistics and Probability, 1961: 547-561 (1961) ([euclid](https://projecteuclid.org/ebooks/berkeley-symposium-on-mathematical-statistics-and-probability/Proceedings%20of%20the%20Fourth%20Berkeley%20Symposium%20on%20Mathematical%20Statistics%20and%20Probability,%20Volume%201:%20Contributions%20to%20the%20Theory%20of%20Statistics/chapter/On%20Measures%20of%20Entropy%20and%20Information/bsmsp/1200512181))

Textbook account:

* J. Aczél, Z. Daróczy, Chapter 5 of: *On Measures of Information and their Characterizations*, Mathematics in Science and Engineering **115**, Academic Press 1975 ([ISBN:978-0-12-043760-3](https://www.sciencedirect.com/bookseries/mathematics-in-science-and-engineering/vol/115/suppl/C))

See also

* Wikipedia, *[Rényi entropy](https://en.wikipedia.org/wiki/R%C3%A9nyi_entropy)*

* {#RamSason16} Eshed Ram, Igal Sason, *On Renyi Entropy Power Inequalities* ([arXiv:1601.06555](https://arxiv.org/abs/1601.06555))


On [[holographic Renyi entropy]] in relation to [[holographic entanglement entropy]] and [[quantum error correcting codes]]:

* [[Xi Dong]], *The Gravity Dual of Renyi Entropy*, Nature Communications 7, 12472 (2016) ([arXiv:1601.06788](https://arxiv.org/abs/1601.06788), [doi:10.1038/ncomms12472]( https://doi.org/10.1038/ncomms12472))

* [[Chris Akers]], [[Pratik Rath]], *Holographic Renyi entropy from quantum error correction*,  J. High Energ. Phys. 2019, 52 (2019) ([arXiv:1811.05171](https://arxiv.org/abs/1811.05171))

[[!redirects Rényi entropies]]

[[!redirects Renyi entropy]]
[[!redirects Renyi entropies]]

