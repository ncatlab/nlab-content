
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[Pin group]] in [[dimension]] 2.

## Properties

Let $\mathbb{H} \simeq \mathbb{C} \oplus j \mathbb{C}$ be the [[quaternions]] realized as the [[Cayley-Dickson double]] of the [[complex numbers]], and identify the [[circle group]]

$$
  SO(2) \simeq S\big( \mathbb{C}\big) \hookrightarrow \mathbb{H}
$$

with the [[unit circle]] in $\mathbb{C} \hookrightarrow \mathbb{H}$ this way, with group structure now thought of as given by multiplication of [[quaternions]]. Then the [[Pin group]] $Pin_-(2)$ is [[isomorphism|isomorphic]] to the [[subgroup]] of the [[group of units]] $\mathbb{H}^\times$ of the [[quaternions]] which consists of this copy of [[SO(2)]], together with the multiples of the imaginary quaternion $j$ with this copy:

$$
  Pin_-(2)
  \;\simeq\;
  S\big( \mathbb{C}\big) 
   \;\cup\; 
  j \cdot S\big( \mathbb{C}\big) 
  \;\subset\;
  \mathbb{H}^\times
  \,.
$$

This is in fact inside the [[unit sphere]] $S(\mathbb{H}) \simeq $ [[Spin(3)]]. 

By the classification of the [[finite subgroups of Spin(3)]] this means that the restriction of $Pin_-(2)$ to the inclusion of the [[dihedral group]] $D_{2n}$ into the [[orthogonal group]] $O(2)$ is the [[binary dihedral group]] $2 D_{2n}$:

$$
  \array{
    2 D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Pin_-(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    \\
    D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    O(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

### Appearance in Seiberg-Witten theory and Floer homology

On a [[spin structure|spin]] [[4-manifold]], the $U(1)$-symmetry of the [[Seiberg-Witten equations]] enhances to a $Pin(2)$-symmetry ([Furuta 01](#Furuta01)). Because of this, $Pin(2)$-equivariance appears in [[Seiberg-Witten theory]] and [[Floer homology]]. See the references below.



## Related concepts

[[!include low dimensional rotation groups -- table]]


## References

$Pin(2)$-[[equivariant homotopy theory]]/[[equivariant cohomology theory]] 

application to [[Seiberg-Witten theory]] and [[Floer homology]]:

* {#Furuta01} Mikio Furuta, [_Monopole equation and the $11/8$-conjecture_](https://www.intlpress.com/site/pub/files/_fulltext/journals/mrl/2001/0008/0003/MRL-2001-0008-0003-a005.pdf) Mathematical Research Letters, Volume 8, Number 3, (2001).

* Ciprian Manolescu, _$Pin(2)$-equivariant Seiberg-Witten Floer homology and the Triangulation Conjecture_ ([arXiv:1303.2354](https://arxiv.org/abs/1303.2354))

* Matthew Stoffregen, _$Pin(2)$-equivariant Seiberg-Witten Floer homology of Seifert fibrations_ ([arXiv:1505.03234](https://arxiv.org/abs/1505.03234))

* Matthew Stoffregen, _A Remark on $Pin(2)$-Equivariant Floer Homology_,     Michigan Math. J. Volume 66, Issue 4 (2017), 867-884 ([euclid:1508810818](https://projecteuclid.org/euclid.mmj/1508810818))

$Pin(2)$-[[equivariant K-theory|equivariant]] [[KO-theory]]:

* Jianfeng Lin, _Pin(2)-equivariant KO-theory and intersection forms of spin four-manifolds_, Algebr. Geom. Topol. 15 (2015) 863-902 ([arXiv:1401.3264](https://arxiv.org/abs/1401.3264))

[[!redirects Pin(2)-group]]
[[!redirects Pin(2) group]]

[[!redirects pin(2)]]
[[!redirects pin(2)-group]]
[[!redirects pin(2) group]]


 