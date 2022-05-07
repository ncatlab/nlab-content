
> This entry is about the notion in [[number theory]]/[[combinatorics]]. For partition functions in the sense of [[statistical mechanics]] and [[quantum field theory]] see at *[[partition function]]*.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[number theory]]/[[combinatorics]], the [[function]] which assigns to a [[natural number]] $n \in \mathbb{N}$ the [[number]] $p(n)$ of its [[partitions]] (into [[multisets]] of [[positive number|positive]] [[natural numbers]]) is often called the *paritition function*.


## Properties

### Generating function

Its (ordinary) [[generating function]] is 

$$ 
  \sum_{n=0}^\infty p(n) x^n = \prod_{k=1}^\infty (1 - x^k)^{-1}
  \,.
$$

### Asymptotic expansion
 {#AsymptoticExpansion}

An [[asymptotic expansion]] of the partition function is ([Hardy & Ramanujan 1918](#HardyRamanujan1918), see [DeSalvo 20](#DeSalvo20) for discussion)

$$
 p(n)
  \;\sim\;
 \frac
   { e^{ \sqrt{2/3}\pi \cdot \sqrt{n} } }
   { 4 \sqrt{3} \cdot n}
 \,.
$$

## References

* On-Line Encyclopedia of Integer Sequences, *[OEIS A000041](https://oeis.org/A000041)*

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Partition_function_(number_theory)">Partition function (number theory)</a>*

Asymptotic behaviour:

* {#HardyRamanujan1918} [[Godfrey Hardy]], [[Srinivasa Ramanujan]], *Asymptotic formulaæ in combinatory analysis*, Proceedings of the London Mathematical Society, 2(1):75–115, 1918 ([doi:10.1112/plms/s2-17.1.75](https://doi.org/10.1112/plms/s2-17.1.75), [[HardyRamanujanAsymptoticFormulae.pdf:file]])

* {#DeSalvo20} Stephen DeSalvo, *Will the real Hardy-Ramanujan formula please stand up?* ([arXiv:2003.06908](https://arxiv.org/abs/2003.06908))

