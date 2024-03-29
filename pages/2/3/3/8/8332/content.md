
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In a [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$, the [[suspension object]] of a [[chain complex]] $C_\bullet$ is the complex 

$$
  \Sigma C_\bullet = C[1]_\bullet
$$

(or sometimes denoted $C[-1]_\bullet$, depending on an unessential choice of sign convention) obtained by shifting the [[graded object|degrees]] up by one:

$$
  C[1]_n \coloneqq C_{n-1}
$$

with the [[differential]] the original one but equipped with a sign:

$$
  d^{C[1]}_n \coloneqq - d^C_{n-1}
  \,.
$$

Generally, for $p \in \mathbb{Z}$, $C[p]$ is the chain complex with

$$
  C[p]_n \coloneqq C_{n-p}
$$

$$
  d^{C[p]}_n \coloneqq (-1)^p d^C_{n-p}
  \,.
$$



## Related concepts

* [[mapping cone]]

* [[loop space object]], [[free loop space object]],

  * [[delooping]]

  * [[loop space]], [[free loop space]], [[derived loop space]]

* [[suspension object]]

  * [[suspension]], [[reduced suspension]]

  * [[Sullivan model of a suspension]]

[[!redirects suspension of chain complexes]]
[[!redirects suspensions of a chain complex]]
[[!redirects suspensions of chain complexes]]

