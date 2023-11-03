
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Given a [[field theory]] with [[scalar field|scalar fields]], a frequent question is whether it can be reinterpreted as a [[sigma-model]], where the scalars are the coordinates of some [[target space]]. For [d=4 N=2 supergravity](https://ncatlab.org/nlab/show/D%3D4+supergravity#on___supergravity_2), such target spaces correspond to smooth manifolds with *special geometry*.

## Definition

There are at least two definitions of special geometry on a [[smooth manifold]] $M$. One is local in nature, phrased in terms of the existence of [[coordinates]] satisfying certain conditions, first appearing in ([de Wit, Lauwers & van Proeyen (1985)](#DWLvP85)). The other definition is global, which we recall below. These two definitions are shown to be equivalent in [Strominger (1990)](#Strominger90).

+-- {: .num_defn #SpecialGeometry}
###### Definition

Let $M$ be an $n$-dimensional [[Kähler manifold]] such that its Kähler form $J$ represents in [[de Rham cohomology]] the [[first Chern class]] of a complex [[line bundle]] $L$. Let $H$ be a [[holomorphic vector bundle|holomorphic]] $\text{Sp}(2n+2,\mathbb{R})$ (the [[symplectic group]]) vector bundle over $M$ and $(-,-)$ a compatible [[Hermitian form|Hermitian]] [[inner product|metric]] on $H$. Then $M$ is a **special manifold**, meaning it admits special geometry, if there exists a [[holomorphic function|holomorphic]] section $\Omega$ of $H\otimes L$ such that

$$
J 
  \,=\, 
  -
  \frac{\mathrm{i}}{2\pi} 
 \partial\bar{\partial}
 \text{ln} 
 (\Omega,\bar{\Omega})
  \,.
$$

=--

## Examples

* The [[moduli spaces]] of [[3d Calabi-Yau object
|Calabi-Yau threefolds]] and of $c=9$ $(2,2)$ [[SCFTs]] both admit special geometries.

* The base of any algebraically completely [[integrable system]] has canonically defined special geometry ([Freed 1999](#Freed99)).

## Related concepts

* [[supergravity]]

* [[Hessian manifold]]

## References

* {#dWLvP85} [[Bernard de Wit]], P.G. Lauwers, A. Van Proeyen. *Lagrangians of N = 2 supergravity-matter systems*. Nuclear Physics B **255**. (1985) 569-608. 

* {#Strominger90} [[Andrew Strominger]], _Special geometry_,  Comm. Math. Phys. Volume 133, Number 1 (1990), 163-180 &lbrack;[euclid:cmp/1104201320](http://projecteuclid.org/euclid.cmp/1104201320)&rbrack;

* {#Freed99} [[Daniel Freed]], _Special Kähler manifolds_, Comm. Math. Phys. __203__ (1999) 31--52 &lbrack;[doi:10.1007/s002200050604](https://doi.org/10.1007/s002200050604)&rbrack;

[[!redirects special geometries]]

