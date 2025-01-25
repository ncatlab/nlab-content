
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


\tableofcontents


## Definition ##

Let $H\leq Sym(X)$ and $G\leq Sym(Y)$ be [[permutation groups]]. Then their *wreath product* $H \wr G$ is defined as the [[semidirect product group|semidirect product]] $H^Y \rtimes G$ where $G$ [[group action|acts]] on $H^Y$ by [[permutation|permuting]] the factors in the $Y$-indexed [[direct product group]] $H^Y$. 

Note that the wreath product is itself a permutation group, acting on $X\times Y$ by letting $G$ act trivially on the first and naturally on the second factor and letting $H^Y$ act on $X\times Y$ such that the $y$-th component of $H^Y$ permutes $X\times\{y\}$ naturally and fixes everything else pointwise.

## Examples ##

* Every group $G$ is a permutation group on its [[underlying]] [[set]] $|G|$ (the [[regular action]] aka the Cayley-Yoneda embedding $G\hookrightarrow Sym(|G|)$) and often only this special case is considered so that people speak of "**the** wreath product $H \wr G$" for abstract groups $G$ and $H$ without mentioning their permutation representations.

* $Dih(4)$ the [[dihedral group]] of [[order of a group|order]] $2\cdot 4=8$ is the wreath product $C_2 \wr C_2$ of [[cyclic group of order 2|$C_2$]] with itself (in this sense of regular representations).

* The [[Sylow p-subgroup|Sylow-$p$-subgroups]] $P_n$ of the [[symmetric groups]] $Sym(n)$ can be [[recursion|recursively]] described as the wreath product $C_p \wr P_a$ where $C_p$ is the [[cyclic group]] of [[order of a group|order]] $p$ and $n=ap+r$ with $0\leq r \lneq p$.

* The Sylow-$\ell$-subgroups of [[general linear group|$GL_n(q)$]] for $gcd(q,\ell)=1$ can be recursively described as a wreath product of the Sylow-$\ell$-subgroup of a strictly smaller $GL_{m}(q)$ and a Sylow-$\ell$-subgroups of a suitable symmetric group.


## Relation to the Borel construction

For $X$ a [[connected topological space|connected]] [[G-space]], the [[homotopy quotient]]/[[Borel construction]]

$$
  X \sslash G 
    \simeq_{whe}
  X \times_G E G
$$

has as [[fundamental group]]
the wreath product of $G$ with the fundamental group of $X$: 

$$
  \pi_1(X \sslash G)
  \simeq
  \pi_1(X) \wr G
  \,.
$$

(...)

## References 

Some general treatments

* W. Charles Holland, _The characterization of generalized wreath products_, J. Alg. 13 (1989) 152--172 [pdf](https://core.ac.uk/download/pdf/82380943.pdf)

See also:

* Wikipedia: *[Wreath product](https://en.m.wikipedia.org/wiki/Wreath_product)*
 
Important special cases/applications:

* G. Baumslag, _Wreath products and extensions_, Math Z 81, 286--299 (1963) [doi](https://doi.org/10.1007/BF01111576)
* [[I. G. Macdonald]], _Polynomial functors and wreath products_, J. Pure Appl. Alg. __18__ (1980) 173--204 [pdf](https://core.ac.uk/download/pdf/82423307.pdf)

For semigroups:

* [[Charles Wells]], _Some applications of the wreath product construction_, Amer. Math. Monthly __83__:5 (1976) [doi](https://doi.org/10.1080/00029890.1976.11994114)


category: algebra

[[!redirects wreath products of groups]]