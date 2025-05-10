
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A *4-manifold* is a [[manifold]] of [[dimension of a manifold|dimension]] 4.

## Examples

* [[4-sphere]]

* $U(2)$

* [[spacetime]]

* [[E8-manifold|$E_8$ manifold]]

## Properties

#### Cohomotopy

Let $X$ be a [[4-manifold]] which is [[connected topological space|connected]] and [[orientation|oriented]].

The [[Pontryagin-Thom construction]] as [above](cohomotopy#RelationToCobordismGroup) gives for $n \in \mathbb{Z}$ the [[commuting diagram]] of sets

$$
  \array{
     \pi^n(X) 
       &\overset{\simeq}{\longrightarrow}&
     \mathbb{F}_{4-n}(X)
     \\
     {}^{ \mathllap{h^n} }
     \downarrow
       &&
     \downarrow^{ h_{4-n} }
     \\
     H^n(X,\mathbb{Z})
       &\underset{\simeq}{\longrightarrow}&
     H_{4-n}(X,\mathbb{Z})
     \,,
  }
$$

where $\pi^\bullet$ denotes [[cohomotopy]] sets, $H^\bullet$ denotes [[ordinary cohomology]], $H_\bullet$ denotes [[ordinary homology]] and $\mathbb{F}_\bullet$ is [[normal bundle|normally]] [[framing|framed]] [[cobordism classes]] of [[normal bundle|normally]] [[framing|framed]] [[submanifolds]]. Finally $h^n$ is the operation of pullback of the generating integral cohomology class on $S^n$ (by the nature of [[Eilenberg-MacLane spaces]]):

$$
  h^n(\alpha) \;\colon\; X \overset{\alpha}{\longrightarrow} S^n \overset{generator}{\longrightarrow} B^n \mathbb{Z}
  \,.
$$

Now 

* $h^0$, $h^1$, $h^4$ are [[isomorphisms]]

* $h^3$ is an isomorphism if $X$ is "odd" in that it contains at least one closed oriented [[surface]] of odd self-intersection, otherwise $h^3$ becomes an isomorphism on a $\mathbb{Z}/2$-[[quotient group]] of $\pi^3(X)$ (which is a group via the [[group]]-[[structure]] of the [[3-sphere]] ([[special unitary group|SU(2)]]))

([Kirby-Melvin-Teichner 12](#KirbyMelvinTeichner12))


## Related concepts

* [[Yang-Mills instanton]]

* [[Donaldson-Thomas invariants]]

[[!include low dimensional manifolds -- table]]

## References

### General

* [[Neil Strickland]], section 13 of: *A Bestiary of Topological Objects* \[<a href="https://strickland1.org/courses/bestiary/bestiary.pdf">pdf</a>, [[Strickland-BestiaryTopological.pdf:file]]\]


All [[PL manifold|PL]] [[4-manifolds]] are _simple_ [[branched covers]] of the  [[4-sphere]]:

* {#Piergallini95} [[Riccardo Piergallini]], _Four-manifolds as 4-fold branched covers of $S^4$_, Topology Volume 34, Issue 3, July 1995 (<a href="https://doi.org/10.1016/0040-9383(94)00034-I">doi:10.1016/0040-9383(94)00034-I</a>, [pdf](https://core.ac.uk/download/pdf/82379618.pdf))

* {#IoriPiergallini02} Massimiliano Iori, [[Riccardo Piergallini]], _4-manifolds as covers of the 4-sphere branched over non-singular surfaces_, Geom. Topol. 6 (2002) 393-401 ([arXiv:math/0203087](https://arxiv.org/abs/math/0203087))

On [[cohomotopy]] of 4-manifolds:

* [[Daniel Freed]], [[Karen Uhlenbeck]], Appendix B of: _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#KirbyMelvinTeichner12} [[Robion Kirby]], [[Paul Melvin]], [[Peter Teichner]]: *Cohomotopy sets of 4-manifolds*, Geometry & Topology Monographs **18** (2012) 161-190 &lbrack;[arXiv:1203.1608](https://arxiv.org/abs/1203.1608), [doi:10.2140/gtm.2012.18.161](http://dx.doi.org/10.2140/gtm.2012.18.161)&rbrack;


### Relation to 2d CFTs via 6d CFT

On [[KK-compactification]] of [[D=6 N=(2,0) SCFT]] on [[4-manifolds]] to [[2d CFTs]]:

* [[Abhijit Gadde]], [[Sergei Gukov]], [[Pavel Putrov]], *Fivebranes and 4-manifolds*, in: *Arbeitstagung Bonn 2013*, Progress in Mathematics **319**, Birkhäuser (2016) &lbrack;[arXiv:1306.4320](https://arxiv.org/abs/1306.4320), [doi:10.1007/978-3-319-43648-7_7](https://doi.org/10.1007/978-3-319-43648-7_7)&rbrack;

* [[Mykola Dedushenko]], [[Sergei Gukov]], [[Pavel Putrov]], *Vertex algebras and 4-manifold invariants*, Chapter 11 in: *Geometry and Physics: Volume I*  (2018) 249–318 &lbrack;[arXiv:1705.01645](https://arxiv.org/abs/1705.01645), [doi:10.1093/oso/9780198802013.003.0011](https://doi.org/10.1093/oso/9780198802013.003.0011)&rbrack;

* [[Boris Feigin]], [[Sergei Gukov]], $VOA[M_4]$, J. Math. Phys. **61** 012302 (2020) &lbrack;[arXiv:1806.02470](https://arxiv.org/abs/1806.02470), [doi:10.1063/1.5100059](https://doi.org/10.1063/1.5100059)&rbrack;

In relation to [[M5-brane elliptic genus]]:

* {#GukovPeiPutrovVafa18} [[Sergei Gukov]], [[Du Pei]], [[Pavel Putrov]], [[Cumrun Vafa]], *4-manifolds and topological modular forms*,  J. High Energ. Phys. **2021** 84 (2021) &lbrack;[arXiv:1811.07884](https://arxiv.org/abs/1811.07884), <a href="https://doi.org/10.1007/JHEP05(2021)084">doi:10.1007/JHEP05(2021)084</a>, [spire:1704312](https://inspirehep.net/literature/1704312)&rbrack;

and in relation to [[QFT with defects|defects]]:

* [[Jin Chen]], [[Wei Cui]], [[Babak Haghighat]], [[Yi-Nan Wang]], *SymTFTs and Duality Defects from 6d SCFTs on 4-manifolds*, JHEP **2023** 208 (2023) &lbrack;[arXiv:2305.09734](https://arxiv.org/abs/2305.09734), <a href="https://doi.org/10.1007/JHEP11(2023)208">doi:10.1007/JHEP11(2023)208</a>&rbrack;




[[!redirects 4-manifolds]]