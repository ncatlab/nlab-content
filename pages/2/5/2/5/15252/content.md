
#Contents#
* table of contents
{:toc}

## Idea

On a [[Kähler manifold]] $X$ a _Hodge cycle_ is a $2p$-[[cycle]] in integral [[ordinary homology]] which is represented by an element in Dolbeault homology of bidegree $(p,p)$.

Dually, a _Hodge cocycle_ on $X$ is an integral [[ordinary cohomology]] class of even degree $2p$ which is represented by an element in the [[Dolbeault cohomology]] group $H^{p,p}(X)$.

## Definition

For  $X$ be a [[Kähler manifold]] with [[Dolbeault cohomology]] groups $H^{p,q}(X)$, then for any $p \in \mathbb{N}$ the group $Hdg^p(X)$ of (cohomology classes represented by) **Hodge cocycles** is the [[fiber product]]

$$
  \array{
    && Hdg^p(X)
    \\
    & \swarrow && \searrow
    \\
    H^{2p}(X,\mathbb{Z}) && && H^{p,p}(X)
    \\
    & \searrow && \swarrow
    \\ 
    && H^{2p}(X,\mathbb{C})
  }
  \,.
$$

Since the left arrow here factors through real cohomology, this is in fact the same as the pullback

$$
  \array{
    && Hdg^p(X)
    \\
    & \swarrow && \searrow
    \\
    H^{2p}(X,\mathbb{Z}) && && F^p H^{2p}(X,\mathbb{C})
    \\
    & \searrow && \swarrow
    \\ 
    && H^{2p}(X,\mathbb{C})
  }
  \,,
$$

where $F^\bullet H^{2p}(X,\mathbb{C})$ is the [[Hodge filtration]] on the complex cohomology of $X$.

In this form the definition of Hodge cocycles generalizes to [[complex analytic spaces]] and to [[schemes]] over the [[complex numbers]] and in fact to any situation where there is a [[Hodge structure]] on any kind of [[cohomology theory]].

## References

The general formulation in terms of [[Hodge filtration]] for [[ordinary cohomology]] is noted for instance in 

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], section 7.8 of _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

in the context of discussion of [[intermediate Jacobians]].

The general formulation in terms of [[Hodge filtration]] for [[generalized (Eilenberg-Steenrod) cohomology]] is noted for instance in 


* {#HopkinsQuick12} [[Michael Hopkins]], [[Gereon Quick]], below remark 4.12 in _Hodge filtered complex bordism_ ([arXiv:1212.2173](http://arxiv.org/abs/1212.2173))

See also 


* Wikipedia, _[Hodge cycles](http://en.wikipedia.org/wiki/Hodge_cycle)_
[[!redirects Hodge cycles]]

[[!redirects Hodge cocycle]]
[[!redirects Hodge cocycles]]

[[!redirects Hodge cohomology class]]
[[!redirects Hodge cohomology classes]]

