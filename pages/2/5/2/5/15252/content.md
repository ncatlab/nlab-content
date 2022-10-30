
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

On a [[Kähler manifold]] $X$ a _Hodge cycle_ is a $2p$-[[cycle]] in integral [[ordinary homology]] which corresponds to an element in Dolbeault homology of bidegree $(p,p)$.

Dually, a _Hodge cocycle_ on $X$ is an integral [[ordinary cohomology]] class of even degree $2p$ which corresponds to an element in the [[Dolbeault cohomology]] group $H^{p,p}(X)$.

## Definition

### For K&#228;hler manifolds

+-- {: .num_defn #HodgeCohomologyGroupsForKaehlerManifolds}
###### Definition

For  $X$ be a [[Kähler manifold]] with [[Dolbeault cohomology]] groups $H^{p,q}(X)$, then for any $p \in \mathbb{N}$ the group  of **Hodge cohomology classes** represented by **Hodge cocycles** is the [[fiber product]] 

$$
  Hdg^p(X)
    \coloneqq
  H^{2p}(X,\mathbb{Z})
   \underset{H^{2p}(X,\mathbb{C})}{\times}
  H^{p,p}(X)
$$

in 

$$
  \array{
    && Hdg^p(X)
    \\
    & \swarrow && \searrow
    \\
    H^{2p}(X,\mathbb{Z}) && && H^{p,p}(X)
    \\
    & {}_{\mathllap{H^{2p}(X,\mathbb{Z} \hookrightarrow \mathbb{R})}}\searrow && \swarrow_{\mathrlap{\iota}_{p,p}}
    \\ 
    && H^{2p}(X,\mathbb{C})
  }
  \,
$$

where

* $\iota_{p,p}$ is the inclusion of the [[direct sum|direct summand]] given by the [[Hodge decomposition]];

* $H^{2p}(X,\mathbb{Z} \hookrightarrow \mathbb{R})$ is the morphism on cohomology groups induced by the canonical inclusion of [[coefficients]] ([[integers]] into [[complex numbers]]) as indicated.

=--

### For general complex analytic spaces

Def. \ref{HodgeCohomologyGroupsForKaehlerManifolds} has the following equivalent reformulation, which generalizes the definition to [[complex analytic spaces]] and to [[schemes]] over the [[complex numbers]].

Since the left arrow here factors through real cohomology, this is in fact the same as the pullback

+-- {: .num_defn #HodgeCohomologyGroupsForComplexAnalytic}
###### Definition

For $X$ a [[complex analytic space]] with [[Hodge filtration]] $F^\bullet H^{2p}(X,\mathbb{C})$ on its complex cohomology, then the group of **Hodge cohomology classes** represented by **Hodge cocycles** is the [[fiber product]]

$$
  Hdg^p(X)
  \coloneqq
    H^{2p}(X,\mathbb{Z})
   \underset{H^{2p}(X,\mathbb{C})}{\times}
  F^p H^{2p}(X,\mathbb{X})
$$

in

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
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

If the complex analytic space $X$ happens to carry the structure of a  [[Kähler manifold]], then definition \ref{HodgeCohomologyGroupsForComplexAnalytic} reduces to definition \ref{HodgeCohomologyGroupsForKaehlerManifolds}. 

=--

([e.g. Esnault-Viehweg 88, section 7.8](#EsnaultViehweg88))

+-- {: .proof}
###### Proof

The map from integral cohomology to complex cohomology factors through that of real cohomology via

$$
  \mathbb{Z} \hookrightarrow \mathbb{R}\hookrightarrow \mathbb{C}
$$

and by [[Hodge symmetry]] the real cohomology classes are precisely thos represented by elements of the form $\alpha + \overline{\alpha}$, where

$$
  \overline{(-)} \;\colon\; H^{\bullet_1, \bullet_2}(X) \to H^{\bullet_2, \bullet_1}(X)
$$

is [[complex conjugation]]. But the mid-dimensional [[Hodge filtration]] is

$$
  F^p H^{2p}(X,\mathbb{C})
  =
  H^{p,p}(X)
  \oplus 
  H^{p+1,p-1}(X)
  \oplus
  H^{p+2,p-2}(X)
  \oplus 
  \cdots
  \oplus
  H^{2p,0}(X)
$$

and hence the only elements invariant under complex conjugation -- hence the only real cohomology classes -- that it includes are those in $H^{p,p}(X)$, which is the subgroup appearing in def. \ref{HodgeCohomologyGroupsForComplexAnalytic}.

=--

+-- {: .num_remark}
###### Remark

In the form of def. \ref{HodgeCohomologyGroupsForComplexAnalytic} the definition of Hodge cocycles generalizes to any context in which there is a  [[Hodge structure]]. Notably it generalizes to a natural concept of Hodge cocycles in [[generalized (Eilenberg-Steenrod) cohomology]] ([e.g. Hopkins-Quick 12, below remark 4.12](#HopkinsQuick12))

=--

## Properties

### Relation to intermediate Jacobians

There is a canonical map from holomorphic [[Deligne cohomology]] ([[ordinary differential cohomology]]) $H^{2k+2}(X, \mathbb{Z}\to \Omega^0 \to \cdots\to \Omega^{k}\to 0 \to \cdots)$ to Hodge cocycles. The [[fiber]] of that map is the [[intermediate Jacobian]] $J^{k+1}(X)$. See there for details.

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

