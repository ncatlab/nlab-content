393
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

Given a [[field theory]] with [[scalar field|scalar fields]], a frequent question is whether it can be reinterpreted as a [[sigma-model]], where the scalars are the coordinates of some [[target space]]. For [d=4 N=2 supergravity](https://ncatlab.org/nlab/show/D%3D4+supergravity#on___supergravity_2) and [[D=5 supergravity|d=5 N=2 supergravity]], such target spaces correspond to smooth manifolds with structures collectively known as *special geometry*.

## History

The term *special geometry* first appears in ([Strominger (1990)](#Strominger90)) in the context of d=4 N=2 theories. The structure described therein eventually became known as *special Kähler*, allowing to relate structures other than Kähler to the "special" structure, which essentially refers to the existence of some *special* [[affine space|affine coordinates]]. These variants lead to different [[supersymmetry]] multiplets.

## Definition

The starting point of special geometries is an [[Hermitian manifold]] (see ([Lopes Cardoso & Mohaupt (2020)](#CMhes20))). One then introduces additional compatible structure to get the different variants of special geometries.

### Affine special real geometry

\begin{definition}
An affine special real manifold is a [[Hessian manifold]] $(M,g,\nabla)$ such that the Hessian potential is cubic polynomial in $\nabla$-affine (i.e. special) coordinates.
\end{definition}

This structure appears in the context of five-dimensional theories with vector multiplets ([CM20](#CMhes20)).

### Special Kähler geometry

There are at least two definitions of special Kähler geometry on a [[smooth manifold]] $M$. One is local in nature, phrased in terms of the existence of [[coordinates]] satisfying certain conditions, first appearing in ([de Wit, Lauwers & van Proeyen (1985)](#DWLvP85)). The other definition is global, which we recall below. These two definitions are shown to be equivalent in [Strominger (1990)](#Strominger90).

\begin{definition}

Let $M$ be an $n$-dimensional [[Kähler manifold]] such that its Kähler form $J$ represents in [[de Rham cohomology]] the [[first Chern class]] of a complex [[line bundle]] $L$. Let $H$ be a [[holomorphic vector bundle|holomorphic]] $\text{Sp}(2n+2,\mathbb{R})$ (the [[symplectic group]]) vector bundle over $M$ and $(-,-)$ a compatible [[Hermitian form|Hermitian]] [[inner product|metric]] on $H$. Then $M$ is a **special Kähler manifold**, meaning it admits special geometry, if there exists a [[holomorphic function|holomorphic]] section $\Omega$ of $H\otimes L$ such that

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

\end{definition}

A more general notion is __special complex geometry__ defined in [ACD02](#AlekseevskyCortésDevchand02):  a complex manifold $(M,J)$ with a flat torsionfree connection $\nabla$ such that $\nabla J$ is symmetric.

## Examples

* The [[moduli spaces]] of [[3d Calabi-Yau object
|Calabi-Yau threefolds]] and of $c=9$ $(2,2)$ [[SCFTs]] both admit special geometries.

* The base of any algebraically completely [[integrable system]] has canonically defined special geometry and conversely, any special Kähler manifolds is a base of some integrable system ([Freed 1999](#Freed99)).

## Related concepts

* [[supergravity]]

* [[Hessian manifold]]

## References

* {#dWLvP85} [[Bernard de Wit]], P.G. Lauwers, [[Antoine Van Proeyen]]. *Lagrangians of N = 2 supergravity-matter systems*, Nuclear Physics B **255** (1985) 569--608 [doi](https://doi.org/10.1142/9789814542340_0040)

* {#Strominger90} [[Andrew Strominger]], _Special geometry_,  Comm. Math. Phys. __133__:1 (1990), 163--180 &lbrack;[euclid:cmp/1104201320](http://projecteuclid.org/euclid.cmp/1104201320)&rbrack;

* {#Freed99} [[Daniel Freed]], _Special Kähler manifolds_, Comm. Math. Phys. __203__ (1999) 31--52 &lbrack;[doi:10.1007/s002200050604](https://doi.org/10.1007/s002200050604)&rbrack;

* {#CMhes20} Gabriel Lopes Cardoso, [[Thomas Mohaupt]]. *Special geometry, Hessian structures and applications*. Physics Reports __855__ (2020) 1--141. ([doi](https://doi.org/10.1016/j.physrep.2020.02.002))

* B. Craps, F. Roose, W. Troost, [[Antoine Van Proeyen]], *What is special Kähler geometry?* , Nuclear Physics B __503__:3 (1997) 565--613 (<a href="https://doi.org/10.1016/S0550-3213(97)00408-2">doi</a> arXiv:[hep-th/9703082](https://arxiv.org/abs/hep-th/9703082))

> We show equivalences of some definitions and give examples which show that earlier definitions are not equivalent, and are not sufficient to restrict the Kähler metric to one that occurs in N = 2 supersymmetry.

* [[Pietro Fré]], _Lectures on special Kähler geometry and electric-magnetic duality rotations_, Nucl. Phys. B Proc. Suppl. __45__:2-3, pp. 59--114 (1996) ([hep-th/9512043](https://arxiv.org/abs/hep-th/9512043) <a href="https://doi.org/10.1016/0920-5632(95)00629-X">doi</a>)

Freed's approach to special Kähler geometry is generalized to special complex geometry in

* {#AlekseevskyCortésDevchand02} [[Dmitry Vladimirovich Alekseevsky|D. V. Alekseevsky]], V. Cortés, C. Devchand, _Special complex manifolds_, Journal of Geometry and Physics __42__:1-2 (2002) 85--105 <a href="https://doi.org/10.1016/S0393-0440(01)00078-X">doi</a>


[[!redirects special geometries]]

