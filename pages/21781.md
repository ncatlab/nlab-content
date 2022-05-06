
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


Let $G$ be a [[compact Lie group]] and let $X$ be a [[smooth manifold]] equipped with a [[smooth function|smooth]] [[action]] of $G$.

If this is a [[free action]], hence if $X$ is the total space $X = P$ of a $G$-[[principal bundle]] $P \to B$, then the _Cartan map_ (or _Cartan's map_ or similar) is a [[quasi-isomorphism]] from the [[Cartan model]] for the [[equivariant de Rham cohomology]] of $X = P$ to the ordinary [[de Rham complex]] model for the ordinary [[de Rham cohomology]] of the base manifold $B$:

$$
  \array{
    \overset{
      \color{blue}
      \text{Cartan model}
    }{
    \bigg(
       \Big(
         \Omega^\bullet\big(P \big)
         \otimes
         \mathbb{R}\big[ \{r^a\}_a \big] 
       \Big)^G
       \,,\,
       d_{dR} + r^a \iota_{v^a}
    \bigg)
    }
    &
    \overset{
       \color{blue}
       \text{Cartan's map}
    }{
    \overset{
       \simeq_{qi}
    }{\longrightarrow}
    }
    &
    \overset{
      \color{blue}
      \text{de Rham complex}
    }{
    \Big(
      \Omega^\bullet_{dR}(B),
      \,
      d_{dR}
    \Big)
    }
    \\
    \omega \otimes \langle - \rangle
    &
    \mapsto
    &
    \omega_{hor} \otimes \langle F_\nabla\rangle
  }
$$

given by choosing an [[Ehresmann connection]] $\nabla$ on $P \to B$ and inserting its [[curvature form]] into the [[invariant polynomials]] $\langle-\rangle$ (essentially the [[Chern-Weil homomorphism]]).


A full proof is due to [Guillemin-Sternberg 99, Chapter 5](#GuilleminSternberg99) (which reporduces [[Henri Cartan]]'s original articles in its appendix). Review includes [Meinrenken 06](#Meinrenken06), [Albin-Melrose 09, Theorem 11.1](#AlbinMelrose09).

## Related concepts

* [[Chern-Weil homomorphism]]

* [[Cartan calculus]], [[Cartan's magic formula]]


## References


* {#GuilleminSternberg99} [[Victor Guillemin]], [[Shlomo Sternberg]], _Supersymmetry and equivariant de Rham theory_, Springer, (1999) ([doi:10.1007/978-3-662-03992-2](https://link.springer.com/book/10.1007/978-3-662-03992-2))

* {#Meinrenken06} [[Eckhard Meinrenken]], _Equivariant cohomology and the Cartan model_, in: _Encyclopedia of Mathematical Physics_, Pages 242-250 Academic Press 2006 ([pdf](http://www.math.toronto.edu/mein/research/enc.pdf), [doi:10.1016/B0-12-512666-2/00344-8](https://doi.org/10.1016/B0-12-512666-2/00344-8))

* {#AlbinMelrose09} Pierre Albin, [[Richard Melrose]], _Equivariant cohomology and resolution_ ([arXiv:0907.3211](https://arxiv.org/abs/0907.3211))


