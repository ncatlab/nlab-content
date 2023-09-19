


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### In differential geometry

Let $\pi : P \to X$ be a [[bundle]] in the category [[Diff]] of [[smooth manifold]]s. 

The [[dg-algebra]] $\Omega^\bullet_{vert}(P)$ of _vertical differential forms_ on $P$ is the quotient of the [[de Rham complex]] dg-algebra $\Omega^\bullet(P)$ of all forms on $P$, by the dg-ideal of [[horizontal differential forms]], hence of all those forms that vanish when any one vector in their arguments is a [[vertical vector field]] in that it is in the [[kernel]] of the [[differential]] $d \pi : T P \to T X$.

For a trivial bundle $P = X \times F$ the underlying complex of $\Omega^\bullet_{vert}(P)$ is $\wedge^\bullet_{C^\infty(X \times F)} \Gamma(T^* F)$.

## Related concepts

* [[horizontal differential form]]

* [[Lie integration]]

## References

* Philippe Bonnet, Alexandru Dimca, _Relative differential forms and complex polynomials_, Bulletin des Sciences Mathématiques **124** Issue 7 (2000) pp 557-571, doi:[10.1016/s0007-4497(00)01055-1](https://doi.org/10.1016/s0007-4497%2800%2901055-1), ([author pdf](https://web.archive.org/web/20150326174153/https://jones.math.unibas.ch/~bonnet/Publications/Bullscience.pdf))

[[!redirects vertical differential forms]]

