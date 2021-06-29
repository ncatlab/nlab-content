
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A kind of generalization of [[group characters]] to [[chromatic homotopy theory]].

Let $X//G$ be a [[topological stack|topological]] [[quotient stack]]. Its [[free loop space]] $\mathcal{L}(X//G) =  hom_{Stacks}(S^1, X//G)$ restricts to those loops that are constant as continuous maps, and contain only possibly the transition data with values in $X//G$ (i.e. the "[[twisted loop space]]" retaining "twisted sector" data), this is 

$$
  \mathcal{L}_{const}( X//G )
  \simeq
  hom_{Stacks}(\mathbf{B}\mathbb{Z}, X//G)
  \,.
$$

The [[geometric realization of simplicial topological spaces|geometric realization]] of $\mathcal{L}_{const}(X//G)$ is denoted $Fix(X)$ in ([Hopkins-Kuhn-Ravenel 00](#HopkinsKuhnRavenel00), [Stapleton 13, p. 2](#Stapleton13)).

Regarding $S^1$ as the [[circle group]], there is a canonical $S^1$ [[infinity-action]] on any free loop space $\mathcal{L}(-)$ (by rigid rotation of loops), and it restricts to $\mathcal{L}_{const}(-)$. Hence there is the [[homotopy quotient]] stack

$$
  \mathcal{L}_{const}( X//G ) // S^1
$$

The [[geometric realization of simplicial topological spaces|geometric realization]] of $\mathcal{L}_{const}(X//G) // S^1$ is denoted $Twist(X)$ in ([Stapleton 13, p. 2](#Stapleton13)).

Now with $n \in \mathbb{N}$ and given some prime, write $E_n$ for the $n$th [[Morava E-theory]] and $K(t)$ for the $t$th [[Morava K-theory]]. Then there is a homomorphism of Borel [[equivariant cohomology theories]]

$$
  E_n^\bullet(X//G)
    \longrightarrow
  B_{n-1}^\ast 
   \underset{L_{K(n-1)} E_n^\bullet(B \mathbb{Q}_p/\mathbb{Z}_p)}{\otimes}
  L_{K(n-1)} E^\bullet_n( \mathcal{L}_{const}( X//G ) )// S^1)
  \,,
$$

where $L_{(-)}$ denotes [[Bousfield localization of spectra|Bousfield localization]]. This is the _twisted transchromatic character map_ ([Stapleton 13, p. 5](#Stapleton13)), shown here for the special case $t = n-1$, in the notation there. 

Here $B_{n-1}$ is a ring such that... ([Stapleton 13, p. 3](#Stapleton13))


## Related concepts

* [[Chern character]]

* [[higher chromatic Chern character]]

* [[Morava E-theoretic Chern character]]

## References

For introduction see

* [[Nathaniel Stapleton]], _An Introduction to HKR Character Theory_ ([pdf](http://homepages.uni-regensburg.de/~stn30788/papers/Characters.pdf))

* {#Raksit15} Arpon Raksit, _Characters in global equivariant homotopy theory_, 2015 ([pdf](http://web.stanford.edu/~arpon/math/files/senior-thesis.pdf))

Original articles includes

* {#HopkinsKuhnRavenel00} [[Michael Hopkins]], [[Nicholas Kuhn]], [[Douglas Ravenel]], _Generalized group characters and complex oriented cohomology theories_, J. Amer. Math. Soc. 13 (2000), 553-594 ([publisher](http://www.ams.org/journals/jams/2000-13-03/S0894-0347-00-00332-5/), [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/hkr.pdf))

* {#Stapleton11} [[Nathaniel Stapleton]], _Transchromatic generalized character maps_, Algebr. Geom. Topol. 13 (2013) 171-203 ([arXiv:1110.3346](https://arxiv.org/abs/1110.3346), [euclid:agt/1513715495](https://projecteuclid.org/euclid.agt/1513715495))

* {#Stapleton13} [[Nathaniel Stapleton]], _Transchromatic twisted character maps_,  J. Homotopy Relat. Struct. 10, 29–61 (2015). ([arXiv:1304.5194](https://arxiv.org/abs/1304.5194), [doi:10.1007/s40062-013-0040-9](https://doi.org/10.1007/s40062-013-0040-9))

* [[Nathaniel Stapleton]], _Transchromatic generalized character maps (and more!)_ ([pdf](http://etale.site/livetex/saft/stapleton.pdf))

* [[Tomer Schlank]], [[Nathaniel Stapleton]], _A transchromatic proof of Strickland's theorem_ ([arXiv:1404.0717](http://arxiv.org/abs/1404.0717))

* [[Takeshi Torii]], _HKR characters, p-divisible groups and the generalized Chern character_, ([pdf](http://www.ams.org/journals/tran/2010-362-11/S0002-9947-2010-05194-3/S0002-9947-2010-05194-3.pdf))

[[!redirects transchromatic characters]]

[[!redirects tanschromatic character]]

[[!redirects transchromatic character map]]
[[!redirects transchromatic character maps]]
