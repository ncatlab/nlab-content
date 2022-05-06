

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
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

The [[equivariant cohomology|equivariant]] [[generalized cohomology theory]] which is [[Brown representability theorem|represented]] by the [[equivariant sphere spectrum]] may also be called _equivariant stable cohomotopy_, as it is the [[equivariant stable homotopy theory]] version of [[stable cohomotopy]], hence of [[cohomotopy]].

Just as the plain [[sphere spectrum]] is a distinguished object of plain [[stable homotopy theory]], so the [[equivariant sphere spectrum]] is distinguished in [[equivariant stable homotopy theory]] and hence so is equivariant stable cohomotopy theory.

## Properties

### Equivariant stable $\pi_3^{\mathbb{S}}$

See at _[quaternionic Hopf fibration --  Class in equivariant stable homotopy theory](quaternionic+Hopf+fibration#ClassInEquivariantStableHomotopyTheory)_


## Examples

### Of the point: The Burnside ring

+-- {: .num_prop #BurnsideRingIsEquivariantStableCohomotopyOfPoint}
###### Proposition
**([[Burnside ring is equivariant stable cohomotopy of the point]])**

Let $G$ be a [[finite group]], then its [[Burnside ring]] $A(G)$ is [[isomorphism|isomorphic]] to the [[equivariant stable cohomotopy]] [[cohomology ring]] $\mathbb{S}_G(\ast)$ of the [[point]] in degree 0. 

$$
  A(G) \overset{\simeq}{\longrightarrow} \mathbb{S}_G(\ast)
  \,.
$$

=--

This is due to [Segal 71](#Segal71), a detailed proof is given by [tom Dieck 79, theorem 8.5.1](#tomDieck79). See also [Lück 05, theorem 1.13](#Lueck05), [tom Dieck-Petrie 78](#tomDieckPetrie78).

[[!include Segal completion -- table]]


More explicitly, this means that the Burnside ring of a group $G$ is isomorphic to the [[colimit]]

$$
  A(G) \simeq \underset{\longrightarrow}{\lim}_V [S^V,S^V]_G
$$

over $G$-[[representations]] in a complete [[G-universe]], of $G$-[[homotopy classes]] of $G$-equivariant based [[continuous functions]] from the [[representation sphere]] $S^V$ to itself ([Greenlees-May 95, p. 8](#GreenleesMay95)).



## Related concepts

[[!include flavours of cohomotopy -- table]]


* [[Burnside ring]]

* [[Segal conjecture]], [[Sullivan conjecture]]

## References

Relation to [[Burnside ring]]

* {#Segal71} [[Graeme Segal]], _Equivariant stable homotopy theory_, In Actes du Congr&egrave;s International des Math &eacute;maticiens (Nice, 1970), Tome 2 , pages 59–63. Gauthier-Villars, Paris, 1971

* {#tomDieckPetrie78} [[Tammo tom Dieck]], T. Petrie,  _Geometric modules over the Burnside ring_, Invent. Math. 47 (1978) 273-287 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/tomDieck-geometric.pdf))

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Springer 1979

Relation to [[Segal-Carlsson completion theorem]]:

* Czes Kosniowski, _Equivariant cohomology and Stable Cohomotopy_, Math. Ann. 210, 83-104 (1974) ([pdf](https://link.springer.com/content/pdf/10.1007/BF01360033.pdf))

* Erkki Laitinen, _On the Burnside ring and stable cohomotopy of a finite group_,  Mathematica Scandinavica Vol. 44, No. 1 (August 30, 1979), pp. 37-72 ([jstor:24491306](https://www.jstor.org/stable/24491306), [[Laitinen79.pdf:file]])  

* [[Gunnar Carlsson]], _Equivariant Stable Homotopy and Segal's Burnside Ring Conjecture_,  Annals of Mathematics Second Series, Vol. 120, No. 2 (Sep., 1984), pp. 189-224 ([jstor:2006940](https://www.jstor.org/stable/2006940), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/carlsson.pdf))

* {#Lueck05} [[Wolfgang Lück]], _The Burnside Ring and Equivariant Stable Cohomotopy for Infinite Groups_ ([arXiv:math/0504051](https://arxiv.org/abs/math/0504051))

* Noe Barcenas, _Nonlinearity, Proper Actions and Equivariant Stable Cohomotopy_ ([arXiv:1302.1712](https://arxiv.org/abs/1302.1712))

Discussion of unstable equivariant [[cohomotopy]] is in 

* {#Cruickshank03} James Cruickshank, _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">doi:10.1016/S0166-8641(02)00183-9</a>)


A lift of [[Seiberg-Witten invariants]] to classes in [[circle group]]-equivariant stable cohomotopy is discussed in

* Stefan Bauer, Mikio Furuta _A stable cohomotopy refinement of Seiberg-Witten invariants: I_ ([arXiv:math/0204340](http://arxiv.org/abs/math/0204340))

* Stefan Bauer, _A stable cohomotopy refinement of Seiberg-Witten invariants: II_ ([arXiv:math/0204267](http://arxiv.org/abs/math/0204267))

* Christian Okonek, Andrei Teleman, _Cohomotopy Invariants and the Universal Cohomotopy Invariant Jump Formula_, J. Math. Sci. Univ. Tokyo 15 (2008), 325-409 ([pdf](http://www.matmor.unam.mx/~barcenas/nonlinearity.pdf))

Discussion of [[M-brane]] physics in terms of [[equivariant rational homotopy theory|rational]] equivariant [[cohomotopy]] is in 

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

[[!redirects equivariant stable cohomotopy theory]]
[[!redirects equivariant stable cohomotopy theories]]
