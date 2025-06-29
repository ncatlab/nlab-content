
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


\tableofcontents

## Idea

For an odd integer $n$, and $a$ relatively prime to $n$, the *Jacobi symbol* $\left(\frac{a}{n}\right)$ (notated below as $(a \vert n)$) is the [[sign of the permutation]] on the group of units in the integers modulo $n$ where the permutation is given by multiplying by $a$. 

If $a$ and $n$ share a prime factor, then $(a \vert n)$ is set to $0$ by default. 

## Properties

* If $n = p$ is an odd prime, then the value of $(a \vert p)$ is the same as for the [[Legendre symbol]] $\left(\frac{a}{p}\right)$. 

* If the prime factorization of an odd integer $n$ is $p_1 p_2 \ldots p_k$, then 
$$(a \vert n) = \left(\frac{a}{p_1}\right)\left(\frac{a}{p_2}\right)\cdots \left(\frac{a}{p_k}\right).$$

* The quadratic reciprocity law holds in the generality of the Jacobi symbol: if $m, n$ are relatively prime odd integers, then 
$$(m \vert n)(n \vert m) = (-1)^{\frac{m-1}{2} \cdot \frac{n-1}{2}}.$$

## Related concepts 

* [[quadratic reciprocity law]] 

## References

See also:

* Wikipedia: *[Jacobi symbol](https://en.wikipedia.org/wiki/Jacobi_symbol)*

