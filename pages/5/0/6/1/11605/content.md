
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

The generalization of the concept of [[Jacobian variety]] to higher dimensional [[algebraic varieties]].

In [[differential geometry]] these appear as [[moduli spaces]] of [[flat infinity-connection|flat]] [[circle n-bundles with connection]] that are equipped with [[symplectic structure]] and [[Kähler polarization]] induced from any choice of [[complex structure]] on the base space. 


## Definition

### In complex geometry
 {#InComplexGeometry}

#### The underlying real manifold

Let $\Sigma$ be a [[projective variety|projective]] [[smooth variety|smooth]] [[complex variety]] (see at _[[GAGA]]_). 

For $k \in \mathbb{N}$ the _$k$th intermediate Jacobian_ of $\Sigma$ is, as a [[real manifold]], the [[quotient]]

$$
  J^{k+1}(\Sigma) 
    \coloneqq 
  H^{2k+1}(\Sigma,\mathbb{R})/H^{2k+1}(\Sigma,\mathbb{Z})
$$

of the [[ordinary cohomology|ordinary]] [[cohomology groups]] of $X$ with [[coefficients]] in the [[abelian groups]] of [[real numbers]] and of [[integers]], respectively, induced by the canonical inclusion $\mathbb{Z} \hookrightarrow \mathbb{R}$.

Here $H^{2k+1}(\Sigma,\mathbb{R})$ is naturally a [[vector space]] over the [[real numbers]] and this is what induces the [[smooth manifold]]-structure on the quotient. 

For eventually equipping this with the structure of a [[complex manifold]] one realizes this as the quotient of the [[complex vector space]] of cohomology with complex coefficients as follows:

Notice that a real [[differential form]] 

$$
  \alpha \in \Omega^{2k+1}_{\mathbb{R}}(\Sigma)
$$

is, by the [[Hodge theorem]], a sum of complex differential forms in homogeneous [[Dolbeault complex|Dolbeaut bidegree]] of the kind

$$
  \alpha = \alpha^{2k+1,0}+ \alpha^{2k,1} + \cdots + \overline{\alpha^{1,2k}} + \overline{\alpha^{0,2k+1}}
  \,.
$$

It follows with the [[de Rham theorem]] that there is a canonical [[isomorphism]] of real vector spaces

$$
  H^{2k+1}(\Sigma, \mathbb{R}) \simeq H^{2k+1}(\Sigma,\mathbb{C})/(F^{k+1} H^{2k+1}(\Sigma))
 \,,
$$

where 

$$
  F^{k+1} H^{2k+1}(\Sigma) \coloneqq \underset{p \geq k}{\oplus} H^{p,2k+1-p}(\Sigma)
$$

is the $k$th stage in the [[Hodge filtration]] of $H^{2k+1}(\Sigma,\mathbb{C})$. 

Hence an equivalent way to write the intermediate Jacobian (still asa realmanifold) as the quotient of the real manfifold underlying a complex vector space is

$$
  J^{k+1}(\Sigma)
   \simeq 
   H^{2k+1}(\Sigma,\mathbb{C})/(F^{k+1} H^{2k+1}(\Sigma) \oplus H^{2k+1}(\Sigma,\mathbb{Z}))
  \,.
$$

There are two canonical way to equip $H^{2k+1}(\Sigma,\mathbb{C})$, and hence the above quotient, with the structure of a [[complex manifold]]. Sometimes these agree, but in general they do not, and hence they go by different names,the 

* [Griffith intermediate Jacobian](#GriffithIntermediateJacobian)

and the


* [Weil intermediate Jacobian](#WeilIntermediateJacobian)


#### The Griffith complex structure
 {#GriffithIntermediateJacobian}

The [[isomorphism]]

$$
  H^{2k+1}(\Sigma , \mathbb{C})
  \simeq 
  H^{2k+1}(\Sigma , \mathbb{R})\otimes_{\mathbb{R}} (\mathbb{C})
$$

induces a [[complex manifold]] structure on $H^{2k+1}(\Sigma , \mathbb{C})$ and hence the structure of a [[complex torus]] on $k$th intermediate Jacobian as defined above. This is the structure originally defined in ([Griffiths 68a](#Griffiths68a), [Griffiths 68b](#Griffiths68b)) and hence called the _Griffith intermediate Jacobian_.  Reviews include ([Walls 12](#Walls12)).


#### Weil complex structure
 {#WeilIntermediateJacobian}

There is another natural [[complex structure]] on $H^{2k-1}(X, \mathbb{R})/H^{2k-1}(X, \mathbb{Z})$, equipped with that it is called the _Weil intermediate Jacobian_.

We describe it in mid dimension, where it is most interesting.

Let 

$$
  n \coloneqq dim_{\mathbb{C}}(\Sigma) = 2k+1
  \,.
$$

Choose a [[Hermitian manifold]] structure on $\Sigma$. Then [[Serre duality]] on mid-dimensional forms 

$$
  \bar \star \;\colon\; \Omega^{p,n-p}(\Sigma) \longrigtharrow \Omega^{n-p,p}(\Sigma)
$$

is an [[antilinear function]] which squares to -1. Therefore

$$
 i \bar \star \;\colon\;  H^{2k+1}(\Sigma,\mathbb{C}) \to  H^{2k+1}(\Sigma,\mathbb{C})
$$

is...


### Algebraically

At least for the plain [[Jacobian]] of a [[curve]] $\Sigma$ (hence $dim_{\mathbb{C}}(\Sigma) = 1$) one may reformulate as follows (e.g. [Polishchuk 03, section 16.4](#Polishchuk03)):

Notice that the canonical map 

$$
  H^1(\Sigma,\mathbb{R})
  \hookrightarrow 
  H^1(\Sigma, \mathbb{C})
  \to
  H^{0,1}(\Sigma)
  \stackrel{\simeq}{\to} H^1(\Sigma, \mathcal{O}_{\Sigma})
$$ 

is an [[isomorphism]]. (The first map is induced by the splitting $H^1(\Sigma, \mathbb{C}) \simeq H^1(\Sigma,\mathbb{R})\oplus i H^1(\Sigma,\mathbb{R})$ given by [[complexification]] and the second by the splitting $H^1(\Sigma,\mathbb{C}) \simeq H^{0,1}(\Sigma)\oplus H^{1,0}(\Sigma)$ of [[Dolbeault cohomology]], the last map is the [[Dolbeault isomorphism]]).


Now by the [[long exact sequence in cohomology]] of the [[exponential exact sequence]] we have that

$$
  \begin{aligned}
  J^1(\Sigma)
  & \coloneqq
  H^1(\Sigma, \mathbb{R})/H^1(\Sigma, \mathbb{Z})
  \\
  & \simeq
  H^1(\Sigma,\mathcal{O}_{\Sigma})/H^1(\Sigma, \mathbb{Z}) 
  \\
  & \simeq
  ker(H^1(\Sigma, \mathcal{O}^\times_{\Sigma})\to H^2(\Sigma, \mathbb{Z}))
  \\
  & = 
  Pic_0(\Sigma)
  \end{aligned}
$$

is the connected component of the [[Picard variety]] of $\Sigma$.



## Properties

### Cycle map / Abel-Jacobi map

The intermediate Jacobians receive canonical maps from cycles (...)
See at _[[Abel-Jacobi map]]_.

### Polarization

For a [[Hodge manifold]] the intermediate Jacobian canonically inherits the structure of a [[polarized variety]]. (...)


### Theta-characteristics

A certain [[square root]] of the [[canonical bundle]] on intermediate Jacobians -- hence a [[Theta characteristic]] -- in dimension $2k+1$ thought of as [[moduli spaces]] of (flat) [[circle n-bundles with connection|circle (2k+1)-bundles with connection]] yields the [[partition function]] of [[self-dual higher gauge theory]].  ([Witten 96](#Witten96), [Hopkins-Singer 02](#HopkinsSinger02)).


## Examples

### $n = 1$: Picard varitey

For $n =1$ the inermediate Jacobian  is the [[Jacobian variety]], the connected component of the [[Picard scheme]]:

$$
  J^1(X) = Pic^0_X
  \,.
$$ 

### $n = 2 dim(X)-1$: Albanese variety

For $n = 2 dim(X)-1$ then $J^{2 dim(X)-1}(X) = Alb(X)$
is called the _[[Albanese variety]]_ of $X$.


### Of elliptic curves

... [[moduli space of flat connections]]... [[Hitchin connection]]... [[modular functor]]... [[WZW model]]...

### Of Calabi-Yau 3-folds

A review of intermediate Jacobians of [[Calabi-Yau varieties]] of ([[complex manifold|complex]]) [[dimension]] 3 is in ([Baarsma 11, section 2](#Baarsma11)).

The (real) dimensional of the intermediate Jacobian of a CY3 $X$ is 

$$
  dim (J(X)) = 2(1+ h^{1,2})
$$

(e.g. [Baarsma 11, (2.21)](#Baarsma11))

Hence the intermediate Jacobian of a rigid CY3 (with $h^{1,2} = 0$) is an [[elliptic curve]] (e.g. [BKNPP 09, (1.8)](#BKNPP09)).

### $n = 3$: supergravity C-field

For the moment see at _[[7d Chern-Simons theory]]_ and at _[[M5-brane]]_.

### $n = 3$: type II 3-form 

For the [[RR-field]] component in degree 4 of [[type IIA superstring theory]]: ([Morrison 95](#Morrison95))


## Related concepts

[[!include moduli of higher lines -- table]]


## References

### General

Original articles include

* {#Griffiths68a} [[Phillip Griffiths]], _Periods of integrals on algebraic manifolds. I_ Construction and properties of the modular varieties", American Journal of Mathematics 90 (2): 568&#8211;626, (1968) doi:10.2307/2373545, ISSN 0002-9327, JSTOR 2373545, MR 0229641

* {#Griffiths68a} [[Phillip Griffiths]],  _Periods of integrals on algebraic manifolds. II_ Local study of the period mapping", American Journal of Mathematics 90 (3): 805&#8211;865 (1968), doi:10.2307/2373485, ISSN 0002-9327, JSTOR 2373485, MR 0233825

Reviews and surveys include

* [[eom]], _[Intermediate Jacobian](http://www.encyclopediaofmath.org/index.php/Intermediate_Jacobian)_

* Wikipedia, _[Intermediate Jacobian](http://en.wikipedia.org/wiki/Intermediate_Jacobian)_

* {#Walls12} [[Patrick Walls]], _Intermediate Jacobians and Abel-Jacobi maps_, 2012 ([[WallsJacobian.pdf:file]])

* {#Brylinski07} [[Jean-Luc Brylinski]], around theorem I 1.5.11 of _Loop Spaces, Characteristic Classes and Geometric Quantization_ Springer, 2007

* [[Arnaud Beauville]], _Vari&#233;t&#233;s de Prym et jacobiennes interm&#233;diaire_,  Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 3 (1977), p. 309-391   ([pdf](http://math.unice.fr/~beauvill/pubs/prym.pdf)) ([jstor]( http://www.numdam.org/item?id=ASENS_1977_4_10_3_309_0))

* Valentin Zakharevich, _Mixed Intermediate Jacobians_, 2012 ([pdf](http://www.algant.eu/documents/theses/zakharevich.pdf))


* {#Polishchuk03} [[Alexander Polishchuk]], _Abelian varieties, Theta functions and the Fourier transform_, Cambridge University Press (2003) ([pdf](http://math1.unice.fr/~beauvill/pubs/poli.pdf))


### For Calabi-Yau 3-folds

* C. Herbert Clemens, [[Phillip Griffith]], _The intermediate Jacobian of the cubic threefold_, Annals of Mathematics Second Series, Vol. 95, No. 2 (Mar., 1972), pp. 281-356 ([JSTOR](http://www.jstor.org/stable/1970801))

* [[Claire Voisin]] ([pdf](http://www.math.polytechnique.fr/~voisin/Articlesweb/griffithsgroup.pdf))

* [[Andreas Höring]], _Minimal classes on the intermediate Jacobian of a generic cubic threefold_, 2008 ([pdf](http://math.unice.fr/~hoering/articles/a5-intermediate.pdf))


In [[positive number|positive]] [[characteristic]]:

* {#GeerKatsura03} [[Gerard van der Geer]], T. Katsura, _On the height of Calabi-Yau varieties in positive characteristic_ ([arXiv:math/0302023](http://arxiv.org/abs/math/0302023))

Applications in [[string theory]]:

* {#Morrison95} [[David Morrison]], section 4 of _Mirror Symmetry and the Type II String_, Nucl.Phys.Proc.Suppl. 46 (1996) 146-155 ([arXiv:hep-th/9512016](http://arxiv.org/abs/hep-th/9512016))

* {#BKNPP09} Ling Bao, Axel Kleinschmidt, Bengt E. W. Nilsson, Daniel Persson, Boris Pioline, _Instanton Corrections to the Universal Hypermultiplet and Automorphic Forms on SU(2,1)_, Commun. Num. Theor. Phys. 4 (1), 187-266 (2010) ([arXiv:0909.4299](http://arxiv.org/abs/0909.4299))

* {#Baarsma11} A. Baarsma, _The hypermultiplet moduli space of compactified type IIA string theory_, Master Thesis, Utrecht 2011 ([web](http://dspace.library.uu.nl/handle/1874/203182))


The relation of Theta characteristics on [[intermediate Jacobians]] to [[self-dual higher gauge theory]] was first recognized in 

* {#Witten96} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J.Geom.Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))

and the argument there was made rigorous in 

* {#HopkinsSinger02} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_
 
[[!redirects intermediate Jacobians]]

[[!redirects Griffith intermediate Jacobian]]
[[!redirects Griffith intermediate Jacobians]]

[[!redirects Weil intermediate Jacobian]]
[[!redirects Weil intermediate Jacobians]]