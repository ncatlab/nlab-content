
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

In the context of [[probability theory]], the **max-entropy** or **Hartley entropy** of a [[probability distribution]] on a [[finite set]] is the [[logarithm]] of the number of outcomes with nonzero probability. 

In [[quantum probability theory]] this means that the max entropy is the logarithm of the [[rank]] of the [[density matrix]].

## Properties

### Relation to Shannon entropy

The ordinary [Shannon entropy](entropy#entropy_of_a_partition_of_a_discrete_probability_space) of a probability distribution is never greater than the max-entropy.

### Relation to Renyi entropy

The Hartley entropy of a finite probability distribution $(p_i)_{i = 1}^n$ is the special case of [[Renyi entropy]] 

$$
  S_\alpha(p)
  \;=\;
  \frac{1}{1 - \alpha}
  ln
  \left(
  \underoverset
    {i = i}
    {n}
    {\sum}
    (p_i)^\alpha
  \right)
$$

for $\alpha = 0$.

[[!include Renyi entropies -- table ]]


## Related entries

* [[min-entropy]]


## References

Review:

* Scholarpedia, *[Quantum entropies -- Hartley entropy](http://www.scholarpedia.org/article/Quantum_entropies#Max_entropy_.28Hartley_entropy.29)*

* J. Aczél, B. Forte and C. T. Ng, Advances in Applied Probability
Advances in Applied Probability, Vol. 6, No. 1 (Mar., 1974), pp. 131-146 ([jstor:1426210](https://www.jstor.org/stable/1426210))

[[!redirects max-entropies]]

[[!redirects Hartley entropy]]
[[!redirects Hartley entropies]]


