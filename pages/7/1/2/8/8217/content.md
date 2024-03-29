
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Definition

For $C_\bullet$ a [[chain complex]], the _truncation_ $(\tau_{\leq} C)_\bullet$ at some $n \in \mathbb{N}$ is the chain complex defined by

$$
  (\tau_n C)_i = 
  \left\{
    \array{
      0 & | i \gt  n \\
      C_n/B_n & | i = n \\
      C_n & | i \lt n
    }
  \right.
 \,,
$$

where $B_n = im(d_n)$.

For connective chain complexes this is the notion of [[truncated object in an (infinity,1)-category]] realized in the [[(infinity,1)-category of chain complexes]].

## References

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

