


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Combinatorics
+--{: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

For $n \in \mathbb{N}_0$ a [[natural number]] or zero and $(k_i \in \mathbb{N}_0)_{i = 1}^r$ with $\underset{i}{\sum} k_i = n$, the corresponding _multinomial  coefficient_ 

$$
  \left(
     n
     \atop
     {
       k_1, k_2, \cdots, k_r  
     }
  \right)
  \;\coloneqq\;
  \frac{
     n!
  }{
    k_1 ! \, k_2 ! \, \cdots \, k_r
  }
  \;\in\;
  \mathbb{N}
$$

is the quotient of the [[factorial]] of $n$ by the [[multiplication]] of the factorials of the $k_i$.

This number is the number of ways of drawing $k_1$ elements and then $k_2$ elements and so forth from $n$ elements, all in an unordered way.

For $r = 2$ this is the _[[binomial coefficient]]_.

## Related entries

* [[binomial theorem]]

* [[binomial coefficient]]

## References

See also

* Wikipedia, _[Multinomial theorem](https://en.wikipedia.org/wiki/Multinomial_theorem)_

[[!redirects multinomial coefficients]]