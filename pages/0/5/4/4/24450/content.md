
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A generalization of [[quasigroup]] to [[n-ary operation]]s. 

## Definition

Given a natural number $n$, an $n$-ary quasigroup is a set $S$ with an $n$-ary operation $f:S^n \to S$ and $n$ $n$-ary operations $f_i^{-1}:S^n \to S$ for natural numbers $i \lt n$, such that, for $0 \lt m \lt n - 1$,

$$f(f_0^{-1}(a_1, \ldots a_{n - 1}, b), \ldots a_{n - 1}) = b$$

$$f(a_0, \ldots a_{m - 1}, f_m^{-1}(a_0, \ldots a_{m - 1}, a_{m + 1}, \ldots a_{n - 1}, b), a_{m + 1}, \ldots a_{n - 1}) = b$$

$$f(a_0, \ldots a_{n - 2}, f_{n - 1}^{-1}(a_0, \ldots a_{n - 2}, b)) = b$$

## See also

* [[quasigroup]]

* [[n-ary magma]]

* [[n-ary semigroup]]

* [[n-ary group]]

## References

* Wikipedia, [n-ary group](https://en.wikipedia.org/wiki/N-ary_group)
