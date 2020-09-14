

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Where the [[Chern-Weil homomorphism]] assigns [[characteristic forms]] in [[de Rham cohomology]] to [[principal bundles]], the _Cheeger-Simons homomorphism_ refines this to an assignment of [[secondary characteristic classes]] in [[ordinary differential cohomology]] to [[principal connections]]:

$$
  \array{
    G Connections(X)_{/\sim}
    &\overset{ 
      \overset{
        \color{blue}
        \text{Cheeger-Simons homomorphism}
      }{
        cs_G
      } 
    }{\longrightarrow}&
    Hom
    \Big(
      H^\bullet(B G;\, \mathbb{Z})
      \,,\,
      \widehat H^\bullet(X)
    \Big)
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    G Bundles(X)_{/\sim}
    &\underset{ 
      \underset{
        \color{blue}
        \text{Chern-Weil homomorphism}
      }{cw_G} 
    }{\longrightarrow}&
    Hom
    \Big(
      imv^\bullet(\mathfrak{g})
      \,,\,
      H_{dR}^\bullet(X)
    \Big)      
  }
$$

## References

* {#CheegerSimons85} [[Jeff Cheeger]],  [[James Simons]], Section 2 of: _Differential characters and geometric invariants_, pages 50&#8211;80 in: _Geometry and Topology_, Lecture Notes in Mathematics, vol 1167. Springer (1985)  ([pdf](http://numr.wdfiles.com/local--files/differential-cohomology/cheeger-simons.pdf), [doi:10.1007/BFb0075212](https://doi.org/10.1007/BFb0075212))

* [[Michael Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_, J. Differential Geom. Volume 70, Number 3 (2005), 329-452 ([arXiv:math.AT/0211216](http://arxiv.org/abs/math.AT/0211216), [euclid:1143642908](https://projecteuclid.org/euclid.jdg/1143642908))



